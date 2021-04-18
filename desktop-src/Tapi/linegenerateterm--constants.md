---
description: Die linegenerateterm \_ -bitflagkonstanten beschreiben die Bedingungen, unter denen die Ziffern-oder Tongenerierung beendet wird.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: LINEGENERATETERM_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371563"
---
# <a name="linegenerateterm_-constants"></a><span data-ttu-id="0fb2a-103">Linegenerateterm- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="0fb2a-103">LINEGENERATETERM\_ Constants</span></span>

<span data-ttu-id="0fb2a-104">Die **linegenerateterm \_** -bitflagkonstanten beschreiben die Bedingungen, unter denen die Ziffern-oder Tongenerierung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fb2a-104">The **LINEGENERATETERM\_** bit-flag constants describe the conditions under which digit or tone generation is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="0fb2a-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**linegenerateterm \_ Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="0fb2a-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0fb2a-106">Die Digit-oder Tone-Generierungs Anforderung wurde von dieser Anwendung, von einer anderen Anwendung oder von der Beendigung des Aufrufes abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="0fb2a-106">The digit or tone generation request was canceled by this application, by another application, or because the call terminated.</span></span> <span data-ttu-id="0fb2a-107">Dieser Wert kann auch zurückgegeben werden, wenn die Ziffern-oder Tongenerierung aufgrund eines internen Fehlers des Dienstanbieters nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fb2a-107">This value can also be returned when digit or tone generation cannot be completed due to internal failure of the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0fb2a-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**linegenerateterm \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="0fb2a-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM\_DONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0fb2a-109">Die angeforderte Anzahl von Ziffern oder angeforderten Tönen wurde für die angeforderte Dauer generiert.</span><span class="sxs-lookup"><span data-stu-id="0fb2a-109">The requested number of digits or requested tones have been generated for the requested duration.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fb2a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fb2a-110">Remarks</span></span>

<span data-ttu-id="0fb2a-111">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="0fb2a-111">No extensibility.</span></span> <span data-ttu-id="0fb2a-112">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="0fb2a-112">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb2a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fb2a-113">Requirements</span></span>



| <span data-ttu-id="0fb2a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fb2a-114">Requirement</span></span> | <span data-ttu-id="0fb2a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0fb2a-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0fb2a-116">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0fb2a-116">TAPI version</span></span><br/> | <span data-ttu-id="0fb2a-117">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0fb2a-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0fb2a-118">Header</span><span class="sxs-lookup"><span data-stu-id="0fb2a-118">Header</span></span><br/>       | <dl> <span data-ttu-id="0fb2a-119"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb2a-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




