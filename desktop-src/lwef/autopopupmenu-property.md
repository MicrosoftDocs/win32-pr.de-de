---
title: Autopopupmenu (Eigenschaft)
description: Autopopupmenu (Eigenschaft)
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310807"
---
# <a name="autopopupmenu-property"></a><span data-ttu-id="74652-103">Autopopupmenu (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="74652-103">AutoPopupMenu Property</span></span>

<span data-ttu-id="74652-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="74652-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="74652-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="74652-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="74652-106">Gibt zurück oder legt fest, ob beim Klicken mit der rechten Maustaste auf das Zeichen oder das zugehörige Task leisten Symbol automatisch das Popup Menü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="74652-106">Returns or sets whether right-clicking the character or its taskbar icon automatically displays the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="74652-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="74652-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="74652-108">\*Agent. ***Zeichen \* \* \* \* ("*** Merkmal-ID \* \* *"). Autopopupmenu*- \*  \[  =  *boolescher* Wert\]</span><span class="sxs-lookup"><span data-stu-id="74652-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").AutoPopupMenu** \[ = *boolean*\]</span></span>



| <span data-ttu-id="74652-109">Teil</span><span class="sxs-lookup"><span data-stu-id="74652-109">Part</span></span>      | <span data-ttu-id="74652-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74652-110">Description</span></span>                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74652-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="74652-111">*boolean*</span></span> | <span data-ttu-id="74652-112">Ein boolescher Ausdruck, der angibt, ob der Server beim Klicken mit der rechten Maustaste automatisch das Popup Menü des Zeichens anzeigt.</span><span class="sxs-lookup"><span data-stu-id="74652-112">A Boolean expression specifying whether the server automatically displays the character's pop-up menu on right-click.</span></span> <span data-ttu-id="74652-113">**True** (Standard) zeigt das Menü mit der rechten Maustaste an.</span><span class="sxs-lookup"><span data-stu-id="74652-113">**True** (Default) Displays the menu on right-click.</span></span> <br/> <span data-ttu-id="74652-114">**False** Mit der rechten Maustaste wird das Menü nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74652-114">**False** Does not display the menu on right-click.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74652-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74652-115">Remarks</span></span>

<span data-ttu-id="74652-116">Wenn Sie diese Eigenschaft auf " **false**" festlegen, können Sie ein eigenes Menü Verarbeitungs Verhalten erstellen.</span><span class="sxs-lookup"><span data-stu-id="74652-116">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="74652-117">Verwenden Sie die [**showPopupMenu**](showpopupmenu-method.md) -Methode, um das Menü nach dem Festlegen dieser Eigenschaft auf **false** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="74652-117">To display the menu after setting this property to **False**, use the [**ShowPopupMenu**](showpopupmenu-method.md) method.</span></span>

<span data-ttu-id="74652-118">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="74652-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="74652-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="74652-119">See Also</span></span>

[<span data-ttu-id="74652-120">**ShowPopupMenu-Methode**</span><span class="sxs-lookup"><span data-stu-id="74652-120">**ShowPopupMenu method**</span></span>](showpopupmenu-method.md)


 

 





