---
title: Width-Eigenschaft (Character-Objekt)
description: Width-Eigenschaft
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039958"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="e2bb4-103">Width-Eigenschaft (Character-Objekt)</span><span class="sxs-lookup"><span data-stu-id="e2bb4-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="e2bb4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e2bb4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e2bb4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2bb4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e2bb4-106">Gibt die Breite des Frames für das angegebene Zeichen zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="e2bb4-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e2bb4-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="e2bb4-108">\*Agent \***. Zeichen ("**_Merkmal-ID_\*_"). Width_- \*  \[ =  *Wert*\]</span><span class="sxs-lookup"><span data-stu-id="e2bb4-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="e2bb4-109">Teil</span><span class="sxs-lookup"><span data-stu-id="e2bb4-109">Part</span></span>    | <span data-ttu-id="e2bb4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2bb4-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="e2bb4-111">*value*</span><span class="sxs-lookup"><span data-stu-id="e2bb4-111">*value*</span></span> | <span data-ttu-id="e2bb4-112">Eine lange ganze Zahl, die die Rahmenbreite des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2bb4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2bb4-113">Remarks</span></span>

<span data-ttu-id="e2bb4-114">Die [**Width**](width-property.md) -Eigenschaft wird immer in Pixel ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="e2bb4-115">Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="e2bb4-116">Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf den externen Dimensionen des rechteckigen Animations Rahmens, der verwendet wurde, als das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




