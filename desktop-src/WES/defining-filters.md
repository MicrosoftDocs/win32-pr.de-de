---
title: Definieren von Filtern
description: Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um Ereignisse basierend auf Ereignisdaten zu filtern.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d9d065fe3a46fc22114cfb4aed5b5b51d9a89eafa3280e2e258199e06aad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056018"
---
# <a name="defining-filters"></a>Definieren von Filtern

Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um Ereignisse basierend auf Ereignisdaten zu filtern. Mit level und keywords bestimmt ETW, ob das Ereignis in das Protokoll geschrieben wird. Bei Filtern verwendet der Anbieter jedoch die Filterdatenkriterien, die die steuernde Sitzung an sie übergibt (siehe [*EnableCallback-Funktion),*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) um zu bestimmen, ob das Ereignis in diese Sitzung schreibt. Die Filter sind nur anwendbar, wenn eine ETW-Ablaufverfolgungssitzung Ihren Anbieter aktiviert.

In der Regel schreiben Anbieter nur Ereignisse, und die Sitzung identifiziert die Ereignistypen, die mithilfe von Level und Schlüsselwörtern verwendet werden. Wenn der Anbieter einen Datenfilter für einen Ereignistyp definiert hat, kann die Sitzung damit Ereignisse für diesen Ereignistyp basierend auf den Ereignisdaten herausfiltern (die Semantik des Filters wird vom Anbieter definiert). Wenn Ihr Anbieter z. B. Prozessereignisse generiert, können Sie einen Datenfilter definieren, der Prozessereignisse basierend auf einem Prozessbezeichner gefiltert hat. Die Sitzung könnte dann einen Prozessbezeichner als Filterdaten an den Anbieter übergeben und nur Prozessereignisse für diesen Prozessbezeichner empfangen.

Das folgende Beispiel zeigt, wie sie das **Filterelement** verwenden, um einen Filter zu definieren. Sie müssen die Namens- und **Wertattribute** **des** Filters angeben. die anderen Attribute sind optional. Das **Tid-Attribut** ist erforderlich, wenn der Filter erfordert, dass die Sitzung Filterdaten übergehen muss.


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

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```