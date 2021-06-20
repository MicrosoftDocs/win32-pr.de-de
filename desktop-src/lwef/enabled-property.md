---
title: Enabled-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die Enabled Balloon-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407303"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="3585c-104">Enabled-Eigenschaft (Balloon-Objekt)</span><span class="sxs-lookup"><span data-stu-id="3585c-104">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="3585c-105">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3585c-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3585c-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3585c-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3585c-107">Gibt zurück, ob die Wortsprechblase für das angegebene Zeichen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3585c-107">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="3585c-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3585c-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3585c-109">*agent\***. Zeichen ("**_CharacterID_*_"). Balloon.Enabled_\*</span><span class="sxs-lookup"><span data-stu-id="3585c-109">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="3585c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="3585c-110">Value</span></span>     | <span data-ttu-id="3585c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3585c-111">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="3585c-112">**True**</span><span class="sxs-lookup"><span data-stu-id="3585c-112">**True**</span></span>  | <span data-ttu-id="3585c-113">Die Sprechblase ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3585c-113">The balloon is enabled.</span></span>  |
| <span data-ttu-id="3585c-114">**False**</span><span class="sxs-lookup"><span data-stu-id="3585c-114">**False**</span></span> | <span data-ttu-id="3585c-115">Die Sprechblase ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3585c-115">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3585c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3585c-116">Remarks</span></span>

<span data-ttu-id="3585c-117">Die **Enabled-Eigenschaft** gibt einen booleschen Wert zurück, der angibt, ob die Sprechblase aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3585c-117">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="3585c-118">Der Standardzustand des Sprechblasens wird als Teil der Definition eines Zeichens festgelegt, wenn das Zeichen im Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="3585c-118">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="3585c-119">Wenn ein Zeichen so definiert ist, dass es die Wortsprechblase nicht unterstützt, ist diese Eigenschaft für das Zeichen immer **False.**</span><span class="sxs-lookup"><span data-stu-id="3585c-119">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




