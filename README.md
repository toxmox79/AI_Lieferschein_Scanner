UniversalScanner PWA
UniversalScanner ist eine Progressive Web App (PWA), die entwickelt wurde, um den Prozess des Hochladens von Lieferscheinen (PDF, Excel, CSV), des Extrahierens von Produktinformationen (EAN, Produkt, Menge, Details) und des Scannens von EANs für die Lagerverwaltung zu vereinfachen. Die App ermöglicht es Ihnen, den Bestand zu verfolgen, gescannte Mengen anzupassen und die Daten für die weitere Verarbeitung zu exportieren.

Funktionen
Lieferschein-Upload: Laden Sie Lieferscheine, Auftragsbestätigung oder Rechnungen im PDF-, Excel- (.xlsx, .xls) oder CSV-Format hoch.

Intelligente Datenextraktion: Nutzt KI (über konfigurierbare APIs) zur Extraktion von EANs, Produktnamen, Mengen und zusätzlichen Details aus hochgeladenen Dokumenten.

EAN-Scan-Funktionalität: Erfassen Sie EANs manuell oder über ein externes Scan-Gerät.

Bestandsabgleich: Verfolgen Sie die gescannten Mengen im Vergleich zu den erwarteten Mengen aus dem Lieferschein. Farbliche Hervorhebung hilft, den Status auf einen Blick zu erkennen (grün für vollständig, orange für überzählt).

Manuelle Mengenanpassung: Erhöhen oder verringern Sie die gescannten Mengen direkt in der Tabelle.

EAN-Bearbeitungsmodus: Korrigieren Sie EANs direkt in der Tabelle, falls ein Fehler vorliegt oder eine Anpassung notwendig ist.

Export-Optionen: Exportieren Sie die gescannten Daten als Excel- oder CSV-Datei.

PWA-Funktionalität: Installierbar auf dem Startbildschirm (Mobilgerät) oder als Desktop-Anwendung (Browser), bietet Offline-Fähigkeiten durch Service Worker und schnelles Laden.

Erste Schritte & Wichtiger Hinweis zur API-Konfiguration
Um UniversalScanner voll nutzen zu können, ist es unerlässlich, eine API für die Datenextraktion in den Einstellungen zu konfigurieren. Die Anwendung verwendet KI, um Informationen aus Ihren hochgeladenen Dokumenten zu parsen.

So konfigurieren Sie die API:
Öffnen Sie die App in Ihrem Webbrowser oder als installierte PWA.

Klicken Sie oben rechts auf den Button "Einstellungen".

Im Einstellungs-Modal wählen Sie unter "API Anbieter auswählen" Ihren bevorzugten Anbieter aus. Empfohlen wird Groq AI für schnelle und kostengünstige (oft sogar kostenlose) Anfragen.

Klicken Sie auf den Registrierungslink, um sich bei dem ausgewählten API-Anbieter zu registrieren und Ihren persönlichen API Key zu erhalten.

Kostenfreie Optionen: Anbieter wie Groq AI bieten oft ein großzügiges kostenloses Kontingent, das für den Anfang und moderate Nutzung ausreichend ist.

Fügen Sie Ihren erhaltenen API Key in das Feld "API Key" ein.

Klicken Sie auf "Speichern".

Nachdem die API erfolgreich konfiguriert wurde, können Sie mit dem Hochladen von Lieferscheinen beginnen und die Extraktionsfunktionen nutzen.

Verwendung
Lieferschein hochladen: Klicken Sie auf "Datei auswählen" und laden Sie Ihr PDF, Excel oder CSV hoch. Die App wird automatisch versuchen, die relevanten Daten zu extrahieren.

EAN scannen: Geben Sie EANs manuell in das Eingabefeld ein und drücken Sie "Scannen" oder verwenden Sie einen externen Barcode-Scanner, der die EAN als Tastatureingabe simuliert.

Mengen anpassen: Verwenden Sie die + und - Buttons in der Spalte "Gescannte EANs", um die Zählungen manuell anzupassen.

EAN bearbeiten: Aktivieren Sie den "EAN bearbeiten"-Modus. Klicken Sie dann auf eine EAN-Zelle in der Tabelle, um sie direkt zu bearbeiten. Bestätigen Sie die Änderung durch Klicken außerhalb der Zelle oder Drücken von Enter.

Daten exportieren: Klicken Sie auf "Als Excel exportieren" oder "Als CSV exportieren", um Ihre gescannten Daten herunterzuladen.

Entwicklung und Installation
Diese PWA kann einfach auf einem Webserver gehostet werden. Für die lokale Entwicklung oder Bereitstellung auf GitHub Pages (wie dieses Repository), sind keine speziellen Backend-Server oder Datenbanken erforderlich, da sie rein statische Dateien nutzt und externe APIs für die KI-Extraktion verwendet.
