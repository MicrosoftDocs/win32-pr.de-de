---
title: Größen Ereignis
description: Größen Ereignis
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855983"
---
# <a name="size-event"></a><span data-ttu-id="9629d-103">Größen Ereignis</span><span class="sxs-lookup"><span data-stu-id="9629d-103">Size Event</span></span>

<span data-ttu-id="9629d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9629d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9629d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9629d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9629d-106">Tritt ein, wenn die Größe eines Zeichens geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9629d-106">Occurs when a character's size changes.</span></span>

</dd> <dt>

<span data-ttu-id="9629d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9629d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9629d-108">**Sub** - *Agent*- \_ **Größe (ByVal** - *Kenn zeichenkennung*, **ByVal** - *Breite*, **ByVal** - *Höhe*)</span><span class="sxs-lookup"><span data-stu-id="9629d-108">**Sub** *agent*\_**Size (ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)</span></span>



| <span data-ttu-id="9629d-109">Teil</span><span class="sxs-lookup"><span data-stu-id="9629d-109">Part</span></span>          | <span data-ttu-id="9629d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9629d-110">Description</span></span>                                                         |
|---------------|---------------------------------------------------------------------|
| <span data-ttu-id="9629d-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="9629d-111">*CharacterID*</span></span> | <span data-ttu-id="9629d-112">Gibt die ID des Zeichens zurück, das verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="9629d-112">Returns the ID of the character that moved.</span></span>                         |
| <span data-ttu-id="9629d-113">*Width*</span><span class="sxs-lookup"><span data-stu-id="9629d-113">*Width*</span></span>       | <span data-ttu-id="9629d-114">Gibt die neue Breite des Zeichen Rahmens (in Pixel) als ganze Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="9629d-114">Returns the character frame's new width (in pixels) as an integer.</span></span>  |
| <span data-ttu-id="9629d-115">*Height*</span><span class="sxs-lookup"><span data-stu-id="9629d-115">*Height*</span></span>      | <span data-ttu-id="9629d-116">Gibt die neue Höhe des Zeichen Rahmens (in Pixel) als ganze Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="9629d-116">Returns the character frame's new height (in pixels) as an integer.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9629d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9629d-117">Remarks</span></span>

<span data-ttu-id="9629d-118">Dieses Ereignis tritt auf, wenn eine Anwendung die Größe eines Zeichens ändert.</span><span class="sxs-lookup"><span data-stu-id="9629d-118">This event occurs when an application changes the size of a character.</span></span> <span data-ttu-id="9629d-119">Dieses Ereignis wird nur an die Clients des Zeichens gesendet (Anwendungen, die das Zeichen geladen haben).</span><span class="sxs-lookup"><span data-stu-id="9629d-119">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

### <a name="see-also"></a><span data-ttu-id="9629d-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9629d-120">See Also</span></span>

[<span data-ttu-id="9629d-121">**Ereignis verschieben**</span><span class="sxs-lookup"><span data-stu-id="9629d-121">**Move event**</span></span>](move-event.md)


 

 




