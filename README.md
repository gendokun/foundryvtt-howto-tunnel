# Übersicht 
In diesem kleinen Tutorial möchte ich euch zeigen wie ihr euer Foundry auf dem PC, ohne weitere Router Konfiguration oder Port-Forwarding, aus dem Internet erreichbar macht.
Dazu nutzen wir von Cloudflare ein typschies Produkt für Unternehmen, dass seitens des Herstellers kostenlos angeboten wird.
Es gibt keine Gewährleistung auf Performance or Verfügbarkeit, das entsprechend bedenken. 

Falls weiteres Interesse besteht, lasst es mich in den Issues wissen, dann zeige ich euch wie man dass mit "Cloudflare Teams" , in der kostenlosen Variante, weiter verbessern kann.

# Technischer Hintergrund
Zu schreiben


# Schritt für Schritt Anleitung

Wir nutzen die sog. "Quick Tunnel" Funktion die grundsätzlich hier beschrieben ist. [Quick Tunnels](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/run-tunnel/trycloudflare)

1. Download der Anwendung um die Tunnel Verbindung herzustellen -> [HIER](https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-windows-amd64.exe)
2. Kopieren der Anwendung in einen beliebigen Ordner - bspw. C:\Cloudflare
![Explorer Übersicht](/Windows_Explorer.jpg)
3. Öffnen einer Eingabeaufforderung via Windows Taste/Start
4. `cmd` eingeben
5. Wechseln in den Cloudflare Ordner 
![CMD Ordner](/CMD-Folder.jpg)
6. Starten der Tunnelanwendung via (in meinen Beispiel, Foundry Standard Port 30000)
`cloudflared-windows-amd64.exe tunnel --url http://localhost:30000`
![Tunnel Setup](/CF-Tunnel-setup.jpg)
7. Teilen eures Links für den Login. In meinem Beispiel hier ist mein Foundry jetzt unter
 `https://boxes-bass-beam-suddenly.trycloudflare.com` erreichbar (siehe Screenshot)
![Foundry Login](/FoundryLogin.jpg)
