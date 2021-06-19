---
title: Width-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Width-Eigenschaft des Characters-Objekts, die die Breite des Frames für das angegebene Zeichen zurückgibt oder legt.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395126"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="9e498-103">Width-Eigenschaft (Characters-Objekt)</span><span class="sxs-lookup"><span data-stu-id="9e498-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="9e498-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9e498-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9e498-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e498-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9e498-106">Gibt die Breite des Frames für das angegebene Zeichen zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="9e498-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="9e498-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9e498-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="9e498-108">*agent\***. Zeichen ("**_CharacterID_*_"). Breitenwert_ \*  \[ =  \]</span><span class="sxs-lookup"><span data-stu-id="9e498-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="9e498-109">Teil</span><span class="sxs-lookup"><span data-stu-id="9e498-109">Part</span></span>    | <span data-ttu-id="9e498-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e498-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="9e498-111">*value*</span><span class="sxs-lookup"><span data-stu-id="9e498-111">*value*</span></span> | <span data-ttu-id="9e498-112">Eine lange ganze Zahl, die die Framebreite des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="9e498-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e498-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e498-113">Remarks</span></span>

<span data-ttu-id="9e498-114">Die [**Width-Eigenschaft**](width-property.md) wird immer in Pixel ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="9e498-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="9e498-115">Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="9e498-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="9e498-116">Obwohl das Zeichen in einem unregelmäßig angeordneten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf den externen Dimensionen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft Agent-Zeichen-Editor verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9e498-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




