---
title: Aktivierte Eigenschaft (Sprechblasen Objekt)
description: Enabled-Eigenschaft
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341983"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="63757-103">Aktivierte Eigenschaft (Sprechblasen Objekt)</span><span class="sxs-lookup"><span data-stu-id="63757-103">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="63757-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="63757-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="63757-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63757-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="63757-106">Gibt zurück, ob die Word-Sprechblase für das angegebene Zeichen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63757-106">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="63757-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="63757-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="63757-108">\*Agent \***. Zeichen ("**_Merkmal-ID_*_"). Sprechblase. aktiviert_*</span><span class="sxs-lookup"><span data-stu-id="63757-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="63757-109">Wert</span><span class="sxs-lookup"><span data-stu-id="63757-109">Value</span></span>     | <span data-ttu-id="63757-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63757-110">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="63757-111">**True**</span><span class="sxs-lookup"><span data-stu-id="63757-111">**True**</span></span>  | <span data-ttu-id="63757-112">Die Sprechblase ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="63757-112">The balloon is enabled.</span></span>  |
| <span data-ttu-id="63757-113">**False**</span><span class="sxs-lookup"><span data-stu-id="63757-113">**False**</span></span> | <span data-ttu-id="63757-114">Die Sprechblase ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="63757-114">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63757-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63757-115">Remarks</span></span>

<span data-ttu-id="63757-116">Die **aktivierte** Eigenschaft gibt einen booleschen Wert zurück, der angibt, ob die Sprechblase aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63757-116">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="63757-117">Der Standardzustand der Word-Sprechblase wird als Teil der Definition eines Zeichens festgelegt, wenn das Zeichen im Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="63757-117">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="63757-118">Wenn ein Zeichen definiert ist, um die Word-Sprechblase nicht zu unterstützen, wird diese Eigenschaft für das Zeichen immer **false** sein.</span><span class="sxs-lookup"><span data-stu-id="63757-118">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




