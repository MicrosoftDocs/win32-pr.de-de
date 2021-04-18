---
description: Die \_ Bit-Flag-Konstanten von linetransfermode beschreiben verschiedene Methoden zum Auflösen von Anforderungen zum Aufrufen von Anforderungen.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: LINETRANSFERMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357957"
---
# <a name="linetransfermode_-constants"></a><span data-ttu-id="bbd0a-103">Linetransfermode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="bbd0a-103">LINETRANSFERMODE\_ Constants</span></span>

<span data-ttu-id="bbd0a-104">Die Bit-Flag-Konstanten von **linetransfermode \_** beschreiben verschiedene Methoden zum Auflösen von Anforderungen zum Aufrufen von Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="bbd0a-104">The **LINETRANSFERMODE\_** bit-flag constants describe different ways of resolving call transfer requests.</span></span>

<dl> <dt>

<span data-ttu-id="bbd0a-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**linetransfermode- \_ Konferenz**</span><span class="sxs-lookup"><span data-stu-id="bbd0a-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bbd0a-106">Die Übertragung erfolgt durch das Einrichten einer drei-Wege-Konferenz zwischen der Anwendung, der mit dem ersten-Befehl verbundenen Partei und der mit dem Beratungsgespräch verbundenen Partei.</span><span class="sxs-lookup"><span data-stu-id="bbd0a-106">The transfer is resolved by establishing a three-way conference between the application, the party connected to the initial call, and the party connected to the consultation call.</span></span> <span data-ttu-id="bbd0a-107">Wenn diese Option ausgewählt ist, wird ein Konferenzgespräch erstellt.</span><span class="sxs-lookup"><span data-stu-id="bbd0a-107">A conference call is created when this option is selected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bbd0a-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**linetransfermode- \_ Übertragung**</span><span class="sxs-lookup"><span data-stu-id="bbd0a-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bbd0a-109">Die Übertragung wird durch übertragen des ersten Aufrufes auf den-Rückruf aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="bbd0a-109">The transfer is resolved by transferring the initial call to the consultation call.</span></span> <span data-ttu-id="bbd0a-110">Beide Aufrufe werden in den Leerlauf der Anwendung versetzt.</span><span class="sxs-lookup"><span data-stu-id="bbd0a-110">Both calls will become idle to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbd0a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbd0a-111">Remarks</span></span>

<span data-ttu-id="bbd0a-112">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="bbd0a-112">No extensibility.</span></span> <span data-ttu-id="bbd0a-113">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="bbd0a-113">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd0a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbd0a-114">Requirements</span></span>



| <span data-ttu-id="bbd0a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbd0a-115">Requirement</span></span> | <span data-ttu-id="bbd0a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="bbd0a-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bbd0a-117">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="bbd0a-117">TAPI version</span></span><br/> | <span data-ttu-id="bbd0a-118">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bbd0a-118">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="bbd0a-119">Header</span><span class="sxs-lookup"><span data-stu-id="bbd0a-119">Header</span></span><br/>       | <dl> <span data-ttu-id="bbd0a-120"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbd0a-120"><dt>Tapi.h</dt></span></span> </dl> |



 

 




