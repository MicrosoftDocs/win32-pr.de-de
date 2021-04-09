---
description: Windows-Explorer steuert die Erstellung eines Suchconnector für einen Protokollhandler über Registrierungsschlüssel Einträge. Durch die Registrierung können sowohl Implementierer als auch Drittanbieter neue und ältere Protokollhandler für die Teilnahme an der Windows 7-Suche aktivieren.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Erstellen eines Suchconnector für einen Protokoll Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128597"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a>Erstellen eines Suchconnector für einen Protokoll Handler

Windows-Explorer steuert die Erstellung eines Suchconnector für einen Protokollhandler über Registrierungsschlüssel Einträge. Durch die Registrierung können sowohl Implementierer als auch Drittanbieter neue und ältere Protokollhandler für die Teilnahme an der Windows 7-Suche aktivieren.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu Suchconnectors für Protokollhandler in Windows 7](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [Aktivieren von Protokoll Handlern für die Teilnahme an der Suche](#enabling-protocol-handlers-to-participate-in-search)
    -   [Der Suchconnector für die Protokoll Handler-Suche wird deaktiviert.](#disabling-protocol-handler-search-connector-creation)
    -   [Anpassen des Namens, der Beschreibung oder des foldertype für einen protokollhandlersuchconnector](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [Verwenden von Registrierungs Zeichenfolgen](#using-registry-string-redirection)
    -   [Wiederherstellen eines gelöschten Suchconnector für Protokoll Handler](#restoring-a-deleted-protocol-handler-search-connector)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a>Informationen zu Suchconnectors für Protokollhandler in Windows 7

In Windows 7 enthalten Suchvorgänge im **Startmenü** oder im Windows-Explorer nur Dateien an indizierten Speicherorten und nicht Dateisystem Elemente, wie z. b. Remote Datenspeicher oder protokollhandlerelemente, die über einen Suchconnector verfügen. Der Suchconnector ermöglicht nicht nur die protokollhandlerelemente im Bereich von **Startmenü** und shellsuchvorgängen, sondern auch das **Startmenü** , um protokollhandlerelemente in den Ergebnissen des **Start** Menüs zu gruppieren. Dies hat den Vorteil, dass der Benutzer auf den Gruppen Header klicken und Ergebnisse nur aus dem Protokollhandler anzeigen kann. Alternativ kann der Benutzer zum Ordner **Suchen** navigieren, die Suchconnector-Datei öffnen und eine Suche durchführen, die nur Elemente aus dem spezifischen Protokollhandler enthält, der diesem Suchconnector zugeordnet ist.

Wenn ein Benutzer eine Anwendung startet, die einen Protokollhandler registriert, generiert Windows Explorer eine Suchconnector-Datei (. searchconnector-MS) für den Protokollhandler im Ordner " **Such** Vorgänge" des Benutzers. Anwendungen mit Protokoll Handlern können dieses Verhalten deaktivieren oder den Namen und die Beschreibung des suchverbindungs-Connector für den Protokollhandler anpassen.

> [!Note]  
> Der Speicherort des **Such** Ordners des Benutzers lautet "% User Profile% \\ Suchen" oder "folderid \_ savedsuchen". Die GUID für folderid \_ savedsuchen ist {7d1d3a04-Debb-4115-95cf-2f29da2920da}.

 

Windows-Explorer steuert die Erstellung eines Suchconnector für einen Protokollhandler über Registrierungsschlüssel Einträge, die in den folgenden Abschnitten beschrieben werden:

-   [Aktivieren von Protokoll Handlern für die Teilnahme an der Suche](#enabling-protocol-handlers-to-participate-in-search)
-   [Der Suchconnector für die Protokoll Handler-Suche wird deaktiviert.](#disabling-protocol-handler-search-connector-creation)
-   [Anpassen des Namens, der Beschreibung oder des foldertype für einen protokollhandlersuchconnector](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [Wiederherstellen eines gelöschten Suchconnector für Protokoll Handler](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> Es gibt keine programmatischen Möglichkeiten, einen Suchconnector für einen Protokollhandler zu erstellen. Sie müssen über die Registrierung konfiguriert werden.

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a>Aktivieren von Protokoll Handlern für die Teilnahme an der Suche

Die Registrierungsschlüssel und die möglichen Werte sind in der folgenden Tabelle aufgeführt. Ein Protokollhandler kann einige oder alle dieser Registrierungsschlüssel auffüllen, wobei Beispiels <protocol> Weise durch den tatsächlichen Namen des Protokolls ersetzt wird, z. b. MAPI, File oder csc.



| Registrierungsschlüssel                                                                                                                 | Mögliche Werte                                                                                                                     | Typ       | Kommentare                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ phsearchconnectors- \\ <protocol> \\ Version                     | Ist nicht vorhanden (Standard). Andernfalls ist Sie 1 oder größer.                                                                               | REG \_ DWORD | Dieser Wert wird verwendet, um Änderungen an den Speicherort Vorlagen Registrierungen für Such Stämme zu erkennen, die bereits verarbeitet wurden. Wenn nicht vorhanden ist, verwenden Sie 0 als Standardwert. Sie können auch die Version erhöhen, um Windows-Explorer darüber zu informieren, dass der Suchconnector neu generiert werden soll, weil eine neuere Version des Protokoll Handlers installiert wurde. |
| HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ phsearchconnectors \\ <protocol> \\ donotkreatesearchconnectors | Ist nicht vorhanden (Standard). Andernfalls auf 1 festgelegt.                                                                                         | REG \_ DWORD | Wenn Sie nicht vorhanden ist, erstellen Sie eine searchconnector-MS-Datei im Ordner "Suchvorgänge". Wenn 1, markieren Sie als verarbeitet, und führen Sie nichts aus.                                                                                                                                                                                                                                   |
| HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ \\ <protocol> \\ Standard \\ Beschreibung von "phsearchconnectors"        | Eine lokalisierbare Zeichenfolge, die die Beschreibung des Suchconnector enthält.                                                              | REG- \_ SZ    | Dies ist optional. Sie wird im Description-Element der. searchconnector-MS-Datei verwendet.                                                                                                                                                                                                                                                                          |
| HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ \\ <protocol> \\ Standard Name für Standard \\ Name               | Eine lokalisierte Zeichenfolge, um den Suchconnector zu benennen. Wird als Name der. searchconnector-MS-Datei verwendet.                                    | REG- \_ SZ    | Jeder Speicherort muss einen eindeutigen Namen aufweisen. Wenn dieser Wert nicht vorhanden ist, wird der von der [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Protokoll Handlers bereitgestellte Anzeige Name verwendet.                                                                                                                             |
| HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ \\ <protocol> \\ Standard \\ foldertype         | Eine GUID, die die [foldertypeid](../shell/foldertypeid.md) identifiziert, die auf den Suchconnector angewendet werden soll. | REG- \_ SZ    | Dies ist optional. Wird im foldertype-Element der. searchconnector-MS-Datei verwendet, um anzugeben, welche Vorlagen zum Anzeigen von Ergebnissen verwendet werden sollen. Beispielsweise der GUID-Wert von foldertypeid- \_ Dokumenten.                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a>Der Suchconnector für die Protokoll Handler-Suche wird deaktiviert.

Wenn Ihre Anwendung Elemente über einen Protokollhandler zur Verwendung in der Anwendung selbst verfügbar macht und Sie die Elemente nicht über die Shell (im **Startmenü** und in Windows Explorer-suchen) verfügbar machen möchten, müssen Sie die Erstellung eines Suchconnector für Ihren Protokollhandler deaktivieren.

Wenn Sie die suchconnectorerstellung deaktivieren möchten, legen Sie donotkreatesearchconnectors auf 0x00000001 (1) fest, wie im folgenden Beispiel für den Registrierungsschlüssel gezeigt.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

Wenn donotkreatesearchconnectors auf 1 festgelegt ist, wird empfohlen, die [System. Shell. omitfromview](/windows/desktop/properties/props-system-shell-omitfromview) -Eigenschaft für jedes Element verfügbar zu machen, das vom Protokollhandler verfügbar gemacht wird, und den Wert dieser Eigenschaft auf **true** festzulegen. Dadurch wird verhindert, dass die protokollhandlerelemente unter der **Datei** Gruppe " **Startmenü** " angezeigt werden.

Wenn donotkreatesearchconnectors vorhanden und auf 0 (null) festgelegt ist, erstellt Windows-Explorer einen Suchconnector für den Protokollhandler, und die protokollhandlerelemente werden im **Startmenü** und in Windows Explorer-suchen zurückgegeben.

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a>Anpassen des Namens, der Beschreibung oder des foldertype für einen protokollhandlersuchconnector

Der suchconnectorname wird nicht nur verwendet, um den Suchconnector im **Suchordner zu** identifizieren, sondern als Gruppen Kopfzeile für die Ergebnisse im **Startmenü** . Daher ist es wichtig, einen beschreibenden Namen für den Suchconnector bereitzustellen. Wenn im Registrierungsschlüssel kein Name angegeben ist, verwendet Windows Explorer standardmäßig den von der [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) bereitgestellten Namen für den Such Stamm des Protokoll Handlers und die leere Beschreibung. Sie können den Standardnamen über einen Registrierungsschlüssel Eintrag überschreiben, ohne die IShellFolder-Schnittstelle Umbenennen zu müssen. Obwohl Sie nicht so sichtbar wie der Suchconnector-Name ist, können Sie die Beschreibung für den Suchconnector auch überschreiben, indem Sie eine eigene Beschreibung angeben.

Wenn Sie den Standardnamen oder die Beschreibung überschreiben möchten, legen Sie die Einträge wie im folgenden Registrierungs Beispiel dargestellt fest.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

Außerdem kann der foldertype-Eintrag auf eine der [foldertypeid](../shell/foldertypeid.md) -GUIDs festgelegt werden. Der Wert muss die tatsächliche GUID und nicht sein Name sein. Beispiel: {94d6ddcc-4a68-4175-A374-bd584a510 B78} anstelle von foldertypeid \_ Music. Die GUID für eine foldertypeid kann in der Header Datei "shlguid. h" im [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)abgerufen werden.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a>Verwenden von Registrierungs Zeichenfolgen

Sie können eine [umgeleitete Zeichenfolge](../intl/using-registry-string-redirection.md) verwenden, um sicherzustellen, dass der von Ihnen für den Suchconnector bereitgestellte Name lokalisiert werden kann. Sie können lokalisierbare Zeichen folgen für die Registrierungsschlüssel Name und Beschreibung einschließen, anstatt die tatsächliche Zeichenfolge in die Registrierung einzugeben.

Wenn Sie eine lokalisierbare Zeichenfolge für den Namen oder die Beschreibungs Werte einschließen möchten, legen Sie den Wert wie im folgenden Beispiel für den Registrierungsschlüssel gezeigt fest

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

Die lokalisierbare Zeichenfolge hat das folgende Format:

-   @dllname.dll,-ResourceID, wobei:
    -   @dllname.dll der Pfad zu der dll, die die Zeichen folgen Ressource enthält.
    -   ResourceId ist die ganzzahlige Ressourcen-ID der Zeichen folgen Ressource.

Das Format für eine indirekte Zeichenfolge und eine indirekte Zeichenfolge, die mit einem versionsmodifizierer angehängt wird, werden in der [shloadderetstring-Funktion](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)beschrieben.

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a>Wiederherstellen eines gelöschten Suchconnector für Protokoll Handler

Da Suchconnectors Dateien auf dem Computer des Benutzers sind, können Sie versehentlich gelöscht werden. Um alle gelöschten Suchconnectors für Protokollhandler wiederherzustellen, stellen Sie die Standardbibliotheken wieder her. Öffnen Sie hierzu Windows-Explorer, klicken Sie mit der rechten Maustaste auf den Ordner **Bibliotheken** , und wählen Sie dann **Standardbibliotheken wiederherstellen** aus.

![Screenshot mit der Menüoption "Standardbibliotheken wiederherstellen"](images/libraries.png)

## <a name="additional-resources"></a>Weitere Ressourcen

-   [IShellItem:: GetDisplayName](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [Signatur- \_ Normal Anzeige](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Grundlegendes zu Protokoll Handlern](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Hinzufügen von Symbolen und Kontextmenüs](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Code Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokoll Handlern](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Debuggen von Protokoll Handlern](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
