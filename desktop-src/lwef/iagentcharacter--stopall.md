---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120913"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="9c445-103">IAgentCharacter::StopAll</span><span class="sxs-lookup"><span data-stu-id="9c445-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="9c445-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9c445-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="9c445-105">Beendet alle Animationen (Anforderungen) und entfernt sie aus der Animationswarteschlange des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="9c445-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="9c445-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span><span class="sxs-lookup"><span data-stu-id="9c445-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="9c445-107">Ein Bitfeld, das die Typen der anzuhaltenden (und aus der Warteschlange des Zeichens zu entfernenden) Anforderungen angibt, bestehend aus folgendem Code:</span><span class="sxs-lookup"><span data-stu-id="9c445-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



| <span data-ttu-id="9c445-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9c445-108">Value</span></span>                                                                                  |  <span data-ttu-id="9c445-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c445-109">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c445-110">**const unsigned long** **STOP TYPE ALL = \_ \_ 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="9c445-110">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="9c445-111">Beendet alle Animationsanforderungen, einschließlich nicht in die Warteschlange [**gestellter**](iagentcharacter--prepare.md) Vorbereitungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="9c445-111">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="9c445-112">**const unsigned long** **STOP TYPE PLAY = \_ \_ 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="9c445-112">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="9c445-113">Beendet alle Wiedergabeanforderungen.</span><span class="sxs-lookup"><span data-stu-id="9c445-113">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="9c445-114">**const unsigned long** **STOP TYPE MOVE = \_ \_ 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="9c445-114">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="9c445-115">Beendet alle [**Move-Anforderungen.**](https://www.bing.com/search?q=**Move**)</span><span class="sxs-lookup"><span data-stu-id="9c445-115">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="9c445-116">**const unsigned long** **STOP TYPE SPEAK = \_ \_ 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="9c445-116">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="9c445-117">Beendet alle [**Speak-Anforderungen.**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="9c445-117">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="9c445-118">**const unsigned long** **STOP TYPE PREPARE = \_ \_ 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="9c445-118">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="9c445-119">Beendet alle in der [**Warteschlange warteschlangenbereiten**](iagentcharacter--prepare.md) Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="9c445-119">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="9c445-120">**const unsigned long** **STOP TYPE \_ \_ NONQUEUEDPREPARE = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="9c445-120">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="9c445-121">Beendet alle Vorbereitungsanforderungen, die sich nicht in der [**Warteschlange**](iagentcharacter--prepare.md) befinden.</span><span class="sxs-lookup"><span data-stu-id="9c445-121">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="9c445-122">**const unsigned long** **STOP TYPE VISIBLE = \_ \_ 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="9c445-122">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="9c445-123">Beendet alle [**Hide-**](iagentcharacter--hide.md) [**oder Show-Anforderungen.**](iagentcharacter--show.md)</span><span class="sxs-lookup"><span data-stu-id="9c445-123">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="9c445-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9c445-124">See Also</span></span>

[<span data-ttu-id="9c445-125">**IAgentCharacter::Stop**</span><span class="sxs-lookup"><span data-stu-id="9c445-125">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





