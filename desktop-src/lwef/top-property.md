---
title: Top-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Top-Eigenschaft (Characters-Objekt). Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396345"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="09586-104">Top-Eigenschaft (Characters-Objekt)</span><span class="sxs-lookup"><span data-stu-id="09586-104">Top Property (Characters Object)</span></span>

<span data-ttu-id="09586-105">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="09586-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="09586-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09586-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="09586-107">Gibt den oberen Rand des Rahmens des angegebenen Zeichens zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="09586-107">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="09586-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="09586-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="09586-109">*agent\***. Zeichen ("**_CharacterID_*_"). Oberster_ \*  \[  =  *Wert*\]</span><span class="sxs-lookup"><span data-stu-id="09586-109">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="09586-110">Teil</span><span class="sxs-lookup"><span data-stu-id="09586-110">Part</span></span>    | <span data-ttu-id="09586-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09586-111">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="09586-112">*value*</span><span class="sxs-lookup"><span data-stu-id="09586-112">*value*</span></span> | <span data-ttu-id="09586-113">Eine long-Ganzzahl, die den oberen Rand des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="09586-113">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09586-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09586-114">Remarks</span></span>

<span data-ttu-id="09586-115">Die **Top-Eigenschaft** wird immer in Pixel relativ zum Bildschirmursprung (oben links) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="09586-115">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="09586-116">Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="09586-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="09586-117">Obwohl das Zeichen in einem unregelmäßig formatierten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf den externen Dimensionen des rechteckigen Animationsrahmens, der beim Kompilieren des Zeichens mit dem Microsoft-Agent-Zeichen-Editor verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="09586-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="09586-118">Verwenden Sie die [**MoveTo-Methode,**](moveto-method.md) um die Position des Zeichens zu ändern.</span><span class="sxs-lookup"><span data-stu-id="09586-118">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="09586-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="09586-119">See Also</span></span>

<span data-ttu-id="09586-120">[**Left-Eigenschaft,**](left-property.md) [ **MoveTo-Methode**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="09586-120">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




