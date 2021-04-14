---
title: FontSize-Eigenschaft (Sprechblasen Objekt)
description: FontSize-Eigenschaft
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569c07e98fb8bf973a554e89655f71e816b4a51b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391444"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="c3280-103">FontSize-Eigenschaft (Sprechblasen Objekt)</span><span class="sxs-lookup"><span data-stu-id="c3280-103">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="c3280-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c3280-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c3280-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3280-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c3280-106">Gibt den Schrift Grad zurück, der für die Wort Sprechblase für das angegebene Zeichen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c3280-106">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="c3280-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c3280-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c3280-108">*Agent. \* \* \* Zeichen* \*  **("**_Merkmal-ID_*_"). Sprechblase. FontSize_* - \[  =  *Punkte*\]</span><span class="sxs-lookup"><span data-stu-id="c3280-108">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="c3280-109">Teil</span><span class="sxs-lookup"><span data-stu-id="c3280-109">Part</span></span>     | <span data-ttu-id="c3280-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3280-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="c3280-111">*Punkt*</span><span class="sxs-lookup"><span data-stu-id="c3280-111">*Points*</span></span> | <span data-ttu-id="c3280-112">Ein Long Integer-Wert, der den Schrift Grad in Punkten angibt.</span><span class="sxs-lookup"><span data-stu-id="c3280-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3280-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3280-113">Remarks</span></span>

<span data-ttu-id="c3280-114">Die [**FontSize**](fontsize-property.md) -Eigenschaft gibt einen Long Integer-Wert zurück, der den aktuellen Schrift Grad in Punkten angibt.</span><span class="sxs-lookup"><span data-stu-id="c3280-114">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="c3280-115">Der maximale Wert für **FontSize** beträgt 2160 Punkte.</span><span class="sxs-lookup"><span data-stu-id="c3280-115">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="c3280-116">Der Standardwert für die Schriftart Einstellungen der Word-Sprechblase eines Zeichens wird im Microsoft-Agent-Zeichen-Editor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3280-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="c3280-117">Außerdem kann der Benutzer die Schriftart Einstellungen für alle Zeichen auf dem Eigenschaften Blatt Microsoft-Agent überschreiben.</span><span class="sxs-lookup"><span data-stu-id="c3280-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




