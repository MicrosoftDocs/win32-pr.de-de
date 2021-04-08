---
title: Height-Eigenschaft (Character-Objekt)
description: Height-Eigenschaft
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739321"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="32217-103">Height-Eigenschaft (Character-Objekt)</span><span class="sxs-lookup"><span data-stu-id="32217-103">Height Property (Characters Object)</span></span>

<span data-ttu-id="32217-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="32217-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="32217-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32217-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="32217-106">Gibt die Höhe des angegebenen Zeichen Rahmens zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="32217-106">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="32217-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="32217-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="32217-108">\*Agent \***. Zeichen ("**_Merkmal-ID_\*_"). Height_- \*  \[ =  *Wert*\]</span><span class="sxs-lookup"><span data-stu-id="32217-108">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="32217-109">Teil</span><span class="sxs-lookup"><span data-stu-id="32217-109">Part</span></span>    | <span data-ttu-id="32217-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32217-110">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="32217-111">*value*</span><span class="sxs-lookup"><span data-stu-id="32217-111">*value*</span></span> | <span data-ttu-id="32217-112">Eine lange ganze Zahl, die die Rahmenhöhe des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="32217-112">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32217-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32217-113">Remarks</span></span>

<span data-ttu-id="32217-114">Die **height** -Eigenschaft wird immer in Pixel ausgedrückt, relativ zu Bildschirm Koordinaten (oben links).</span><span class="sxs-lookup"><span data-stu-id="32217-114">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="32217-115">Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="32217-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="32217-116">Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert die Höhe des Zeichens auf den externen Dimensionen des rechteckigen Animations Rahmens, der verwendet wurde, als das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="32217-116">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




