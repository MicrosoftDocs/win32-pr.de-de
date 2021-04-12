---
title: Definieren von Schweregraden
description: Ebenen werden verwendet, um Ereignisse zu gruppieren und in der Regel den Schweregrad oder die Ausführlichkeit eines Ereignisses anzugeben.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390089"
---
# <a name="defining-severity-levels"></a>Definieren von Schweregraden

Ebenen werden verwendet, um Ereignisse zu gruppieren und in der Regel den Schweregrad oder die Ausführlichkeit eines Ereignisses anzugeben. Verwenden Sie das **Level** -Element, um eine Ebene zu definieren. Die Winmeta.xml Datei definiert die folgenden häufig verwendeten Schweregrade:

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

Consumer verwenden Ebenen zum Abfragen von Ereignissen, die einen bestimmten Level-Wert enthalten. Eine ETW-Ablauf Verfolgungs Sitzung kann auch Ebenen verwenden, um die Ereignisse einzuschränken, die in die Protokolldatei für die Ereignis Ablauf Verfolgung geschrieben werden. Ereignisse mit einem ebenendwert, der gleich oder kleiner als der angegebene ebenendwert ist, werden in die Protokolldatei geschrieben. Wenn die Sitzung z. b. den Level-Wert für Win: Warning angegeben hat, enthält die Protokolldatei Warnungen, Fehler und kritische Ereignisse.

Im folgenden Beispiel wird gezeigt, wie eine Ebene definiert wird. Sie müssen die Attribute **Name** und **value** der Ebene angeben. Der Wert des **value** -Attributs muss zwischen 16 und 255 liegen. Das **Symbol** und die **Nachrichten** Attribute sind optional.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
