---
title: Iagentcharacter stopAll
description: Iagentcharacter stopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342290"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="08b46-103">Iagentcharacter:: stopAll</span><span class="sxs-lookup"><span data-stu-id="08b46-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="08b46-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="08b46-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="08b46-105">Beendet alle Animationen (Anforderungen) und entfernt Sie aus der Animations Warteschlange des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="08b46-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="08b46-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*ltype*</span><span class="sxs-lookup"><span data-stu-id="08b46-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="08b46-107">Ein Bitfeld, das die Typen von Anforderungen angibt, die beendet (und aus der Warteschlange des Zeichens entfernt) werden sollen, bestehend aus folgendem:</span><span class="sxs-lookup"><span data-stu-id="08b46-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b46-108">konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ alle = 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="08b46-108">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="08b46-109">Beendet alle Animations Anforderungen, einschließlich der nicht in die Warteschlange eingereihten [**Vorbereitungs**](iagentcharacter--prepare.md) Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="08b46-109">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="08b46-110">**Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ Play = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="08b46-110">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="08b46-111">Beendet alle Wiedergabe Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="08b46-111">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="08b46-112">**Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ Move = 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="08b46-112">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="08b46-113">Beendet alle [](https://www.bing.com/search?q=**Move**) Verschiebungs Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="08b46-113">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="08b46-114">konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ sprechen = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="08b46-114">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="08b46-115">Beendet alle [**sprach**](iagentcharacter--speak.md) Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="08b46-115">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="08b46-116">konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ Prepare = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="08b46-116">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="08b46-117">Beendet alle [**Vorbereitungs**](iagentcharacter--prepare.md) Anforderungen in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="08b46-117">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="08b46-118">konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ nonqueuedprepare = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="08b46-118">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="08b46-119">Beendet alle [**Vorbereitungs**](iagentcharacter--prepare.md) Anforderungen, die nicht in der Warteschlange stehen.</span><span class="sxs-lookup"><span data-stu-id="08b46-119">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="08b46-120">konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp ist \_ sichtbar = 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="08b46-120">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="08b46-121">Beendet alle Anforderungen zum [**Ausblenden**](iagentcharacter--hide.md) oder [**anzeigen**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="08b46-121">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="08b46-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="08b46-122">See Also</span></span>

[<span data-ttu-id="08b46-123">**Iagentcharacter:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="08b46-123">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





