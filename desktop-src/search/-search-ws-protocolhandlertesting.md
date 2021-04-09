---
description: Eine ganzzahlige Vorgehensweise beim Testen und Debuggen Ihrer protokollhandlerimplementierungen ist das Verständnis der Art und Weise
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Debuggen von Protokoll Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128516"
---
# <a name="debugging-protocol-handlers"></a>Debuggen von Protokoll Handlern

Eine ganzzahlige Vorgehensweise beim Testen und Debuggen Ihrer protokollhandlerimplementierungen ist das Verständnis der Art und Weise

Dieses Thema ist wie folgt organisiert:

-   [Informationen zum Debugging von Protokoll Handlern](#about-debugging-protocol-handlers)
-   [Einrichten des Debuggens](#setting-up-debugging)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-debugging-protocol-handlers"></a>Informationen zum Debugging von Protokoll Handlern

Der SearchIndexer-Prozess (searchindexer.exe) beginnt eine Kopie des SearchProtocolHost-Prozesses (SearchProtocolHost.exe) im Systemkontext und eine weitere Kopie im Benutzer Kontext. Anschließend werden die Protokollhandler nach Bedarf in den SearchProtocolHost-Prozess geladen. Sie werden erst entladen, wenn der Suchdienst beendet wurde. Dieselbe Instanz eines Protokoll Handlers wird beliebig oft wieder verwendet, während der Dienst ausgeführt wird.

Die SearchIndexer-und SearchProtocolHost-Prozesse kommunizieren häufig während der Indizierung. Wenn Sie den Prozess zum Debuggen von SearchProtocolHost anhalten oder anhalten, startet der SearchIndexer einen neuen SearchProtocolHost-Prozess, wodurch Ihre Debuggingsitzung ungültig wird. Wenn Sie den Debugger direkt an den SearchProtocolHost-Prozess anfügen, können Sie die Handle-Vererbung von searchindexer.exe zu searchprotocolhost.exe unterbrechen, und die beiden Prozesse können nicht miteinander kommunizieren.

Um diese Probleme zu vermeiden, müssen Sie den Suchdienst Benachrichtigen, den Sie Debuggen, und Sie müssen den Debugger an den SearchIndexer-Prozess anfügen, um die untergeordneten Prozesse wie im folgenden beschrieben zu debuggen.

## <a name="setting-up-debugging"></a>Einrichten des Debuggens

Führen Sie die folgenden Schritte aus, um das Debuggen für Ihren Protokollhandler einzurichten.

1.  Benachrichtigen Sie den Search-Dienst, den Sie Debuggen, indem Sie den debugfilters-Wert in der Registrierung auf 1 festlegen:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  Fügen Sie einen Debugger mit dem Registrierungsschlüssel für die Bild Datei Ausführungs Optionen an:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    Die Optionen für einen Beispiel Debugger werden in der folgenden Tabelle beschrieben.

    

    **Beispiel für die Verwendung des NGS-Debugger-**   *Debugger = C: Debugger \\ \\ntsd.exe-odgx-C: "sxe ld mydll.dll; g"*<br/>

3.  Starten Sie searchindexer.exe unter dem Debugger mithilfe von "compmgmt. msc", "Services. msc" oder einem Befehlsfenster mit Befehlen ähnlich den folgenden:
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

Um zwischen einem im Systemkontext laufenden SearchProtocolHost-Prozess und einem im Benutzer Kontext laufenden Prozess zu unterscheiden, können Sie die Umgebungs Zeichenfolgen überprüfen. Mit ntsd.exe können Sie z. b. den Erweiterungs Befehl " **!** " verwenden, um eine formatierte Ansicht der Informationen im Process Environment Block (-Peer) anzuzeigen.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Weitere Informationen zum Erstellen von Handlern finden Sie unter [Registrieren von Shellerweiterungen](../shell/reg-shell-exts.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>**Konzeptionelle**</dt> <dt><a href="-search-3x-wds-phaddins.md">Entwicklung von Protokoll Handlern</a></dt> mit Informationen zu <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Protokoll Handlern</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">, die den Index von Änderungen beim</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Hinzufügen von Symbolen und Kontextmenüs</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">angeben Code Beispiel: Shellerweiterungen für Protokoll</a></dt> Handler <dt><a href="-search-3x-wds-ph-search-connector.md">Erstellen eines Suchconnector für einen Protokollhandler erstellen</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">und Registrieren von Protokoll Handlern</a></dt> </dl>

 

 
