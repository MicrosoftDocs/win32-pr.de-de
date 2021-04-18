---
description: Die bitflagkonstanten von linegatherterm \_ beschreiben die Bedingungen, unter denen die pufferte Ziffern Erfassung beendet wird.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: LINEGATHERTERM_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354830"
---
# <a name="linegatherterm_-constants"></a><span data-ttu-id="0ece1-103">Linegatherterm- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="0ece1-103">LINEGATHERTERM\_ Constants</span></span>

<span data-ttu-id="0ece1-104">Die bitflagkonstanten von **linegatherterm \_** beschreiben die Bedingungen, unter denen die pufferte Ziffern Erfassung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ece1-104">The **LINEGATHERTERM\_** bit-flag constants describe the conditions under which buffered digit gathering is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="0ece1-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**linegatherterm \_ bufferfull**</span><span class="sxs-lookup"><span data-stu-id="0ece1-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM\_BUFFERFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ece1-106">Die angeforderte Anzahl von Ziffern wurde gesammelt.</span><span class="sxs-lookup"><span data-stu-id="0ece1-106">The requested number of digits has been gathered.</span></span> <span data-ttu-id="0ece1-107">Der Puffer ist voll.</span><span class="sxs-lookup"><span data-stu-id="0ece1-107">The buffer is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ece1-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**linegatherterm \_ Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="0ece1-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ece1-109">Die Anforderung wurde von dieser Anwendung, von einer anderen Anwendung oder von der Beendigung des Aufrufes abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="0ece1-109">The request was canceled by this application, by another application, or because the call terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ece1-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**linegatherterm \_ firsttimeout**</span><span class="sxs-lookup"><span data-stu-id="0ece1-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM\_FIRSTTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ece1-111">Das erste Ziffern Timeout ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="0ece1-111">The first digit timeout expired.</span></span> <span data-ttu-id="0ece1-112">Der Puffer enthält keine Ziffern.</span><span class="sxs-lookup"><span data-stu-id="0ece1-112">The buffer contains no digits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ece1-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**linegatherterm- \_ intertimeout**</span><span class="sxs-lookup"><span data-stu-id="0ece1-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM\_INTERTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ece1-114">Das zwischen Ziffern Timeout ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="0ece1-114">The inter-digit timeout expired.</span></span> <span data-ttu-id="0ece1-115">Der Puffer enthält mindestens eine Ziffer.</span><span class="sxs-lookup"><span data-stu-id="0ece1-115">The buffer contains at least one digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ece1-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**linegatherterm \_ termdigit**</span><span class="sxs-lookup"><span data-stu-id="0ece1-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM\_TERMDIGIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ece1-117">Eine der Beendigungs Ziffern entsprach einer empfangenen Ziffer.</span><span class="sxs-lookup"><span data-stu-id="0ece1-117">One of the termination digits matched a received digit.</span></span> <span data-ttu-id="0ece1-118">Die übereinstimmende Abbruch Ziffer ist die letzte Ziffer im Puffer.</span><span class="sxs-lookup"><span data-stu-id="0ece1-118">The matched termination digit is the last digit in the buffer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ece1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ece1-119">Remarks</span></span>

<span data-ttu-id="0ece1-120">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="0ece1-120">No extensibility.</span></span> <span data-ttu-id="0ece1-121">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="0ece1-121">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ece1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ece1-122">Requirements</span></span>



| <span data-ttu-id="0ece1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ece1-123">Requirement</span></span> | <span data-ttu-id="0ece1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0ece1-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0ece1-125">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0ece1-125">TAPI version</span></span><br/> | <span data-ttu-id="0ece1-126">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0ece1-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0ece1-127">Header</span><span class="sxs-lookup"><span data-stu-id="0ece1-127">Header</span></span><br/>       | <dl> <span data-ttu-id="0ece1-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ece1-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




