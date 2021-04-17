---
title: Eigenschaft "Vertrauen"
description: Eigenschaft "Vertrauen"
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390178"
---
# <a name="confidence-property"></a><span data-ttu-id="0a3e6-103">Eigenschaft "Vertrauen"</span><span class="sxs-lookup"><span data-stu-id="0a3e6-103">Confidence Property</span></span>

<span data-ttu-id="0a3e6-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0a3e6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0a3e6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a3e6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0a3e6-106">Gibt zurück oder legt fest, ob das **Vertrauen** des Clients in der Abhör Info angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0a3e6-106">Returns or sets whether the client's **Confidence** appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="0a3e6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0a3e6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0a3e6-108">\*Agent ***. Zeichen ("*** Merkmal-ID ***"). Befehle ("*** Name \***")**. \* \* Vertrauens\* \*  \[  =  *Nummer*\]</span><span class="sxs-lookup"><span data-stu-id="0a3e6-108">*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.\*\*Confidence*\* \[ = *Number*\]</span></span>



| <span data-ttu-id="0a3e6-109">Teil</span><span class="sxs-lookup"><span data-stu-id="0a3e6-109">Part</span></span>     | <span data-ttu-id="0a3e6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a3e6-110">Description</span></span>                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3e6-111">*Number*</span><span class="sxs-lookup"><span data-stu-id="0a3e6-111">*Number*</span></span> | <span data-ttu-id="0a3e6-112">Ein numerischer Ausdruck, der eine lange ganze Zahl ergibt, die den Vertrauens Wert für den [**Befehl**](/windows/desktop/lwef/the-command-object)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0a3e6-112">A numeric expression that evaluates to a Long integer that identifies confidence value for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a3e6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a3e6-113">Remarks</span></span>

<span data-ttu-id="0a3e6-114">Wenn der zurückgegebene Vertrauens Wert der besten Entsprechung (User Input. Confidence) nicht den Wert überschreitet, den Sie für die Eigenschaft **Vertrauen** festgelegt haben, wird der in [**conficetext**](confidencetext-property.md) angegebene Text in der lausch Info angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0a3e6-114">If the returned confidence value of the best match (UserInput.Confidence) does not exceed value you set for the **Confidence** property, the text supplied in [**ConfidenceText**](confidencetext-property.md) is displayed in the Listening Tip.</span></span>

 

 