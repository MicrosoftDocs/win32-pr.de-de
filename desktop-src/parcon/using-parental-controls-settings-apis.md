---
description: Verwenden von Jugendschutz-Einstellungen APIs
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: Verwenden von Jugendschutz-Einstellungen APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9dd75565559e8fe52413280e35abf076a57ad6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885812"
---
# <a name="using-parental-controls-settings-apis"></a>Verwenden von Jugendschutz-Einstellungen APIs

Einstellungen werden vor der Protokollierung erläutert, da die Protokollierung von den Einstellungen des Benutzers abhängig ist.

## <a name="wmi-api-settings-writeread"></a>WMI-API Einstellungen Schreiben/Lesen

Die WMI-API bietet nicht abstrahierten (unformatierten) Zugriff auf alle Einstellungen, die von der Infrastruktur der Elternsteuerung instanziiert werden, wie in der Schemadatei Wpcsprov.mof definiert. Der Einstellungsspeicher ist im \\ \\ Stammnamespace CIMV2-Anwendungen \\ WindowsParentalControls vorhanden, und die folgenden Klassendefinitionen \\ definieren ein Schema. Erweiterbarkeitselemente werden notiert.

Pro Computer:

-   WpcSystemSettings (eine Instanz)
    -   AddUser()- und RemoveUser()-Methoden zum Erstellen und Löschen von Einstellungen der Jugendschutzsteuerelemente für eine bestimmte SID bzw.
    -   Eigenschaften für das aktuelle Spielbewertungssystem und Nachverfolgung und Benachrichtigung im Zusammenhang mit der Administratorüberprüfung von Protokollen.
    -   Erweiterbarkeit: Eigenschaften für schreibgeschützte und Lese-/Schreib-HTTP-Anwendungs- und URL-Ausnahmelisten für die Webinhaltsfilterung, Überschreibungs-ID und Name des Ressourcen-DLL-Pfads und -ID des Webinhaltsfilters sowie benutzerdefinierte Protokollereignisnummer von Feldern und Headernamenregistrierung.
-   WpcRatingsSystem (eine Instanz pro installierten Bewertungssystem)
    -   WpcRating (eine Instanz pro Bewertungsebene).
    -   WpcRatingDescriptor (eine Instanz pro Bewertungsdeskriptor).
-   Erweiterbarkeit: WpcExtension (eine Instanz pro hinzugefügter Erweiterbarkeitslink des Jugendschutzbereichs).
    -   Eigenschaften für GUID, Subsystem, ID, Ressourcenpfad des Images, Ressourcenpfad des deaktivierten Zustandsbilds, Pfad der ausführbaren Datei, Dll-Pfad und ID der Anzeigenamenressource, Dll-Pfad und ID der Untertitelressource.

Kontrollierter Benutzer:

-   WpcUserSettings (eine Instanz pro kontrolliertem Benutzer)
    -   Eigenschaften für die besitzende SID, das Ein-/Aus-Flag der Eltern, das Ein-/Aus-Flag für die Anmeldung, das Ein-/Aus-Flag, das Flag für aktivierte/deaktivierte Zeitlimits, das Aktiviert-Flag, die Maske für Anmeldestunden und das Flag "Allgemeine Anwendungseinschränkungen ein/aus".
    -   In Windows 8 stellt die vorhandene -Eigenschaft die erste halbe Stunde für jede Stunde dar. Es wurde eine neue Eigenschaft für eine halbe Stunde hinzugefügt, um die zweite Hälfte jeder Stunde zu repräsentieren. Es wurde eine zusätzliche neue Eigenschaft eingeführt, um das Tageszeitrecht zu repräsentieren.

        **Windows 7 und Windows Vista:** Timereinschränkungen unterstützten eine Granularität von einer Stunde.

-   WpcWebSettings (eine Instanz pro kontrolliertem Benutzer)
    -   Eigenschaften für die besitzende SID, filter on/off flag, filter level, file downloads blocked flag, unrated sites blocked flag.
-   WpcUrlOverride (eine Instanz pro URL, die explizit in der URL-Überschreibungsliste zulässig oder verweigert wird, die als Liste "Zulassen/Blockieren" für die Filterung von Webinhalten verwendet wird)
    -   Eigenschaften für besitzende SID, betroffene URL, Status "Zulässig/Blockiert".
-   WpcAppOverride (eine Instanz pro Pfad, die in der Anwendungsüberschreibungsliste "Allgemeine Anwendungseinschränkungen" explizit zulässig ist)
    -   Eigenschaften für die besitzende SID. SAFER-Regel-ID, Pfad zur Anwendung.
-   WpcGamesSettings (eine Instanz pro kontrolliertem Benutzer)
    -   Eigenschaften für die besitzende SID, das Zulässige Flag für Spiele, die GUID des Bewertungssystems für diese Einstellungen, das Flag "Nicht bewertete Spiele zulassen", die ID der maximal zulässigen Bewertung unter dem aktuellen System, die Sammlung abgelehnter Deskriptoren.
-   WpcGameOverride (eine Instanz pro Anwendungs-ID explizit zulässig oder verweigert)
    -   Eigenschaften für die besitzende SID, die Anwendungs-ID, die das Spiel identifiziert, den Status "Zulässig/Verweigert".

## <a name="data-representation-notes"></a>Hinweise zur Datendarstellung

Einige der Einstellungen innerhalb des Schemas werden durch die MOF-Datei mit dem Attribut nicht \_ NULL eingeschränkt. Diese können nicht auf eine NULL-Variante festgelegt werden. Für alle Nicht-Arraytypen initialisiert der Code für die Jugendschutzsteuerung Werte. Bei Arrays können leere Zustände mithilfe einer NULL-Variante, einer leeren Variante oder eines Variantenarrays der Größe 0 (null) geschrieben werden. Der WMI-Anbieter normalisiert alle diese beim Lesen in eine Nullvariante-Zustandsdarstellung.

## <a name="user-interface-extensibility-link-notes"></a>Benutzeroberfläche Extensibility Link Notes (Hinweise zur Erweiterbarkeit)

Die Verwendung von WMI zum Registrieren eines Benutzeroberflächenerweiterungslinks erfordert die Angabe der folgenden Informationen:

-   GUID: Mehrere Links können dieselbe GUID gemeinsam verwenden, wenn sie Teil eines gemeinsamen Pakets oder einer gemeinsamen Suite sind.
-   Subsystem: Dient zum Angeben von Klassifizierungen von Linktypen, z. B. Sammlungen oder eigenständige konforme Anwendungen.
-   Name resource DLL path and ID (Name des Ressourcen-DLL-Pfads und der ID) gibt die Ressource für den Anzeigenamen an, der für den Link angezeigt werden soll.
-   Dll-Pfad und ID der Untertitelressource: Gibt die Ressource für zusätzlichen Text unterhalb des Namens an.
-   Bildpfad – vollständiger Pfad einer 24-bit× 24-Pixel-Bitmap (BMP), mit 8 Bits pro Pixel-Farbtiefe und vorzugsweise einem Alphakanal. Dies wird auf eine Weise angegeben, die mit den Shellerweiterungen konsistent ist: <file system path> , <negative resource ID> . Beispiel: C: Windows \\ \\ System32 \\Wpccpl.dll,-20.
-   Deaktivierter Bildpfad – identisch mit dem obigen Bildpfad, mit Ausnahme einer Variante der Bitmap, die den deaktivierten Zustand zeigt. Diese Abbildung wird angezeigt, wenn die Jugendschutzkontrollen deaktiviert sind.
-   EXE-Pfad: vollständiger Pfad zu einer ausführbaren Datei, die mithilfe von ShellExecute() aufgerufen werden soll. Dieser Pfad muss mit schrägen Schrägstrichen angegeben werden, da der Link die ausführbare Datei nicht aufruft. Das Hinzufügen eines %SID%-Tokens nach dem EXE-Pfad führt dazu, dass die Linkausführung die SID-Zeichenfolge für den Benutzer abgibt, für den die Hubseite gerade angezeigt wird. Die ausführbare Datei kann dann die SID-Zeichenfolge verwenden, um die Funktionalität für den angegebenen Benutzer zu verwalten.

Bei der Deinstallation der Anwendung muss eine Erweiterbarkeitslinkregistrierung entfernt werden.

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Hinweise zur Außerkraftsetzung von Weberweiterbarkeitslinks und Webinhaltsfiltern

Durch Festlegen der FilterID-Eigenschaft auf die gleiche GUID wie bei einem vorhandenen Link zur Erweiterbarkeit der registrierten Benutzeroberfläche wird der angezeigte Link von einem generischen Link in Andere Einstellungen zum exklusiven Link Webeinschränkungen. Dies ist eine computerweite Einstellung, die dazu führen wird, dass der In-Box-Webinhaltsfilter-LSP alle Filter für alle kontrollierten Benutzer umgeht. Ein beschreibender Name sollte auch in der FilterName-Eigenschaft festgelegt werden, die durch einen Pfad zu Ressourcen-DLL und -ID angegeben wird.

Das System für die Jugendschutzkontrollen empfiehlt Folgendes aus allen überschreibenden Webfiltern:

-   Honor the overall Parental Controls on/off state for a user.
-   Honor the Aktivitätsberichterstattung settings for a user.
-   Überwachen Sie die FilterID-Eigenschaft. Wenn sie sich von der vom Anbieter angegebenen GUID ändert, hat ein anderer Filter den Besitz übernommen, und der Filter des Anbieters sollte sich selbst deaktivieren. Es wurde eine COM-Schnittstelle hinzugefügt, um den Mehraufwand der regelmäßigen Überprüfung auf diese Änderung im Vergleich zu einem WMI-Aufruf zu reduzieren.
-   Es wird dringend empfohlen, sowohl schreibgeschützte als auch Lese-/Schreib-HTTP-Anwendungs- und URL-Ausnahmelisteneinträge zu verwenden.
-   Es wird empfohlen, die Überschreibungsliste pro Benutzer-URL (Liste zulassen/blockieren) zu verwenden.
-   Seien Sie robust, um schnelle Benutzerwechsel zu machen.

Die Steuerung der Eltern spricht keine Einschränkungen dafür aus, wie ein Web- oder anderer Inhaltsfilter Windows Filterung einfährt. Anbieter können ihre aktuellen Investitionen oder bevorzugten Technologien (LSP, TDI, andere) nutzen.

Die Deinstallation des Herstellerfilters muss die Registrierung der Einträge FilterID und FilterName aufheben. Dies erfolgt, indem FilterID auf GUID \_ NULL und FilterName auf eine Variante NULL festgelegt wird. Der In-Box-Webinhaltsfilter wird dann erneut aktiviert.

Beachten Sie, dass beim erneuten Aktivieren des In-Box-Webfilters nur neue Sitzungen gefiltert werden, nicht jedoch Sitzungen, die vor dem Switch aktiv sind.

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Webinhaltsfilter : Export-/Importformat für Listen zulassen/blockieren

Dieses Feature wird in der Windows 8.

**Windows 7 und Windows Vista:** Dieses Feature wird unterstützt.

&lt;WebAddresses&gt;

<URL AllowBlock="1">https://alloweddomain.com/&lt;/URL&gt;

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html&lt;/URL&gt;

<URL AllowBlock="2">https://blockeddomain.com/&lt;/URL&gt;

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html&lt;/URL&gt;

&lt;/WebAddresses&gt;

## <a name="application-restrictions-override-notes"></a>Hinweise zur Außerkraftsetzung von Anwendungseinschränkungen

Außerkraftsetzungen von Anwendungseinschränkungen werden pro Benutzer festgelegt, um bestimmte Binärdateien oder Pfade zu ermöglichen. Wenn ein neuer jugendgesteuerter Benutzer konfiguriert ist und anwendungseinschränkungsüberschreibungen für diesen Benutzer erforderlich sind, wird empfohlen, den Windows-Ausführungsschlüssel in der Registrierung mit einer kleinen Anwendung zu verwenden, die als erforderlich gekennzeichnet ist, dass die Rechteerweiterung zum Schreiben der Außerkraftsetzungen erforderlich ist. Dies führt zu einer einmaligen Aufforderung zur Eingabe von Anmeldeinformationen, um die Außerkraftsetzungen für den Benutzer zu konfigurieren. Danach stellen die Zielbinärdateien für die Außerkraftsetzungen keine Lässigung für Benutzer aufgrund weiterer Aufforderungen zur Außerkraftsetzung durch administratoren.

## <a name="actions-required-for-settings-changes-to-become-effective"></a>Erforderliche Aktionen, damit Einstellungen wirksam werden

Wenn ein Administrator die Einstellungen für einen angemeldeten Standardbenutzer ändert, wird eine Warnmeldung generiert. Sie gibt an, dass die Einstellungsänderungen möglicherweise erst wirksam werden, wenn sich der gesteuerte Benutzer ab- und wieder anmeldet. Dies ist ein konservativer Entwurf. Die meisten Einstellungen werden fast sofort wirksam, während der kontrollierte Benutzer angemeldet ist. Eine Ausnahme sind Spiele, bei denen Die Einstellungen bei der nächsten Ausführung des Spiele-Explorers oder beim Aufrufen des Spiels wirksam werden.

## <a name="sample-code"></a>Beispielcode

C++-Beispiele werden im SDK bereitgestellt, um die Verwendung der Erweiterbarkeitsfeatures für Einstellungen zu demonstrieren. Weitere Informationen finden Sie im Abschnitt Beispiele für Jugendschutz.

## <a name="independent-test-tools"></a>Unabhängige Test Tools

Die Überprüfung von Klassen und Instanzen wird durch das Wmimgmt.msc-Plug-In und das Wbemtest.exe-Tool ermöglicht.

## <a name="64-bit-considerations"></a>64-Bit-Überlegungen

In 64-Bit-Windows Betriebssystemversionen ist derzeit sowohl ein 32-Bit-WMI-Anbieter als auch ein 64-Bit-Anbieter installiert.

## <a name="general-code-development-and-debugging"></a>Allgemeine Codeentwicklung und Debuggen

Wenn Visual Studio für die Codeentwicklung der Einstellungsverwaltung verwendet wird, erfordert das lokale Debuggen die Ausführung von Visual Studio mit Administratorrechten (aufrufen mit Als Administrator ausführen über die Befehlszeile oder mit der Rechtsklickoption). Dies liegt an der Prozess- und Nachrichtenisolation, die von der UAC implementiert wird.

## <a name="minimum-compliance-api-settings-read"></a>Minimum Compliance API Einstellungen Read

### <a name="interfaces-and-methods"></a>Schnittstellen und Methoden

Die von der Headerdatei Wpcapi.h gesteuerte Kompatibilitäts-API ermöglicht den vereinfachten schreibgeschützten Zugriff auf die folgenden Einstellungen mithilfe von COM-Schnittstellen.

[**IWindowsParentalControls-Stammschnittstellenmethoden**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) bieten Zugriff auf:

-   IWPCSettings-Methoden:
    -   IsLoggingRequired(): Ist die Aktivitätsberichterstellung für den Benutzer als ein konfiguriert?
    -   GetLastSettingsChangeTime(): Die Anwendung kann beachten, ob seit einer vorherigen Überprüfung Einstellungsrichtlinien geändert wurden.
    -   GetRestrictions(): Lesen Sie, ob Webeinschränkungen, Zeitlimits, Spieleinschränkungen oder Anwendungseinschränkungen auf on festgelegt sind.
-   IWPCWebSettings-Methoden:
    -   GetSettings(): Ruft Flags für filter on oder off ab und lädt blockiert.
    -   RequestURLOverride(): Geben Sie eine Anforderung in den Administratorüberschreibungsmechanismus (over-the-shoulder approval) ein, der ein Dialogfeld mit den zu genehmigenden URLs enthält.
-   IWPCGamesSettings-Methoden:
    -   IsBlocked(): Für eine bestimmte Spielanwendungs-ID ist das Spiel, das von den Jugendschutzmaßnahmen blockiert wird und aus welchem Grund.
-   GetVisibility(): Enthält Informationen dazu, ob die Benutzeroberfläche der Jugendschutzelemente derzeit ausgeblendet ist.
-   GetWebFilterInfo(): Stellt eine Schnittstelle zum Abrufen der ID des derzeit aktiven Webinhaltsfilters bereit.

### <a name="sample-code"></a>Beispielcode

C++-Beispiele werden im SDK bereitgestellt, um die Verwendung der Compliance-API zu veranschaulichen. Weitere Informationen finden Sie im Abschnitt Beispiele für die Jugendschutzmaßnahmen.

 

 



