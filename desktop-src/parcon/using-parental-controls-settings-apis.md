---
description: Verwenden von Einstellungen für die Jugend Steuerungseinstellungen
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: Verwenden von Einstellungen für die Jugend Steuerungseinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dde4827dfe3ed5ee7eec6787744e6ff92f18775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757753"
---
# <a name="using-parental-controls-settings-apis"></a>Verwenden von Einstellungen für die Jugend Steuerungseinstellungen

Die Einstellungen werden vor der Protokollierung erläutert, da die Protokollierung für die Benutzereinstellungen bedingt ist.

## <a name="wmi-api-settings-writeread"></a>WMI-API-Einstellungen schreiben/lesen

Die WMI-API bietet einen nicht abstrahierten (unformatierten) Zugriff auf alle Einstellungen, die von der Infrastruktur der Jugendschutz Infrastruktur instanziiert werden, wie in der Schema Datei "wpcsprov. mof" definiert. Der Einstellungs Speicher \\ \\ ist im \\ \\ windowsparentalcontrols-Namespace der root cimv2 Applications vorhanden, wobei die folgenden Klassendefinitionen ein Schema definieren. Erweiterbarkeits Elemente werden vermerkt.

Pro Computer:

-   Wpcsystemsettings (eine Instanz)
    -   Die Methoden "adduser ()" und "RemoveUser ()" zum Erstellen und Löschen von Einstellungen für Eltern Steuerelemente für eine bestimmte sid.
    -   Eigenschaften für das aktuelle Spiel Bewertungssystem in Kraft und Überwachung und Benachrichtigung im Zusammenhang mit der Administrator Überprüfung von Protokollen.
    -   Erweiterbarkeit: Eigenschaften für Lese-und Lese-/Schreibzugriff auf http-Anwendungs-und URL-Ausnahme Listen für das Filtern von Webinhalten, den Webinhalts Filter Überschreibungs-ID und die ID-Pfad und-ID des Namens Ressourcen sowie die Anzahl von Feldern und die Registrierung von Header Namen.
-   Wpcratingssystem (eine Instanz pro installiertem Bewertungssystem)
    -   Wpcrating (eine Instanz pro Bewertungsstufe).
    -   Wpcratingdescriptor (eine Instanz pro Bewertungs Deskriptor).
-   Erweiterbarkeit: wpcextension (eine Instanz pro Steuerelement-Erweiterbarkeits Verknüpfung, die hinzugefügt wurde).
    -   Eigenschaften für "GUID", "Subsystem", "ID", "Image-Ressourcen Pfad", "deaktivierte Zustands Image-Ressourcen Pfad", "Pfad der ausführbaren Datei", "Name der Ressourcen-DLL-Pfad

Pro-gesteuerter Benutzer:

-   Wpcusersettings (eine Instanz pro kontrolliertem Benutzer)
    -   Eigenschaften für die besitzende sid, das on/off-Flag für elterliche Steuerelemente, das Flag zum Anmelden/Abmelden, das Aktivieren/Deaktivieren von Flag, das Flag für aktivierte außer Kraft setzungen, die Anmelde Stunden Maske und allgemeine Anwendungs Einschränkungen für ein/aus.
    -   In Windows 8 stellt die vorhandene Eigenschaft die erste halbe Stunde für jede Stunde dar. Es wurde eine neue halbstündige Eigenschaft hinzugefügt, die die zweite Hälfte der einzelnen Stunden darstellt. Eine zusätzliche neue Eigenschaft wurde eingeführt, um das tägliche Zeitkontingent darzustellen.

        **Windows 7 und Windows Vista:** Zeit Geber Einschränkungen unterstützten eine Granularität von 1 Stunde.

-   Wpcwebsettings (eine Instanz pro kontrolliertem Benutzer)
    -   Eigenschaften für die besitzende sid, das Flag zum Filtern ein/aus, die Filter Ebene, das blockierte Flag für Dateidownloads und das Flag für nicht bewertete Sites.
-   Wpcurrloverride (eine Instanz pro URL wurde in der URL-Außerkraftsetzungs Liste explizit zugelassen oder verweigert, die als Zulassungs-/Blockierungs Liste für das Filtern von Inhalten verwendet wird
    -   Eigenschaften für besitzende sid, URL betroffen, zulässiger/blockierter Zustand.
-   Wpcappoverride (eine Instanz pro Pfad ist explizit in der Anwendungs Einschränkungs Liste der Anwendungs Einschränkungen zulässig)
    -   Eigenschaften für die besitzende sid. Sicherere Regel-ID, Pfad zur Anwendung.
-   Wpcgamessettings (eine Instanz pro kontrolliertem Benutzer)
    -   Eigenschaften für die besitzende sid, die Anzahl zulässiger Spiele, die GUID des Bewertungssystems für diese Einstellungen, das Flag für nicht bewertete Spiele zulassen, die ID der maximal zulässigen Bewertung unter dem aktuellen System, die Sammlung der verweigerten Deskriptoren.
-   Wpcgameoverride (eine Instanz pro Anwendungs-ID explizit zugelassen oder verweigert)
    -   Eigenschaften für die besitzende sid, die Anwendungs-ID, das das Spiel identifiziert hat

## <a name="data-representation-notes"></a>Hinweise zur Datendarstellung

Einige der Einstellungen innerhalb des Schemas werden durch die MOF-Datei mit einem nicht-NULL-Attribut eingeschränkt \_ . Diese können nicht auf eine NULL-Variante festgelegt werden. Bei allen nicht-Array-Typen initialisiert der Jugendschutz Code-Werte. Für Arrays können leere Zustände mit einem NULL-Variant, einem leeren Variant oder einem Variant-Array der Größen NULL geschrieben werden. Der WMI-Anbieter normalisiert alle diese auf eine NULL Variant-Statusdarstellung beim Lesen.

## <a name="user-interface-extensibility-link-notes"></a>Hinweise zur Erweiterbarkeit der Benutzeroberfläche

Die Verwendung von WMI zum Registrieren eines UI-Erweiterbarkeits Links erfordert die Angabe der folgenden Informationen:

-   GUID: mehrere Links können dieselbe GUID verwenden, wenn Sie Teil eines gemeinsamen Pakets oder einer gemeinsamen Sammlung sind.
-   Subsystem: dient zum Angeben von Klassifizierungen von Linktypen, z. b. Suites oder eigenständigen kompatiblen Anwendungen.
-   Name Ressourcen-DLL-Pfad und-ID: gibt die Ressource für den anzeigen Amen an, der für den Link angezeigt werden soll.
-   Untertitel Ressourcen-DLL-Pfad und-ID: gibt die Ressource für zusätzlichen Text unterhalb des Namens an.
-   Image Pfad: vollständiger Pfad einer 24 × 24 Pixel Bitmap (BMP) mit einer Farbtiefe von 8 Bits pro Pixel und vorzugsweise einem Alphakanal. Diese Angabe wird in Übereinstimmung mit den Shellerweiterungen angegeben: <file system path> , <negative resource ID> . Beispiel: C: \\ Windows \\ system32 \\Wpccpl.dll,-20.
-   Deaktivierter Bildpfad-identisch mit dem obigen Bildpfad, außer Variant of Bitmap, die den deaktivierten Zustand anzeigt. Dieses Bild wird angezeigt, wenn die Eltern Steuerelemente deaktiviert sind.
-   Exe-Pfad: vollständiger Pfad zu einer ausführbaren Datei, die mit ShellExecute () aufgerufen werden soll. Dieser Pfad muss mit umgekehrten Schrägstrichen angegeben werden, oder der Link Ruft die ausführbare Datei nicht auf. Das Hinzufügen eines% sid%-Tokens nach dem Pfad der exe-Datei führt dazu, dass die Link Ausführung durch die SID-Zeichenfolge für den Benutzer ersetzt wird, für den die Hub-Seite derzeit angezeigt wird. Die ausführbare Datei kann dann die SID-Zeichenfolge verwenden, um die Funktionalität für den angegebenen Benutzer zu verwalten.

Beim Deinstallieren von Anwendungen muss eine Erweiterbarkeits Link Registrierung entfernt werden.

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Hinweise zur weberweiterbarkeit und zum Überschreiben von Webinhalts Filtern

Durch Festlegen der filterid-Eigenschaft auf die gleiche GUID wie ein vorhandener registrierter Benutzeroberflächen-Erweiterbarkeits Link wird der angezeigte Link von einem generischen Link in anderen Einstellungen auf den Link für exklusive Webeinschränkungen herauf gestuft. Dabei handelt es sich um eine Computer weite Einstellung, die bewirkt, dass der in-Box-Filter LSP alle Filter für alle kontrollierten Benutzer umgeht. Ein beschreibender Name sollte auch in der Filter Name-Eigenschaft festgelegt werden, die durch einen Pfad zur Ressourcen-DLL und ID angegeben wird.

Das Eltern Steuerungssystem empfiehlt Folgendes von jedem über schreibenden Webfilter:

-   Beachten Sie, dass der Status der übergeordneten Steuerelemente für einen Benutzer ein/aus ist.
-   Beachten Sie die Aktivitäts Berichterstattungs Einstellungen für einen Benutzer.
-   Überwachen Sie die filterid-Eigenschaft. Wenn er sich von der angegebenen GUID des Anbieters ändert, hat ein anderer Filter den Besitz übernommen, und der Filter des Herstellers sollte sich selbst deaktivieren. Es wurde eine COM-Schnittstelle hinzugefügt, um den mehr Aufwand bei der regelmäßigen Überprüfung für diese Änderung im Vergleich zu einem WMI-
-   Es wird dringend empfohlen, sowohl die schreibgeschützte http-Anwendung als auch die Lese-/Schreib-Zugriffsliste zu berücksichtigen.
-   Empfohlen, die URL-außer Kraft setzung der benutzerspezifischen URL (Zulassungs-/Blockierungs Liste) zu berücksichtigen.
-   Seien Sie robust für die schnelle Benutzerumschaltung.

Bei der Jugendschutz Kontrolle gelten keine Einschränkungen für die Art und Weise, wie ein Web-oder anderer Inhaltsfilter zum Implementieren von Filtern an Windows angeschlossen ist. Anbieter können Ihre aktuellen Investitionen oder bevorzugten Technologien (LSP, TDI, andere) nutzen.

Bei der Deinstallation des Filters des Anbieters muss die Registrierung der Filter ID-und Filter Name-Einträge aufgehoben werden. Dies erfolgt durch Festlegen von filterid auf GUID \_ null und Filter Name auf eine Variante NULL. Der in-Box-Webinhalts Filter wird dann erneut aktiviert.

Beachten Sie, dass bei der erneuten Aktivierung des in-Box-Webfilters nur neue Sitzungen gefiltert werden, und nicht die Sitzungen, die vor dem Wechsel aktiv sind.

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Export/Import-Format für Webinhalts Filter zulassen/blockieren

Diese Funktion wird unter Windows 8 nicht unterstützt.

**Windows 7 und Windows Vista:** Diese Funktion wird unterstützt.

<WebAddresses>

<URL AllowBlock="1">https://alloweddomain.com/</URL>

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html</URL>

<URL AllowBlock="2">https://blockeddomain.com/</URL>

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html</URL>

</WebAddresses>

## <a name="application-restrictions-override-notes"></a>Hinweise zur Anwendungs Einschränkung außer Kraft setzen

Anwendungs Einschränkungs Überschreibungen werden pro Benutzer festgelegt, um bestimmte Binärdateien oder Pfade zuzulassen. Wenn ein neuer, von einem Administrator kontrollierter Benutzer konfiguriert ist und Anwendungs Einschränkungen außer Kraft setzungen für diesen Benutzer erforderlich sind, wird empfohlen, dass der Windows-Lauf Schlüssel in der Registrierung für eine kleine Anwendung verwendet wird, die für das Schreiben der außer Kraft setzungen bereitgestellt wird. Dies führt zu einer Eingabeaufforderung für einmalige Anmelde Informationen, um die außer Kraft setzungen für den Benutzer zu konfigurieren. Anschließend werden die Ziel Binärdateien für die außer Kraft setzungen für Benutzer aufgrund weiterer Administrator Überschreibungs Aufforderungen nicht als lästig festgesetzt.

## <a name="actions-required-for-settings-changes-to-become-effective"></a>Erforderliche Aktionen für Einstellungsänderungen, damit Sie wirksam werden

Wenn ein Administrator die Einstellungen für einen angemeldeten Standardbenutzer ändert, wird eine Warnmeldung generiert. Es gibt an, dass die Einstellungsänderungen möglicherweise erst wirksam werden, wenn sich der kontrollierte Benutzer erneut anmeldet und wieder anmeldet. Dies ist ein konservatives Design. Die meisten Einstellungen werden fast sofort wirksam, während der kontrollierte Benutzer angemeldet ist. Eine Ausnahme ist für Spiele, bei denen Einstellungen wirksam werden, wenn der Spiele-Explorer das nächste Mal ausgeführt wird oder das Spiel aufgerufen wird.

## <a name="sample-code"></a>Beispielcode

Im SDK werden C++-Beispiele bereitgestellt, die die Verwendung der Erweiterbarkeits Features der Einstellungen veranschaulichen. Weitere Informationen finden Sie im Abschnitt "Jugend Steuerungs Beispiele".

## <a name="independent-test-tools"></a>Unabhängige TestTools

Die Überprüfung von Klassen und Instanzen wird durch das wmimgmt. msc-Plug-in und das Wbemtest.exe Tool ermöglicht.

## <a name="64-bit-considerations"></a>64-Bit-Überlegungen

64-Bit-Windows-Betriebssystemversionen haben derzeit sowohl einen 32-Bit-WMI-Anbieter als auch einen 64-Bit-Anbieter installiert.

## <a name="general-code-development-and-debugging"></a>Allgemeine Code Entwicklung und-Debuggen

Wenn Visual Studio für die Entwicklung von Einstellungen für die Code Entwicklung verwendet wird, erfordert das lokale Debuggen das Ausführen von Visual Studio mit Administratorrechten (Aufrufen mit "Ausführen als Administrator" mithilfe der Befehlszeile oder mit der rechten Maustaste). Dies liegt an der von UAC implementierten Prozess-und Nachrichten Isolation.

## <a name="minimum-compliance-api-settings-read"></a>Minimale Konformität-API-Einstellungen lesen

### <a name="interfaces-and-methods"></a>Schnittstellen und Methoden

Die von der Header Datei "wpcapi. h" gesteuerte Kompatibilitäts-API bietet vereinfachten schreibgeschützten Zugriff auf die folgenden Einstellungen mithilfe von COM-Schnittstellen.

[**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) -Stamm Schnittstellen Methoden ermöglichen den Zugriff auf:

-   Iwpcsettings-Methoden:
    -   Isloggingrequired () – ist die Aktivitäts Berichterstattung, die für den Benutzer als on konfiguriert ist?
    -   Getlastsettingschangetime () – die Anwendung kann erkennen, ob sich die Einstellungs Richtlinien seit einer vorherigen Überprüfung geändert haben.
    -   Getrestrictions () – lesen Sie, ob Webeinschränkungen, Zeitlimits, Spiel Einschränkungen oder Anwendungs Einschränkungen auf ON festgelegt sind.
-   Iwpcwebsettings-Methoden:
    -   GetSettings () – Hiermit werden Flags für Filter ein-oder ausgeschaltet und Downloads blockiert.
    -   Requesturloverride () – gibt eine Anforderung in den Administrator Überschreibungs Mechanismus (over-the-Shoulder Approval) ein, der ein Dialogfeld mit den zu genehmigenden URLs enthält.
-   Iwpcgamessettings-Methoden:
    -   Isblockierte () – für eine bestimmte Game-Anwendungs-ID wird das Spiel von Eltern Steuerelementen blockiert und aus welchem Grund.
-   Getvisibility () – enthält Informationen dazu, ob die Benutzeroberfläche für die Jugend Steuerungselemente zurzeit ausgeblendet ist.
-   Getwebfilterinfo () – stellt eine Schnittstelle zum Abrufen der ID des aktuell aktiven Webinhalts Filters bereit.

### <a name="sample-code"></a>Beispielcode

C++-Beispiele werden im SDK bereitgestellt, um die Verwendung der Kompatibilitäts-API zu demonstrieren. Weitere Informationen finden Sie im Abschnitt "Jugend Steuerungs Beispiele".

 

 



