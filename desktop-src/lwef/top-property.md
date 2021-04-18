---
title: Top-Eigenschaft (Zeichen-Objekt)
description: Top-Eigenschaft
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338307"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="bdb34-103">Top-Eigenschaft (Zeichen-Objekt)</span><span class="sxs-lookup"><span data-stu-id="bdb34-103">Top Property (Characters Object)</span></span>

<span data-ttu-id="bdb34-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bdb34-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bdb34-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdb34-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bdb34-106">Gibt den oberen Rand des Frames des angegebenen Zeichens zurück oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="bdb34-106">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="bdb34-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="bdb34-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bdb34-108">\*Agent \***. Zeichen ("**_Merkmal-ID_\*_"). Top_- \*  \[  =  *Wert*\]</span><span class="sxs-lookup"><span data-stu-id="bdb34-108">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="bdb34-109">Teil</span><span class="sxs-lookup"><span data-stu-id="bdb34-109">Part</span></span>    | <span data-ttu-id="bdb34-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdb34-110">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="bdb34-111">*value*</span><span class="sxs-lookup"><span data-stu-id="bdb34-111">*value*</span></span> | <span data-ttu-id="bdb34-112">Eine lange ganze Zahl, die den oberen Rand des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="bdb34-112">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdb34-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdb34-113">Remarks</span></span>

<span data-ttu-id="bdb34-114">Die **Top** -Eigenschaft wird immer in Pixel ausgedrückt, relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="bdb34-114">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="bdb34-115">Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="bdb34-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="bdb34-116">Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf den externen Dimensionen des rechteckigen Animations Rahmens, der verwendet wurde, als das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="bdb34-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="bdb34-117">Verwenden Sie die Methode " [**muveto**](moveto-method.md) ", um den Speicherort des Zeichens zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bdb34-117">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="bdb34-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bdb34-118">See Also</span></span>

<span data-ttu-id="bdb34-119">[**Left-Eigenschaft**](left-property.md), " [ **muveto** "-Methode](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="bdb34-119">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




