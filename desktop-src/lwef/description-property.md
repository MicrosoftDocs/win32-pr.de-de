---
title: Description-Eigenschaft (Features der Legacy-Windows-Umgebung)
description: Description-Eigenschaft
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039940"
---
# <a name="description-property-legacy-windows-environment-features"></a><span data-ttu-id="4528b-103">Description-Eigenschaft (Features der Legacy-Windows-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="4528b-103">Description Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="4528b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4528b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4528b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4528b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4528b-106">Gibt eine Zeichenfolge zurück, die die Beschreibung für das angegebene Zeichen angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4528b-106">Returns or sets a string that specifies the description for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="4528b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="4528b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4528b-108">*Agent*. **Zeichen ("**_Merkmal-ID_*_"). Description_* - \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="4528b-108">*agent*.**Characters("**_CharacterID_*_").Description_* \[ = *string*\]</span></span>



| <span data-ttu-id="4528b-109">Teil</span><span class="sxs-lookup"><span data-stu-id="4528b-109">Part</span></span>     | <span data-ttu-id="4528b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4528b-110">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4528b-111">*string*</span><span class="sxs-lookup"><span data-stu-id="4528b-111">*string*</span></span> | <span data-ttu-id="4528b-112">Ein Zeichen folgen Wert, der der Beschreibung des Zeichens entspricht (in der aktuellen Spracheinstellung).</span><span class="sxs-lookup"><span data-stu-id="4528b-112">A string value corresponding to the character's description (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4528b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4528b-113">Remarks</span></span>

<span data-ttu-id="4528b-114">Die **Beschreibung** eines Zeichens hängt möglicherweise von der **LanguageID** -Einstellung des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="4528b-114">A character's **Description** may depend on the character's **LanguageID** setting.</span></span> <span data-ttu-id="4528b-115">Der Name eines Zeichens in einer Sprache kann anders sein oder andere Zeichen als in einem anderen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4528b-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="4528b-116">Die Standard **Beschreibung** des Zeichens für eine bestimmte Sprache wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="4528b-116">The character's default **Description** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

> [!Note]  
> <span data-ttu-id="4528b-117">Die **Description** -Eigenschaften Einstellung ist optional und kann nicht für alle Zeichen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4528b-117">The **Description** property setting is optional and may not be supplied for all characters.</span></span>

 

 

 




