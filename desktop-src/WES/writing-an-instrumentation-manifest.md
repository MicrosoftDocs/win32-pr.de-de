---
title: Schreiben eines Instrumentierungs Manifests
description: Anwendungen und DLLs verwenden ein Instrumentierungs Manifest, um die Instrumentierungs Anbieter und die Ereignisse zu identifizieren, die von den Anbietern geschrieben werden.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390354"
---
# <a name="writing-an-instrumentation-manifest"></a>Schreiben eines Instrumentierungs Manifests

Anwendungen und DLLs verwenden ein Instrumentierungs Manifest, um die Instrumentierungs Anbieter und die Ereignisse zu identifizieren, die von den Anbietern geschrieben werden. Ein Manifest ist eine XML-Datei, die die Elemente enthält, die Ihren Anbieter identifizieren. Die Konvention besteht darin,. man als Erweiterung für das Manifest zu verwenden. Das Manifest muss der Ereignis Manifest-XSD entsprechen. Ausführliche Informationen zum Schema finden Sie unter [eventmanifest-Schema](eventmanifestschema-schema.md).

Bei einem Instrumentations Anbieter handelt es sich um eine beliebige Anwendung oder dll, die die Funktionen [**EventWrite-Ex**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWrite-String**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)oder [**eventschreitetransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) zum Schreiben von Ereignissen in eine Ablauf Verfolgungs Sitzung ( [Event Tracing](/windows/desktop/ETW/event-tracing-portal) , etw) oder einen Ereignisprotokoll Kanal aufruft. Eine Anwendung kann einen einzelnen Instrumentierungs Anbieter definieren, der alle Ereignisse abdeckt, die geschrieben werden, oder es kann einen Anbieter für die Anwendung und einen Anbieter für jede seiner DLLs definieren. Die Anzahl der Anbieter, die die Anwendung im Manifest definiert, hängt ausschließlich davon ab, wie die Anwendung die Ereignisse organisieren möchte, die Sie schreibt.

Der Vorteil der Angabe eines Anbieters für jede DLL besteht darin, dass Sie die einzelnen Anbieter und somit die generierten Ereignisse aktivieren und deaktivieren können. Dieser Vorteil gilt nur, wenn der Anbieter durch eine ETW-Ablauf Verfolgungs Sitzung aktiviert wird. Alle Ereignisse, die einen Ereignisprotokoll Kanal angeben, werden immer in diesen Channel geschrieben.

Das Manifest muss den Anbieter und die Ereignisse identifizieren, die es schreibt, aber die anderen Metadaten, z. b. Kanäle, Ebenen und Schlüsselwörter, sind optional. ob Sie die optionalen Metadaten definieren, hängt davon ab, wer die Ereignisse verbrauchen wird. Wenn beispielsweise Administratoren oder Supportmitarbeiter die Ereignisse mit einem Tool wie dem Windows-Ereignisanzeige nutzen, das Ereignisse aus Ereignisprotokoll Kanälen liest, müssen Sie die Kanäle definieren, auf die die Ereignisse geschrieben werden. Wenn der Anbieter jedoch nur durch eine ETW-Ablauf Verfolgungs Sitzung aktiviert wird, müssen Sie keine Kanäle definieren.

Obwohl die Metadaten für Ebenen, Tasks, Opcodes und Schlüsselwörter optional sind, sollten Sie diese verwenden, um die Ereignisse logisch zu gruppieren oder zu Bucket. Durch das Gruppieren der Ereignisse können die Consumer nur die Ereignisse nutzen, die von Interesse sind. Der Consumer könnte beispielsweise alle Ereignisse Abfragen, bei denen die Ebene "kritisch" und das Schlüsselwort "Write" ist, oder eine Abfrage für alle Ereignisse, die von einer bestimmten Aufgabe geschrieben wurden.

Zusätzlich zu den Consumern, die Level und Schlüsselwörter verwenden, um bestimmte Ereignis Typen zu verarbeiten, kann eine ETW-Ablauf Verfolgungs Sitzung die Metadaten der Ebene und des Schlüssel Worts verwenden, um etw anzuweisen, die in das Ereignis Ablauf Verfolgungs Protokoll geschriebenen Ereignisse einzuschränken. Beispielsweise kann die Sitzung die Ereignisse auf Ereignisse beschränken, bei denen die Ebene "Error" oder "Critical" und das Schlüsselwort "Read" lauten.

Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um die Ereignisse auf der Grundlage von Ereignisdaten zu filtern. Mit den Ebenen und Schlüsselwörtern bestimmt etw, ob das Ereignis in das Protokoll geschrieben wird, aber mit Filtern. der Anbieter verwendet die Filterdaten Kriterien, um zu bestimmen, ob das Ereignis in diese Sitzung geschrieben wird. Die Filter sind nur anwendbar, wenn der Anbieter durch eine ETW-Ablauf Verfolgungs Sitzung aktiviert wird.

In den folgenden Abschnitten wird gezeigt, wie die Komponenten des Manifests definiert werden:

-   [Identifizieren des Anbieters](identifying-the-provider.md)
-   [Definieren der Kanäle, an die die Ereignisse geschrieben werden](defining-channels.md)
-   [Definieren der Schweregrade von Ereignissen, die vom Anbieter geschrieben werden](defining-severity-levels.md)
-   [Definieren von Aufgaben und Vorgängen, die der Anbieter ausführt](defining-tasks-and-opcodes.md)
-   [Definieren der Schlüsselwörter, mit denen die vom Anbieter Schreibvorgänge klassifiziert werden](defining-keywords-used-to-classify-types-of-events.md)
-   [Definieren der Filter, die der Anbieter zum Filtern der von ihm Schreibvorgänge verwendet](defining-filters.md)
-   [Definieren von Name-Wert-Zuordnungen, auf die die Vorlagen Daten verweisen](defining-name-value-mappings.md)
-   [Definieren der Vorlagen, die ereignisspezifische Daten definieren](defining-event-data-templates.md)
-   [Definieren der vom Anbieter Schreibvorgänge](defining-events.md)

Obwohl Sie ein Instrumentations Manifest manuell erstellen können, sollten Sie die Verwendung des ECManGen.exe Tools in Erwägung gezogen, das im \\ Ordner "bin" des Windows SDK enthalten ist. Das ECManGen.exe Tool verwendet eine GUI, die Sie durch die Erstellung eines Manifests von Grund auf neu führt, ohne dass Sie jemals XML-Tags verwenden müssen. Wenn Sie die Informationen in diesem Abschnitt und im Abschnitt " [eventmanifest-Schema](eventmanifestschema-schema.md) " kennen, können Sie das Tool verwenden.

Wenn Sie Visual Studio als XML-Editor verwenden, können Sie dem Projekt das [Event Manifest](eventmanifestschema-schema.md) -Schema hinzufügen (siehe das XML-Menü), um IntelliSense, Inline Schema Validierung und andere Features zu nutzen, um das Schreiben des Manifests zu vereinfachen und zu optimieren.

Verwenden Sie nach dem Schreiben des Manifests den Nachrichten Compiler, um das Manifest zu validieren und die Ressourcen-und Header Dateien zu generieren, die Sie in Ihren Anbieter einschließen. Weitere Informationen finden Sie unter [Kompilieren eines Instrumentierungs Manifests](compiling-an-instrumentation-manifest.md).

Das folgende Beispiel zeigt das Gerüst eines vollständig definierten Ereignis Manifests.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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



 

 