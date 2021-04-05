---
title: Activateinput-Ereignis
description: Activateinput-Ereignis
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037481"
---
# <a name="activateinput-event"></a><span data-ttu-id="3d208-103">Activateinput-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3d208-103">ActivateInput Event</span></span>

<span data-ttu-id="3d208-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3d208-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3d208-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3d208-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3d208-106">Tritt auf, wenn ein Client als Eingabe aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="3d208-106">Occurs when a client becomes input-active.</span></span>

</dd> <dt>

<span data-ttu-id="3d208-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3d208-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3d208-108">**Sub** - *Agent* \_ activateinput **(ByVal** - *Merkmal-ID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="3d208-108">**Sub** *agent*\_ActivateInput **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="3d208-109">Teil</span><span class="sxs-lookup"><span data-stu-id="3d208-109">Part</span></span>          | <span data-ttu-id="3d208-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d208-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="3d208-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="3d208-111">*CharacterID*</span></span> | <span data-ttu-id="3d208-112">Gibt die ID des Zeichens zurück, über das der Client als Eingabe aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="3d208-112">Returns the ID of the character through which the client becomes input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3d208-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d208-113">Remarks</span></span>

<span data-ttu-id="3d208-114">Der Input-Active-Client empfängt die vom Server bereitgestellten Maus-und Spracheingabe Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="3d208-114">The input-active client receives mouse and speech input events supplied by the server.</span></span> <span data-ttu-id="3d208-115">Der Server sendet dieses Ereignis nur an den Client, der als Eingabe aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="3d208-115">The server sends this event only to the client that becomes input-active.</span></span>

<span data-ttu-id="3d208-116">Dieses Ereignis kann auftreten, wenn der Benutzer zum [Befehls](the-command-object.md) Objekt wechselt, z. b. durch Auswählen des Befehls Objekt Eintrags im Befehlsfenster oder im Popup Menü eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3d208-116">This event can occur when the user switches to your [Command](the-command-object.md) object, for example, by choosing your Command object entry in the Commands Window or in the pop-up menu for a character.</span></span> <span data-ttu-id="3d208-117">Dies kann auch vorkommen, wenn der Benutzer ein Zeichen (durch Klicken oder benennen des Namens) auswählt, wenn ein Zeichen sichtbar wird und wenn das Zeichen einer anderen Client Anwendung ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d208-117">It can also occur when the user selects a character (by clicking or speaking its name), when a character becomes visible, and when the character of another client application becomes hidden.</span></span> <span data-ttu-id="3d208-118">Sie können auch die [Aktivierungsmethode](activate-method.md) (mit dem **Status** 2) aufgerufen werden, um explizit das Zeichen zu erstellen, was dazu führt, dass die Client Anwendung aktiv wird und dieses Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="3d208-118">You can also call the [Activate Method](activate-method.md) (with **State** set to 2) to explicitly make the character topmost, which results in your client application becoming input-active and triggers this event.</span></span> <span data-ttu-id="3d208-119">Dieses Ereignis tritt jedoch nicht auf, wenn Sie die Methode Methode aktivieren nur verwenden, um anzugeben, ob der Client der aktive Client des Zeichens ist.</span><span class="sxs-lookup"><span data-stu-id="3d208-119">However, this event does not occur if you use the Activate Method method only to specify whether your client is the active client of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="3d208-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3d208-120">See Also</span></span>

<span data-ttu-id="3d208-121">[**Deactivateinput** -Ereignis](deactivateinput-event.md), [Methode **aktivieren**](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="3d208-121">[**DeactivateInput** event](deactivateinput-event.md), [**Activate** method](activate-method.md)</span></span>


 

 




