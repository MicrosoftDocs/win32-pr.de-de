---
title: Debug-Ereignis
description: Debug-Ereignis
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947838"
---
# <a name="deactivateinput-event"></a><span data-ttu-id="779fa-103">Debug-Ereignis</span><span class="sxs-lookup"><span data-stu-id="779fa-103">DeactivateInput Event</span></span>

<span data-ttu-id="779fa-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="779fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="779fa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="779fa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="779fa-106">Tritt auf, wenn ein Client nicht mehr Eingabe aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="779fa-106">Occurs when a client becomes non-input-active.</span></span>

</dd> <dt>

<span data-ttu-id="779fa-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="779fa-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="779fa-108">**Sub** - \*Agent \* \* \_ \*\* Geräte- \*  ID **(ByVal** - *Merkmal-ID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="779fa-108">**Sub** *agent\*\*\*\_DeactivateInput*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="779fa-109">Teil</span><span class="sxs-lookup"><span data-stu-id="779fa-109">Part</span></span>          | <span data-ttu-id="779fa-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="779fa-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="779fa-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="779fa-111">*CharacterID*</span></span> | <span data-ttu-id="779fa-112">Gibt die ID des Zeichens zurück, das dazu führt, dass der Client nicht mehr Eingabe aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="779fa-112">Returns the ID of the character that makes the client become non-input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="779fa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="779fa-113">Remarks</span></span>

<span data-ttu-id="779fa-114">Ein nicht-Eingabe-aktiv-Client empfängt keine Maus-oder sprach Ereignisse mehr vom Server (es sei denn, er wird erneut zur Eingabe aktiv).</span><span class="sxs-lookup"><span data-stu-id="779fa-114">A non-input-active client no longer receives mouse or speech events from the server (unless it becomes input-active again).</span></span> <span data-ttu-id="779fa-115">Der Server sendet dieses Ereignis nur an den Client, der als nicht Eingabe aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="779fa-115">The server sends this event only to the client that becomes non-input-active.</span></span>

<span data-ttu-id="779fa-116">Dieses Ereignis tritt auf, wenn die Client Anwendung aktiv ist und der Benutzer die Beschriftung eines anderen Clients im Popupmenü eines Zeichens oder im Fenster "Sprachbefehle" auswählt oder die [**Aktivierungs**](activate-method.md) Methode aufruft und den Parameter " **State** " auf 0 (null) festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="779fa-116">This event occurs when your client application is input-active and the user chooses the caption of another client in a character's pop-up menu or the Voice Commands Window or you call the [**Activate**](activate-method.md) method and set the **State** parameter to 0.</span></span> <span data-ttu-id="779fa-117">Dies kann auch vorkommen, wenn der Benutzer den Namen eines anderen Zeichens durch Klicken oder sprechen auswählt.</span><span class="sxs-lookup"><span data-stu-id="779fa-117">It may also occur when the user selects the name of another character by clicking or speaking.</span></span> <span data-ttu-id="779fa-118">Sie erhalten dieses Ereignis auch dann, wenn das Zeichen ausgeblendet ist oder ein anderes Zeichen sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="779fa-118">You also get this event when your character is hidden or another character becomes visible.</span></span>

### <a name="see-also"></a><span data-ttu-id="779fa-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="779fa-119">See Also</span></span>

[<span data-ttu-id="779fa-120">**Activateinput-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="779fa-120">**ActivateInput event**</span></span>](activateinput-event.md)


 

 




