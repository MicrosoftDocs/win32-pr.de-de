---
title: Identifizieren des Anbieters
description: Ein Manifest kann einen oder mehrere Anbieter identifizieren. Verwenden Sie das Provider-Element, um einen Anbieter zu identifizieren.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45941a540f8804beccc408435fc202593ddad601
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104516676"
---
# <a name="identifying-the-provider"></a>Identifizieren des Anbieters

Ein Manifest kann einen oder mehrere Anbieter identifizieren. Verwenden Sie das **Provider** -Element, um einen Anbieter zu identifizieren. Sie müssen die Attribute " **Name**", " **GUID**", " **resourceFileName**", " **messagefilename**" und " **Symbol** " angeben. Wenn Sie das Manifest lokalisieren, sollten Sie auch das **Nachrichten** Attribut angeben, das von den Consumern verwendet wird, um den Namen des Anbieters anzuzeigen. Wenn Sie das **Message** -Attribut nicht angeben, verwenden Consumer den Wert des **Name** -Attributs.

Im Manifest können bis zu 16 Anbieter identifiziert werden. Wenn Sie mehr als 16 Anbieter identifizieren möchten, müssen Sie den Abschnitt **messagetable** des Manifests einschließen, mit dem die-und-Anbieter Ressourcen Werte für die Meldungs Zeichenfolgen zuweisen müssen, die Sie definieren – die Nachrichten Tabelle darf keine Nachrichten Zeichenfolgen enthalten, die von den Anbietern 1 bis 16 definiert wurden.

Im folgenden Beispiel wird gezeigt, wie das **Provider** -Element verwendet wird, um einen Anbieter zu identifizieren.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
