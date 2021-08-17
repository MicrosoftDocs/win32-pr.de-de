---
title: Identifizieren des Anbieters
description: Ein Manifest kann einen oder mehrere Anbieter identifizieren. Um einen Anbieter zu identifizieren, verwenden Sie das Provider-Element.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbce9b07aa8a2322311397ae9a48b3d72d60b784e5c55b028afc9772b53f63d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470920"
---
# <a name="identifying-the-provider"></a>Identifizieren des Anbieters

Ein Manifest kann einen oder mehrere Anbieter identifizieren. Um einen Anbieter zu identifizieren, verwenden Sie das **Provider-Element.** Sie müssen die **Symbolattribute** **name,** **guid,** **resourceFileName,** **messageFileName** und angeben. Wenn Sie Ihr Manifest lokalisieren,  sollten Sie auch das Nachrichtenattribut angeben, das Consumer als Anzeigename des Anbieters verwenden. Wenn Sie das **Nachrichtenattribut** nicht angeben, verwenden Consumer den Wert des **Attributs name.**

Sie können bis zu 16 Anbieter im Manifest identifizieren. Wenn Sie mehr als 16 Anbieter identifizieren möchten, müssen Sie den **MessageTable-Abschnitt** des Manifests einschließen, den der Siebzehnte und der Anbieter verwenden müssen, um Ressourcenwerte für die von ihnen definierten Nachrichtenzeichenfolgen zuzuweisen. Die Nachrichtentabelle darf keine Nachrichtenzeichenfolgen enthalten, die von den Anbietern 1 bis 16 definiert werden.

Das folgende Beispiel zeigt, wie sie das **Provider-Element** verwenden, um einen Anbieter zu identifizieren.


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
