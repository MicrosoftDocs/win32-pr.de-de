---
title: FontSize-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die FontSize Balloon-Objekteigenschaft. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068217"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="0fd64-104">FontSize-Eigenschaft (Balloon-Objekt)</span><span class="sxs-lookup"><span data-stu-id="0fd64-104">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="0fd64-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0fd64-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0fd64-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fd64-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0fd64-107">Gibt den Schriftgrad zurück, der für das Wort balloon für das angegebene Zeichen unterstützt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="0fd64-107">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="0fd64-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0fd64-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0fd64-109">*agent.\*\*Characters* \*  **("**_CharacterID_*_"). Balloon.FontSize-Punkte_* \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="0fd64-109">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="0fd64-110">Teil</span><span class="sxs-lookup"><span data-stu-id="0fd64-110">Part</span></span>     | <span data-ttu-id="0fd64-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fd64-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="0fd64-112">*Punkte*</span><span class="sxs-lookup"><span data-stu-id="0fd64-112">*Points*</span></span> | <span data-ttu-id="0fd64-113">Ein ganzzahliger Long-Wert, der den Schriftgrad in Punkten angibt.</span><span class="sxs-lookup"><span data-stu-id="0fd64-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fd64-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fd64-114">Remarks</span></span>

<span data-ttu-id="0fd64-115">Die [**FontSize-Eigenschaft**](fontsize-property.md) gibt einen long integer-Wert zurück, der den aktuellen Schriftgrad in Punkten angibt.</span><span class="sxs-lookup"><span data-stu-id="0fd64-115">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="0fd64-116">Der Höchstwert für **FontSize** beträgt 2160 Punkte.</span><span class="sxs-lookup"><span data-stu-id="0fd64-116">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="0fd64-117">Der Standardwert für die Schriftarteinstellungen der Wortsprechblase eines Zeichens wird im Microsoft Agent-Zeichen-Editor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0fd64-117">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0fd64-118">Darüber hinaus kann der Benutzer Schriftarteinstellungen für alle Zeichen im Microsoft Agent-Eigenschaftenblatt überschreiben.</span><span class="sxs-lookup"><span data-stu-id="0fd64-118">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




