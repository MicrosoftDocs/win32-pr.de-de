---
title: Identifizieren des Anbieters
description: Ein Manifest kann einen oder mehrere Anbieter identifizieren. Um einen Anbieter zu identifizieren, verwenden Sie das provider-Element.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ae37b20ea37d7e67d97846d9e9338e36d52f94
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812670"
---
# <a name="identifying-the-provider"></a>Identifizieren des Anbieters

Ein Manifest kann einen oder mehrere Anbieter identifizieren. Um einen Anbieter zu identifizieren, verwenden Sie das **provider-Element.** Sie müssen die **Symbolattribute name,** **guid,** **resourceFileName,** **messageFileName** **und** angeben. Wenn Sie Ihr Manifest lokalisieren,  sollten Sie auch das Nachrichtenattribut angeben, das von den Kunden als Anzeigename des Anbieters verwendet wird. Wenn Sie das **Nachrichtenattribut nicht** angeben, verwenden Die Benutzer den Wert des **Namensattributs.**

Sie können bis zu 16 Anbieter im Manifest identifizieren. Wenn Sie mehr als 16 Anbieter identifizieren möchten, müssen Sie den **MessageTable-Abschnitt** des Manifests enthalten, den der 17. und anbieter zum Zuweisen von Ressourcenwerten für die von ihnen definierten Nachrichtenzeichenfolgen verwenden müssen. Die Meldungstabelle darf keine Nachrichtenzeichenfolgen enthalten, die von den Anbietern 1 bis 16 definiert werden.

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
