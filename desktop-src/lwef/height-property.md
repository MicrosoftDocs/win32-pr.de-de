---
title: Height-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Height-Eigenschaft des Characters-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068510"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="6e7dd-104">Height-Eigenschaft (Characters-Objekt)</span><span class="sxs-lookup"><span data-stu-id="6e7dd-104">Height Property (Characters Object)</span></span>

<span data-ttu-id="6e7dd-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="6e7dd-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6e7dd-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e7dd-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6e7dd-107">Gibt die Höhe des Rahmens des angegebenen Zeichens zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="6e7dd-107">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="6e7dd-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6e7dd-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6e7dd-109">*agent\***. Zeichen ("**_CharacterID_*_")._ \*  \[ =  *Height-Wert*\]</span><span class="sxs-lookup"><span data-stu-id="6e7dd-109">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="6e7dd-110">Teil</span><span class="sxs-lookup"><span data-stu-id="6e7dd-110">Part</span></span>    | <span data-ttu-id="6e7dd-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e7dd-111">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="6e7dd-112">*value*</span><span class="sxs-lookup"><span data-stu-id="6e7dd-112">*value*</span></span> | <span data-ttu-id="6e7dd-113">Eine lange ganze Zahl, die die Framehöhe des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="6e7dd-113">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e7dd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e7dd-114">Remarks</span></span>

<span data-ttu-id="6e7dd-115">Die **Height-Eigenschaft** wird immer in Pixeln relativ zu Bildschirmkoordinaten (oben links) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="6e7dd-115">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="6e7dd-116">Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="6e7dd-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="6e7dd-117">Obwohl das Zeichen in einem unregelmäßig gestalteten Bereichsfenster angezeigt wird, basiert die Höhe des Zeichens auf den externen Dimensionen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft Agent-Zeichen-Editor verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6e7dd-117">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




