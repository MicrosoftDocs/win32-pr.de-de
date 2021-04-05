---
title: Helpmudeon (Eigenschaft)
description: Helpmudeon (Eigenschaft)
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710925"
---
# <a name="helpmodeon-property"></a><span data-ttu-id="e65a0-103">Helpmudeon (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e65a0-103">HelpModeOn Property</span></span>

<span data-ttu-id="e65a0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e65a0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e65a0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e65a0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e65a0-106">Gibt zurück oder legt fest, ob der kontextabhängige Hilfe Modus für das Zeichen eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="e65a0-106">Returns or sets whether context-sensitive Help mode is on for the character.</span></span>

</dd> <dt>

<span data-ttu-id="e65a0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e65a0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e65a0-108">\*Agent. ***Zeichen ("*** Merkmal-ID \* \* *"). Helpmodeon* \*  \[  =  *booleschen*\]</span><span class="sxs-lookup"><span data-stu-id="e65a0-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").HelpModeOn** \[ = *boolean*\]</span></span>



| <span data-ttu-id="e65a0-109">Teil</span><span class="sxs-lookup"><span data-stu-id="e65a0-109">Part</span></span>      | <span data-ttu-id="e65a0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e65a0-110">Description</span></span>                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e65a0-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="e65a0-111">*boolean*</span></span> | <span data-ttu-id="e65a0-112">Ein boolescher Ausdruck, der angibt, ob der kontextabhängige Hilfe Modus auf ON festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e65a0-112">A Boolean expression specifying whether context-sensitive Help mode is on.</span></span> <span data-ttu-id="e65a0-113">**True** Der Hilfe Modus ist "on".</span><span class="sxs-lookup"><span data-stu-id="e65a0-113">**True** Help mode is on.</span></span> <br/> <span data-ttu-id="e65a0-114">**False** (Standard) der Hilfe Modus ist off.</span><span class="sxs-lookup"><span data-stu-id="e65a0-114">**False** (Default) Help mode is off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e65a0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e65a0-115">Remarks</span></span>

<span data-ttu-id="e65a0-116">Wenn Sie diese Eigenschaft auf **true** festlegen, ändert sich der Mauszeiger in das kontextabhängige Hilfe Bild, wenn es über das Zeichen oder über das Popup Menü für das Zeichen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e65a0-116">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="e65a0-117">Wenn der Benutzer auf das Zeichen klickt oder zieht oder auf ein Element im Popupmenü des Zeichens klickt, löst der Server das [**helpcomplete**](helpcomplete-event.md) -Ereignis aus und beendet den Hilfe Modus.</span><span class="sxs-lookup"><span data-stu-id="e65a0-117">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**HelpComplete**](helpcomplete-event.md) event and exits Help mode.</span></span>

<span data-ttu-id="e65a0-118">Im Hilfe Modus sendet der Server die Ereignisse [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**dragcomplete**](dragcomplete-event.md)und [**Command**](command-event.md) nicht, es sei denn, Sie legen die Eigenschaft [**autopopupmenu**](autopopupmenu-property.md) auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="e65a0-118">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md), and [**Command**](command-event.md) events, unless you set the [**AutoPopupMenu**](autopopupmenu-property.md) property to **True**.</span></span> <span data-ttu-id="e65a0-119">In diesem Fall sendet der Server das **Click** -Ereignis (der Hilfe Modus wird nicht beendet), sondern nur für die Rechte Maustaste, damit Sie das Popup Menü anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="e65a0-119">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="e65a0-120">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="e65a0-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="e65a0-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e65a0-121">See Also</span></span>

[<span data-ttu-id="e65a0-122">**Helpcomplete-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="e65a0-122">**HelpComplete event**</span></span>](helpcomplete-event.md)


 

 





