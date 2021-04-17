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
# <a name="identifying-the-provider"></a><span data-ttu-id="76a58-104">Identifizieren des Anbieters</span><span class="sxs-lookup"><span data-stu-id="76a58-104">Identifying the Provider</span></span>

<span data-ttu-id="76a58-105">Ein Manifest kann einen oder mehrere Anbieter identifizieren.</span><span class="sxs-lookup"><span data-stu-id="76a58-105">A manifest can identify one or more providers.</span></span> <span data-ttu-id="76a58-106">Verwenden Sie das **Provider** -Element, um einen Anbieter zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="76a58-106">To identify a provider, use the **provider** element.</span></span> <span data-ttu-id="76a58-107">Sie müssen die Attribute " **Name**", " **GUID**", " **resourceFileName**", " **messagefilename**" und " **Symbol** " angeben.</span><span class="sxs-lookup"><span data-stu-id="76a58-107">You must specify the **name**, **guid**, **resourceFileName**, **messageFileName**, and **symbol** attributes.</span></span> <span data-ttu-id="76a58-108">Wenn Sie das Manifest lokalisieren, sollten Sie auch das **Nachrichten** Attribut angeben, das von den Consumern verwendet wird, um den Namen des Anbieters anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="76a58-108">If you localize your manifest, you should also specify the **message** attribute, which consumers use as the display the name of the provider.</span></span> <span data-ttu-id="76a58-109">Wenn Sie das **Message** -Attribut nicht angeben, verwenden Consumer den Wert des **Name** -Attributs.</span><span class="sxs-lookup"><span data-stu-id="76a58-109">If you do not specify the **message** attribute, consumers use the value of the **name** attribute.</span></span>

<span data-ttu-id="76a58-110">Im Manifest können bis zu 16 Anbieter identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="76a58-110">You can identify up to 16 providers in the manifest.</span></span> <span data-ttu-id="76a58-111">Wenn Sie mehr als 16 Anbieter identifizieren möchten, müssen Sie den Abschnitt **messagetable** des Manifests einschließen, mit dem die-und-Anbieter Ressourcen Werte für die Meldungs Zeichenfolgen zuweisen müssen, die Sie definieren – die Nachrichten Tabelle darf keine Nachrichten Zeichenfolgen enthalten, die von den Anbietern 1 bis 16 definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="76a58-111">If you want to identify more than 16 providers, you must include the **messageTable** section of the manifest that the seventeenth and on providers must use to assign resource values for the message strings that they define—the message table must not include any message strings that providers 1 through 16 defined.</span></span>

<span data-ttu-id="76a58-112">Im folgenden Beispiel wird gezeigt, wie das **Provider** -Element verwendet wird, um einen Anbieter zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="76a58-112">The following example shows how to use the **provider** element to identify a provider.</span></span>


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
