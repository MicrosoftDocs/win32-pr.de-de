---
title: Conficetext-Eigenschaft
description: Conficetext-Eigenschaft
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390241"
---
# <a name="confidencetext-property"></a><span data-ttu-id="59535-103">Conficetext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="59535-103">ConfidenceText Property</span></span>

<span data-ttu-id="59535-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="59535-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="59535-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59535-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="59535-106">Gibt den **vertrauenden Text** des Clients zurück, der in der Abhör Info angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="59535-106">Returns or sets the client's **ConfidenceText** that appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="59535-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="59535-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="59535-108">\*-Agent ***. Zeichen ("*** Merkmal-ID ***"). Befehle ("*** Name \***")**. **Vertrauvertrautext** \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="59535-108">\*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.**ConfidenceText**\[ = *string*\]</span></span>



| <span data-ttu-id="59535-109">Teil</span><span class="sxs-lookup"><span data-stu-id="59535-109">Part</span></span>     | <span data-ttu-id="59535-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59535-110">Description</span></span>                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59535-111">*string*</span><span class="sxs-lookup"><span data-stu-id="59535-111">*string*</span></span> | <span data-ttu-id="59535-112">Ein Zeichen folgen Ausdruck, der den Text für den **vertrauentext** für den [**Befehl**](/windows/desktop/lwef/the-command-object)ergibt.</span><span class="sxs-lookup"><span data-stu-id="59535-112">A string expression that evaluates to the text for the **ConfidenceText** for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59535-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59535-113">Remarks</span></span>

<span data-ttu-id="59535-114">Wenn der zurückgegebene Vertrauens Wert der besten Entsprechung (User Input. Confidence) die Einstellung " [**Vertrauen**](confidence-property.md) " nicht überschreitet, zeigt der Server den Text an, der in " **vertrauenstext** " in der Abhör info angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="59535-114">When the returned confidence value of the best match (UserInput.Confidence) does not exceed the [**Confidence**](confidence-property.md) setting, the server displays the text supplied in **ConfidenceText** in the Listening Tip.</span></span>

 

 