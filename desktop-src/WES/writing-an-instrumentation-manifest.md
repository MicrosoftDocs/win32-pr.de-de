---
title: Schreiben eines Instrumentierungsmanifests
description: Anwendungen und DLLs verwenden ein Instrumentierungsmanifest, um ihre Instrumentierungsanbieter und die Ereignisse zu identifizieren, die die Anbieter schreiben.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc832278772a12195590a4efdb7b65478f22ef4a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812163"
---
# <a name="writing-an-instrumentation-manifest"></a>Schreiben eines Instrumentierungsmanifests

Anwendungen und DLLs verwenden ein Instrumentierungsmanifest, um ihre Instrumentierungsanbieter und die Ereignisse zu identifizieren, die die Anbieter schreiben. Ein Manifest ist eine XML-Datei, die die Elemente enthält, die Ihren Anbieter identifizieren. Die Konvention besteht in der Verwendung von .man als Erweiterung für Ihr Manifest. Das Manifest muss dem XSD-Ereignismanifest entsprechen. Weitere Informationen zum Schema finden Sie unter [EventManifest-Schema.](eventmanifestschema-schema.md)

Ein Instrumentierungsanbieter ist eine beliebige Anwendung oder DLL, die die [**Funktionen EventWriteEx,**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex) [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)oder [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) aufruft, um Ereignisse in eine ETW-Ablaufverfolgungssitzung [oder](/windows/desktop/ETW/event-tracing-portal) einen Ereignisprotokollkanal zu schreiben. Eine Anwendung kann einen einzelnen Instrumentierungsanbieter definieren, der alle ereignisse abdeckt, die sie schreibt, oder sie kann einen Anbieter für die Anwendung und einen Anbieter für jede ihrer DLLs definieren. Die Anzahl der Anbieter, die die Anwendung im Manifest definiert, hängt ausschließlich davon ab, wie die Anwendung die ereignisse organisieren möchte, die sie schreibt.

Der Vorteil der Angabe eines Anbieters für jede DLL ist, dass Sie dann die einzelnen Anbieter und somit die von ihnen generierten Ereignisse aktivieren und deaktivieren können. Dieser Vorteil gilt nur, wenn der Anbieter durch eine ETW-Ablaufverfolgungssitzung aktiviert wird. Alle Ereignisse, die einen Ereignisprotokollkanal angeben, werden immer in diesen Kanal geschrieben.

Das Manifest muss den Anbieter und die ereignisse identifizieren, die es schreibt, aber die anderen Metadaten wie Kanäle, Ebenen und Schlüsselwörter sind optional. Ob Sie die optionalen Metadaten definieren, hängt davon ab, wer die Ereignisse verwendet. Wenn Administratoren oder Supportmitarbeiter die Ereignisse beispielsweise mit einem Tool wie dem Windows Ereignisanzeige nutzen, das Ereignisse aus Ereignisprotokollkanälen liest, müssen Sie die Kanäle definieren, in die die Ereignisse geschrieben werden. Wenn der Anbieter jedoch nur durch eine ETW-Ablaufverfolgungssitzung aktiviert wird, müssen Sie keine Kanäle definieren.

Obwohl die Ebenen, Aufgaben, Opcodes und Schlüsselwörtermetadaten optional sind, sollten Sie sie verwenden, um die Ereignisse logisch zu gruppieren oder in bucket zu gruppieren. Das Gruppieren der Ereignisse hilft den Kunden, nur die Ereignisse zu nutzen, die von Interesse sind. Beispielsweise kann der Consumer alle Ereignisse abfragen, bei denen level "critical" und das Schlüsselwort "write" ist, oder alle Ereignisse abfragen, die von einer bestimmten Aufgabe geschrieben wurden.

Zusätzlich zu den Consumers, die Level und Schlüsselwörter verwenden, um bestimmte Ereignistypen zu nutzen, kann eine ETW-Ablaufverfolgungssitzung die Metadaten der Ebene und des Schlüsselworts verwenden, um ETW an die Begrenzung der Ereignisse zu bringen, die in das Ereignisablaufverfolgungsprotokoll geschrieben werden. Beispielsweise könnte die Sitzung die Ereignisse auf Ereignisse beschränken, bei denen level "error" oder "critical" und das Schlüsselwort "read" ist.

Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um die Ereignisse basierend auf Ereignisdaten zu filtern. Mit level und keywords bestimmt ETW, ob das Ereignis in das Protokoll geschrieben wird, aber mit Filtern verwendet der Anbieter die Filterdatenkriterien, um zu bestimmen, ob das Ereignis in diese Sitzung geschrieben wird. Die Filter sind nur anwendbar, wenn eine ETW-Ablaufverfolgungssitzung Ihren Anbieter aktiviert.

In den folgenden Abschnitten wird gezeigt, wie die Komponenten des Manifests definiert werden:

-   [Identifizieren des Anbieters](identifying-the-provider.md)
-   [Definieren der Kanäle, in die die Ereignisse geschrieben werden](defining-channels.md)
-   [Definieren der Schweregrade von Ereignissen, die der Anbieter schreibt](defining-severity-levels.md)
-   [Definieren der Aufgaben und Vorgänge, die Ihr Anbieter ausführt](defining-tasks-and-opcodes.md)
-   [Definieren der Schlüsselwörter, die die Ereignisse klassifizieren, die der Anbieter schreibt](defining-keywords-used-to-classify-types-of-events.md)
-   [Definieren der Filter, die der Anbieter zum Filtern der von ihm schreibten Ereignisse verwendet](defining-filters.md)
-   [Definieren der Name-Wert-Zuordnungen, auf die Ihre Vorlagendaten verweisen](defining-name-value-mappings.md)
-   [Definieren der Vorlagen, die die ereignisspezifischen Daten definieren](defining-event-data-templates.md)
-   [Definieren der Ereignisse, die der Anbieter schreibt](defining-events.md)

Obwohl Sie ein Instrumentierungsmanifest manuell erstellen können, sollten Sie die Verwendung des ECManGen.exe-Tools in Betracht ziehen, das im Ordner Bin des Windows \\ SDK enthalten ist. Das ECManGen.exe Tool verwendet eine GRAFISCHE BENUTZEROBERFLÄCHE, die Sie durch das Erstellen eines Manifests von Grund auf führt, ohne jemals XML-Tags verwenden zu müssen. Wenn Sie mit den Informationen in diesem Abschnitt und im [Abschnitt EventManifest-Schema](eventmanifestschema-schema.md) hilft, wenn Sie das Tool verwenden.

Wenn Sie Visual Studio als XML-Editor verwenden, können Sie dem Projekt das [EventManifest-Schema](eventmanifestschema-schema.md) hinzufügen (siehe XML-Menü), um IntelliSense, die Inlineschemavalidierung und andere Features zu nutzen, um das Schreiben des Manifests einfach und präzise zu machen.

Nachdem Sie Ihr Manifest geschrieben haben, verwenden Sie den Nachrichtencompiler, um das Manifest zu überprüfen und die Ressourcen- und Headerdateien zu generieren, die Sie in Ihren Anbieter hinzufügen. Weitere Informationen finden Sie unter [Kompilieren eines Instrumentierungsmanifests.](compiling-an-instrumentation-manifest.md)

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



 

 
