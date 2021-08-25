---
title: Definieren von Schweregraden
description: Ebenen werden verwendet, um Ereignisse zu gruppieren und geben in der Regel den Schweregrad oder die Ausführlichkeit eines Ereignisses an.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3c3c5e663e476f98bef5c9be3f20cae5e0e88a74a7996f6f515d1d92599eb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863680"
---
# <a name="defining-severity-levels"></a>Definieren von Schweregraden

Ebenen werden verwendet, um Ereignisse zu gruppieren und geben in der Regel den Schweregrad oder die Ausführlichkeit eines Ereignisses an. Um eine Ebene zu  definieren, verwenden Sie das level-Element. Die Winmeta.xml-Datei definiert die folgenden häufig verwendeten Schweregrade:

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

Consumer verwenden Ebenen, um Ereignisse abzufragen, die einen bestimmten Ebenenwert enthalten. Eine ETW-Ablaufverfolgungssitzung kann auch Ebenen verwenden, um die Ereignisse einzuschränken, die in die Ereignisablaufverfolgungsprotokolldatei geschrieben werden. Ereignisse mit einem Ebenenwert, der gleich oder kleiner als der angegebene Ebenenwert ist, werden in die Protokolldatei geschrieben. Wenn die Sitzung beispielsweise den Ebenenwert für win:Warning angegeben hat, enthält die Protokolldatei Warnungs-, Fehler- und kritische Ereignisse.

Das folgende Beispiel zeigt, wie eine Ebene definiert wird. Sie müssen den **Namen** und die **Wertattribute** der Ebene angeben. Der Wert  des Wertattributs muss im Bereich von 16 bis 255 liegen. Die **Symbol-** und **Meldungsattribute** sind optional.


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
