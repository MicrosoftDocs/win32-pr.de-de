---
title: Schreiben eines Instrumentierungsmanifests
description: Anwendungen und DLLs verwenden ein Instrumentierungsmanifest, um ihre Instrumentierungsanbieter und die ereignisse zu identifizieren, die die Anbieter schreiben.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b3462d6adc264fba8ba155620a2bbb402d51d5d6fc24f7dbe879b9e2a91ec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587051"
---
# <a name="writing-an-instrumentation-manifest"></a>Schreiben eines Instrumentierungsmanifests

Anwendungen und DLLs verwenden ein Instrumentierungsmanifest, um ihre Instrumentierungsanbieter und die ereignisse zu identifizieren, die die Anbieter schreiben. Ein Manifest ist eine XML-Datei, die die Elemente enthält, die Ihren Anbieter identifizieren. Die Konvention besteht darin, .man als Erweiterung für Ihr Manifest zu verwenden. Das Manifest muss dem Ereignismanifest XSD entsprechen. Ausführliche Informationen zum Schema finden Sie unter [EventManifest-Schema.](eventmanifestschema-schema.md)

Ein Instrumentierungsanbieter ist jede Anwendung oder DLL, die die Funktionen [**EventWriteEx,**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex) [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)oder [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) aufruft, um Ereignisse in eine ETW-Ablaufverfolgungssitzung [(Event Tracing)](/windows/desktop/ETW/event-tracing-portal) oder einen Ereignisprotokollkanal zu schreiben. Eine Anwendung kann einen einzelnen Instrumentierungsanbieter definieren, der alle von ihr geschriebenen Ereignisse abdeckt, oder sie kann einen Anbieter für die Anwendung und einen Anbieter für jede ihrer DLLs definieren. Die Anzahl der Anbieter, die die Anwendung im Manifest definiert, hängt ausschließlich davon ab, wie die Anwendung die geschriebenen Ereignisse organisieren möchte.

Der Vorteil der Angabe eines Anbieters für jede DLL besteht darin, dass Sie dann die einzelnen Anbieter und somit die von ihnen generierten Ereignisse aktivieren und deaktivieren können. Dieser Vorteil gilt nur, wenn der Anbieter durch eine ETW-Ablaufverfolgungssitzung aktiviert wird. Alle Ereignisse, die einen Ereignisprotokollkanal angeben, werden immer in diesen Kanal geschrieben.

Das Manifest muss den Anbieter und die von ihm geschriebenen Ereignisse identifizieren, aber die anderen Metadaten wie Kanäle, Ebenen und Schlüsselwörter sind optional. Ob Sie die optionalen Metadaten definieren, hängt davon ab, wer die Ereignisse nutzen wird. Wenn Administratoren oder Supportmitarbeiter die Ereignisse beispielsweise mit einem Tool wie dem Windows Ereignisanzeige nutzen, das Ereignisse aus Ereignisprotokollkanälen liest, müssen Sie die Kanäle definieren, in die die Ereignisse geschrieben werden. Wenn der Anbieter jedoch nur durch eine ETW-Ablaufverfolgungssitzung aktiviert wird, müssen Sie keine Kanäle definieren.

Obwohl die Metadaten für Ebenen, Aufgaben, Opcodes und Schlüsselwörter optional sind, sollten Sie sie verwenden, um die Ereignisse logisch zu gruppieren oder zu bucketen. Das Gruppieren der Ereignisse hilft den Consumern, nur die Ereignisse zu nutzen, die von Interesse sind. Beispielsweise könnte der Consumer alle Ereignisse abfragen, bei denen die Ebene "kritisch" und das Schlüsselwort "write" ist, oder alle Ereignisse abfragen, die von einer bestimmten Aufgabe geschrieben wurden.

Zusätzlich zu Consumern, die Ebenen und Schlüsselwörter verwenden, um bestimmte Ereignistypen zu nutzen, kann eine ETW-Ablaufverfolgungssitzung die Ebenen- und Schlüsselwortmetadaten verwenden, um ETW anweisen, die Ereignisse einzuschränken, die in das Ereignisablaufverfolgungsprotokoll geschrieben werden. Beispielsweise könnte die Sitzung die Ereignisse auf Ereignisse beschränken, bei denen die Ebene "fehler" oder "kritisch" und das Schlüsselwort "read" ist.

Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um die Ereignisse basierend auf Ereignisdaten zu filtern. Mit level und keywords bestimmt ETW, ob das Ereignis in das Protokoll geschrieben wird, aber mit Filtern verwendet der Anbieter die Filterdatenkriterien, um zu bestimmen, ob das Ereignis in diese Sitzung geschrieben wird. Die Filter sind nur anwendbar, wenn eine ETW-Ablaufverfolgungssitzung Ihren Anbieter aktiviert.

In den folgenden Abschnitten wird gezeigt, wie Sie die Komponenten des Manifests definieren:

-   [Identifizieren des Anbieters](identifying-the-provider.md)
-   [Definieren der Kanäle, in die die Ereignisse geschrieben werden](defining-channels.md)
-   [Definieren der Schweregrade von Ereignissen, die der Anbieter schreibt](defining-severity-levels.md)
-   [Definieren der Aufgaben und Vorgänge, die ihr Anbieter ausführt](defining-tasks-and-opcodes.md)
-   [Definieren der Schlüsselwörter, die die vom Anbieter geschriebenen Ereignisse klassifizieren](defining-keywords-used-to-classify-types-of-events.md)
-   [Definieren der Filter, die der Anbieter zum Filtern der von ihm geschriebenen Ereignisse verwendet](defining-filters.md)
-   [Definieren der Namens-Wert-Zuordnungen, auf die Ihre Vorlagendaten verweisen](defining-name-value-mappings.md)
-   [Definieren der Vorlagen, die die ereignisspezifischen Daten definieren](defining-event-data-templates.md)
-   [Definieren der Ereignisse, die der Anbieter schreibt](defining-events.md)

Obwohl Sie ein Instrumentierungsmanifest manuell erstellen können, sollten Sie die Verwendung des tools ECManGen.exe in Betracht ziehen, das im Ordner Bin des Windows SDK enthalten \\ ist. Das tool ECManGen.exe verwendet eine GRAFISCHE Benutzeroberfläche, die Sie durch die Erstellung eines Manifests von Grund auf führt, ohne xml-Tags verwenden zu müssen. Wenn Sie mit den Informationen in diesem Abschnitt und im Abschnitt [EventManifest Schema (Ereignismanifestschema)](eventmanifestschema-schema.md) informiert sind, ist dies hilfreich, wenn Sie das Tool verwenden.

Wenn Sie Visual Studio als XML-Editor verwenden, können Sie dem Projekt das [EventManifest-Schema](eventmanifestschema-schema.md) hinzufügen (siehe XML-Menü), um IntelliSense, Inlineschemavalidierung und andere Funktionen zu nutzen, um das Schreiben des Manifests einfach und präzise zu gestalten.

Verwenden Sie nach dem Schreiben des Manifests den Nachrichtencompiler, um das Manifest zu überprüfen und die Ressourcen- und Headerdateien zu generieren, die Sie in Ihren Anbieter einschließen. Weitere Informationen finden Sie unter [Kompilieren eines Instrumentierungsmanifests.](compiling-an-instrumentation-manifest.md)

Das folgende Beispiel zeigt das Gerüst eines vollständig definierten Ereignismanifests.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 
