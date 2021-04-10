---
title: Idleon-Eigenschaft
description: Idleon-Eigenschaft
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309139"
---
# <a name="idleon-property"></a><span data-ttu-id="9b591-103">Idleon-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9b591-103">IdleOn Property</span></span>

<span data-ttu-id="9b591-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9b591-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9b591-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b591-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9b591-106">Gibt einen booleschen Wert zurück, der bestimmt, ob der Server die **idlinger** -Zustands Animationen des angegebenen Zeichens verwaltet, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="9b591-106">Returns or sets a Boolean value that determines whether the server manages the specified character's **Idling** state animations.</span></span>

</dd> <dt>

<span data-ttu-id="9b591-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9b591-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9b591-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Idleon*- \*  \[  =  *boolescher* Wert\]</span><span class="sxs-lookup"><span data-stu-id="9b591-108">*agent ***.Characters ("*** CharacterID\*\*\*").IdleOn*\* \[ = *boolean*\]</span></span>

</dd> </dl> 

| <span data-ttu-id="9b591-109">Teil</span><span class="sxs-lookup"><span data-stu-id="9b591-109">Part</span></span>      | <span data-ttu-id="9b591-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b591-110">Description</span></span>                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b591-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="9b591-111">*boolean*</span></span> | <span data-ttu-id="9b591-112">Ein boolescher Ausdruck, der angibt, ob der Server den Leerlauf Modus verwaltet.</span><span class="sxs-lookup"><span data-stu-id="9b591-112">A Boolean expression specifying whether the server manages idle mode.</span></span> <span data-ttu-id="9b591-113">**True** (Standard) die Server Behandlung des Leerlauf Status ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9b591-113">**True** (Default) Server handling of the idle state is enabled.</span></span> <br/> <span data-ttu-id="9b591-114">**False** Die Server Behandlung des Leerlauf Zustands ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9b591-114">**False** Server handling of the idle state is disabled.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b591-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b591-115">Remarks</span></span>

<span data-ttu-id="9b591-116">Der Server legt automatisch ein Timeout fest, nachdem die letzte Animation für ein Zeichen wiedergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9b591-116">The server automatically sets a time-out after the last animation played for a character.</span></span> <span data-ttu-id="9b591-117">Wenn das Intervall des Zeit Gebers abgelaufen ist, beginnt der Server mit dem **Leerlauf** Zustand für ein Zeichen, wobei die zugehörigen **idck** -Animationen in regelmäßigen Abständen abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="9b591-117">When this timer's interval is complete, the server begins the **Idling** state for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="9b591-118">Wenn Sie verhindern möchten, dass der Server die **idck** -Zustands Animationen automatisch wieder gibt, legen Sie die-Eigenschaft auf " **false** " fest, und wiedergeben Sie eine Animation oder rufen Sie [**die Methode "**](stop-method.md)</span><span class="sxs-lookup"><span data-stu-id="9b591-118">If you want to disable the server from automatically playing the **Idling** state animations, set the property to **False** and play an animation or call the [**Stop**](stop-method.md) method.</span></span> <span data-ttu-id="9b591-119">Das Festlegen dieses Werts wirkt sich nicht auf den aktuellen Animations Zustand des Zeichens aus.</span><span class="sxs-lookup"><span data-stu-id="9b591-119">Setting this value does not affect the current animation state of the character.</span></span>

<span data-ttu-id="9b591-120">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="9b591-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 





