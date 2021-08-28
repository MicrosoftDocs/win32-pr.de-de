---
description: Windows Der Explorer steuert die Erstellung eines Suchconnectors für einen Protokollhandler über Registrierungsschlüsseleinträge. Über die Registrierung können sowohl Implementierer als auch Drittanbieter neue und ältere Protokollhandler für die Teilnahme an der Windows 7-Suche aktivieren.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Erstellen eines Suchconnectors für einen Protokollhandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec9c7830f61c0dcbf6682e6dfaea0feb30ebfa5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881682"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a>Erstellen eines Suchconnectors für einen Protokollhandler

Windows Der Explorer steuert die Erstellung eines Suchconnectors für einen Protokollhandler über Registrierungsschlüsseleinträge. Über die Registrierung können sowohl Implementierer als auch Drittanbieter neue und ältere Protokollhandler für die Teilnahme an der Windows 7-Suche aktivieren.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu Suchconnectors für Protokollhandler in Windows 7](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [Aktivieren der Teilnahme von Protokollhandlern an der Suche](#enabling-protocol-handlers-to-participate-in-search)
    -   [Deaktivieren der Connectorerstellung für die Protokollhandlersuche](#disabling-protocol-handler-search-connector-creation)
    -   [Anpassen des Namens, der Beschreibung oder des Ordnertyps für einen Protokollhandler-Suchconnector](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [Verwenden der Umleitung von Registrierungszeichenfolgen](#using-registry-string-redirection)
    -   [Wiederherstellen eines Connectors für die Suche nach gelöschten Protokollhandlern](#restoring-a-deleted-protocol-handler-search-connector)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a>Informationen zu Suchconnectors für Protokollhandler in Windows 7

In Windows 7 enthalten Suchvorgänge im **Startmenü** oder im Windows-Explorer nur Dateien an indizierten Speicherorten und Nichtdateisystemelemente wie Remotedatenspeicher oder Protokollhandlerelemente, die über einen Suchconnector verfügen. Zusätzlich zum Hinzufügen der Protokollhandlerelemente in den Bereich des **Startmenüs**  und der Shellsuche ermöglicht der Suchconnector dem Startmenü, Protokollhandlerelemente in den Ergebnissen des **Startmenüs** zusammen zu gruppen. Dies hat den Vorteil, dass der Benutzer auf den Gruppenheader klicken und nur die Ergebnisse des Protokollhandlers anzeigen kann. Alternativ kann der Benutzer zum  Ordner Suchen navigieren, die Suchconnectordatei öffnen und eine Suche durchführen, die nur Elemente aus dem spezifischen Protokollhandler enthält, der diesem Suchconnector zugeordnet ist.

Wenn ein Benutzer zum ersten Mal eine Anwendung startet, die einen Protokollhandler registriert, generiert Windows Explorer eine Suchconnectordatei  (.searchConnector-ms) für den Protokollhandler im Ordner Suchen des Benutzers. Anwendungen mit Protokollhandlern können dieses Verhalten deaktivieren oder den Namen und die Beschreibung des Protokollsuchconnectors anpassen.

> [!Note]  
> Der Speicherort des Ordners Suchen des **Benutzers** ist %userprofile% \\ Searches oder FOLDERID \_ SavedSearches. Die GUID für FOLDERID \_ SavedSearches ist {7d1d3a04-debb-4115-95cf-2f29da2920da}.

 

Windows Der Explorer steuert die Erstellung eines Suchconnectors für einen Protokollhandler über Registrierungsschlüsseleinträge, die in den folgenden Abschnitten beschrieben werden:

-   [Aktivieren der Teilnahme von Protokollhandlern an der Suche](#enabling-protocol-handlers-to-participate-in-search)
-   [Deaktivieren der Connectorerstellung für die Protokollhandlersuche](#disabling-protocol-handler-search-connector-creation)
-   [Anpassen des Namens, der Beschreibung oder des Ordnertyps für einen Protokollhandler-Suchconnector](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [Wiederherstellen eines Connectors für die Suche nach gelöschten Protokollhandlern](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> Es gibt keine programmgesteuerten Mittel zum Erstellen eines Suchconnectors für einen Protokollhandler. Sie müssen über die Registrierung konfiguriert werden.

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a>Aktivieren der Teilnahme von Protokollhandlern an der Suche

Registrierungsschlüssel und ihre möglichen Werte sind in der folgenden Tabelle aufgeführt. Ein Protokollhandler kann einige oder alle dieser Registrierungsschlüssel auffüllen, wobei das Protokoll durch den tatsächlichen Namen seines Protokolls ersetzt wird, z. B. MAPI, File oder &lt; &gt; csc.



| Registrierungsschlüssel                                                                                                                 | Mögliche Werte                                                                                                                     | Typ       | Kommentare                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors-Protokollversion \\ &lt; &gt; \\                     | Ist nicht vorhanden (Standard). Andernfalls ist es 1 oder höher.                                                                               | REG \_ DWORD | Dieser Wert wird verwendet, um Änderungen an den Speicherortvorlagenregistrierungen für Suchsynten zu erkennen, die bereits verarbeitet wurden. Wenn nicht vorhanden ist, verwenden Sie 0 als Standard. Erhöhen Sie alternativ die Version, um Windows Explorer darüber zu informieren, dass der Suchconnector neu generiert werden soll, da eine neuere Version des Protokollhandlers installiert wurde. |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors-Protokoll \\ &lt; &gt; \\ DoNotCreateSearchConnectors | Ist nicht vorhanden (Standard). Andernfalls auf 1 festgelegt.                                                                                         | REG \_ DWORD | Wenn sie nicht vorhanden ist, erstellen Sie im Ordner Suchen eine Searchconnector-ms-Datei. Wenn 1, markieren Sie als verarbeitet, und unternehmen Sie nichts.                                                                                                                                                                                                                                   |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors-Protokoll \\ &lt; &gt; \\ \\ Standardbeschreibung        | Eine lokalisierbare Zeichenfolge, die die Beschreibung des Suchconnectors enthält.                                                              | REG \_ SZ    | Optional. Sie wird im Description-Element der Datei .searchconnector-ms verwendet.                                                                                                                                                                                                                                                                          |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors-Protokoll \\ &lt; &gt; \\ \\ Standardname               | Eine lokalisierte Zeichenfolge zum Benennen des Suchconnectors. Wird als Name der Datei .searchconnector-ms verwendet.                                    | REG \_ SZ    | Jeder Standort muss einen eindeutigen Namen haben. Wenn dieser Wert nicht vorhanden ist, wird der von der [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Protokollhandlers bereitgestellte Anzeigename verwendet.                                                                                                                             |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors \\ &lt; protocol Default &gt; \\ \\ FolderType         | Eine GUID, die die [FOLDERTYPEID identifiziert,](../shell/foldertypeid.md) die auf den Suchconnector angewendet werden soll. | REG \_ SZ    | Optional. Wird im folderType-Element der Datei .searchconnector-ms verwendet, um anzugeben, welche Vorlagen zum Anzeigen von Ergebnissen verwendet werden sollen. Beispiel: der GUID-Wert von FOLDERTYPEID \_ Documents.                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a>Deaktivieren der Connectorerstellung für die Protokollhandlersuche

Wenn Ihre Anwendung Elemente über einen Protokollhandler zur Verwendung in der Anwendung selbst verfügbar macht und Sie die Elemente nicht über die Shell verfügbar machen möchten (im **Startmenü** und im Windows Explorer-Suchvorgänge), müssen Sie die Erstellung eines Suchconnectors für Ihren Protokollhandler deaktivieren.

Um die Erstellung des Suchconnectors zu deaktivieren, legen Sie DoNotCreateSearchConnectors auf 0x00000001(1) fest, wie im folgenden Registrierungsschlüsselbeispiel gezeigt.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

Wenn DoNotCreateSearchConnectors auf 1 festgelegt ist, wird empfohlen, dass Sie die [System.Shell.OmitFromView-Eigenschaft](/windows/desktop/properties/props-system-shell-omitfromview) für jedes Element verfügbar machen, das vom Protokollhandler verfügbar gemacht wird, und den Wert dieser Eigenschaft auf **TRUE festlegen.** Dadurch wird verhindert, dass die Protokollhandlerelemente unter der Gruppe **Dateien** im **Startmenü angezeigt** werden.

Wenn DoNotCreateSearchConnectors vorhanden ist und auf 0 festgelegt ist, erstellt Windows Explorer einen Suchconnector für den Protokollhandler, und die Protokollhandlerelemente werden im **Startmenü** zurückgegeben und Windows Explorer durchsucht.

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a>Anpassen des Namens, der Beschreibung oder des Ordnertyps für einen Protokollhandler-Suchconnector

Der Name des Suchconnectors wird nicht nur verwendet, um den Suchconnector im Ordner **Suchen** zu identifizieren, sondern auch als Gruppenheader für die Ergebnisse bei Suchvorgängen im **Startmenü.** Daher ist es wichtig, einen aussagekräftigen Namen für den Suchconnector zu geben. Wenn im Registrierungsschlüssel kein Name angegeben wird, verwendet Windows Explorer standardmäßig den von [der IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) bereitgestellten Namen für den Suchstamm und die leere Beschreibung des Protokollhandlers. Sie können den Standardnamen über einen Registrierungsschlüsseleintrag überschreiben, ohne die IShellFolder-Schnittstelle umbenennen zu müssen. Obwohl er nicht so sichtbar ist wie der Name des Suchconnectors, können Sie auch die Beschreibung für den Suchconnector überschreiben, indem Sie Eine eigene Beschreibung angeben.

Um den Standardnamen oder die Standardbeschreibung zu überschreiben, legen Sie die Einträge wie im folgenden Registrierungsbeispiel gezeigt fest.

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

Darüber hinaus kann der FolderType-Eintrag auf eine der [FOLDERTYPEID-GUIDs](../shell/foldertypeid.md) festgelegt werden. Der Wert sollte die tatsächliche GUID und nicht ihr Name sein. Beispiel: {94d6ddcc-4a68-4175-a374-bd584a510b78} anstelle von FOLDERTYPEID \_ Musik. Die GUID für eine FOLDERTYPEID kann in der Headerdatei Shlguid.h im Windows [SDK Windows werden.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

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

### <a name="using-registry-string-redirection"></a>Verwenden der Umleitung von Registrierungszeichenfolgen

Sie können eine [umgeleitete Zeichenfolge verwenden,](../intl/using-registry-string-redirection.md) um sicherzustellen, dass der Name, den Sie für den Suchconnector angeben, lokalisiert werden kann. Sie können lokalisierbare Zeichenfolgen für den Registrierungsschlüssel name und description angeben, anstatt die tatsächliche Zeichenfolge in die Registrierung eingibt.

Wenn Sie eine lokalisierbare Zeichenfolge für die Werte Name oder Beschreibung angeben, legen Sie den Wert wie im folgenden Registrierungsschlüsselbeispiel gezeigt fest.

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

-   @dllname.dll,-resourceID, wobei:
    -   @dllname.dll ist der Pfad zu der DLL, die die Zeichenfolgenressource enthält.
    -   resourceID ist die ganzzahlige Ressourcen-ID der Zeichenfolgenressource.

Das Format für eine indirekte Zeichenfolge und eine indirekte Zeichenfolge, die mit einem Versionsmodifizierer angefügt wird, wird unter [SHLoadIndirectString-Funktion beschrieben.](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a>Wiederherstellen eines Connectors für die Suche nach gelöschten Protokollhandlern

Da es sich bei Suchconnectors um Dateien auf dem Computer des Benutzers handelt, können sie fälschlicherweise gelöscht werden. Stellen Sie die Standardbibliotheken wieder zur Wiederherstellung aller gelöschten Protokollhandler-Suchconnectors wieder zur Verfügung. Öffnen Sie zu diesem Windows Explorer, klicken  Sie mit der rechten Maustaste auf den Ordner Bibliotheken, und wählen Sie dann **Standardbibliotheken wiederherstellen aus.**

![Screenshot: Menüoption "Standardbibliotheken wiederherstellen"](images/libraries.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

-   [IShellItem::GetDisplayName](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [SIGDN \_ NORMALDISPLAY](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Grundlegendes zu Protokollhandlern](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Entwickeln von Protokollhandlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[Benachrichtigen des Änderungsindexes](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Hinzufügen von Symbolen und Kontextmenüs](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Codebeispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokollhandlern](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Debuggen von Protokollhandlern](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
