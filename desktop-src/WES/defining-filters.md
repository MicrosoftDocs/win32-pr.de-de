---
title: Definieren von Filtern
description: Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um Ereignisse auf der Grundlage von Ereignisdaten zu filtern.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102207"
---
# <a name="defining-filters"></a>Definieren von Filtern

Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um Ereignisse auf der Grundlage von Ereignisdaten zu filtern. Mit der Ebene und den Schlüsselwörtern bestimmt etw, ob das Ereignis in das Protokoll geschrieben wird. Allerdings verwendet der Anbieter mit Filtern die Filterdaten Kriterien, die die steuernde Sitzung an ihn übergibt (siehe die [*enablecallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) -Funktion), um zu bestimmen, ob das Ereignis in diese Sitzung geschrieben wird. Die Filter sind nur anwendbar, wenn der Anbieter durch eine ETW-Ablauf Verfolgungs Sitzung aktiviert wird.

In der Regel schreiben Anbieter nur Ereignisse, und die Sitzung identifiziert die Typen von Ereignissen, die Sie mit der Ebene und den Schlüsselwörtern verwenden möchten. Wenn der Anbieter einen Daten Filter für einen Ereignistyp definiert hat, kann er von der Sitzung verwendet werden, um Ereignisse für diesen Ereignistyp basierend auf den Ereignisdaten herauszufiltern (die Semantik des Filters wird vom Anbieter definiert). Wenn Ihr Anbieter z. b. Prozess Ereignisse generiert, können Sie einen Daten Filter definieren, der Prozess Ereignisse auf der Grundlage eines Prozess Bezeichners gefiltert hat. Die Sitzung kann dann eine Prozess-ID als Filterdaten an den Anbieter übergeben und nur Prozess Ereignisse für diese Prozess-ID empfangen.

Im folgenden Beispiel wird gezeigt, wie das **Filter** -Element verwendet wird, um einen Filter zu definieren. Sie müssen die Attribute **Name** und **value** des Filters angeben. die anderen Attribute sind optional. Das **TID** -Attribut ist erforderlich, wenn der Filter erfordert, dass die Sitzung Filterdaten übergibt.


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