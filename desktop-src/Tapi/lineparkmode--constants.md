---
description: Die \_ Bit-Flag-Konstanten von linepark Mode beschreiben verschiedene Arten von Park aufrufen.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: LINEPARKMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361632"
---
# <a name="lineparkmode_-constants"></a><span data-ttu-id="bf6be-103">Lineparkmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="bf6be-103">LINEPARKMODE\_ Constants</span></span>

<span data-ttu-id="bf6be-104">Die Bit-Flag-Konstanten von **linepark Mode \_** beschreiben verschiedene Arten von Park aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bf6be-104">The **LINEPARKMODE\_** bit-flag constants describe different ways of parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="bf6be-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**lineparkmode \_ gerichtet**</span><span class="sxs-lookup"><span data-stu-id="bf6be-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE\_DIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf6be-106">Gibt den gerichteten callpark an.</span><span class="sxs-lookup"><span data-stu-id="bf6be-106">Specifies directed call park.</span></span> <span data-ttu-id="bf6be-107">Die Adresse, in der der-Befehl geparkt werden soll, muss für den Schalter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bf6be-107">The address where the call is to be parked must be supplied to the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf6be-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**lineparkmode \_ nicht gesteuert**</span><span class="sxs-lookup"><span data-stu-id="bf6be-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE\_NONDIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf6be-109">Gibt den nicht gesteuerten callpark an.</span><span class="sxs-lookup"><span data-stu-id="bf6be-109">Specifies nondirected call park.</span></span> <span data-ttu-id="bf6be-110">Die Adresse, in der der-Befehl geparkt ist, wird durch den-Schalter ausgewählt und vom Switch zur Anwendung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bf6be-110">The address where the call is parked is selected by the switch and provided by the switch to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf6be-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf6be-111">Remarks</span></span>

<span data-ttu-id="bf6be-112">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="bf6be-112">No extensibility.</span></span> <span data-ttu-id="bf6be-113">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="bf6be-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="bf6be-114">Die **lineparkmode- \_ Konstanten** werden verwendet, wenn ein-Befehl durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="bf6be-114">The **LINEPARKMODE\_ constants** are used when parking a call.</span></span> <span data-ttu-id="bf6be-115">Sehen Sie sich die Gerätefunktionen einer Zeile an, um herauszufinden, welcher Park Modus verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bf6be-115">Consult a line's address device capabilities to find out which park mode is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf6be-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf6be-116">Requirements</span></span>



| <span data-ttu-id="bf6be-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf6be-117">Requirement</span></span> | <span data-ttu-id="bf6be-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bf6be-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bf6be-119">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="bf6be-119">TAPI version</span></span><br/> | <span data-ttu-id="bf6be-120">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bf6be-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="bf6be-121">Header</span><span class="sxs-lookup"><span data-stu-id="bf6be-121">Header</span></span><br/>       | <dl> <span data-ttu-id="bf6be-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf6be-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




