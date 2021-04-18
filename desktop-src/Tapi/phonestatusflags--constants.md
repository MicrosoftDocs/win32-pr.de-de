---
description: Die \_ Bit-Flag-Konstanten von phonestatusflags beschreiben eine Vielzahl von Telefongeräte Statusinformationen.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: PHONESTATUSFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359287"
---
# <a name="phonestatusflags_-constants"></a><span data-ttu-id="187bb-103">Phonestatus-Flags- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="187bb-103">PHONESTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="187bb-104">Die Bit-Flag-Konstanten von **phonestatusflags \_** beschreiben eine Vielzahl von Telefongeräte Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="187bb-104">The **PHONESTATUSFLAGS\_** bit-flag constants describe a variety of phone device status information.</span></span>

<dl> <dt>

<span data-ttu-id="187bb-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**Verbindung mit phonestatus-Flags \_**</span><span class="sxs-lookup"><span data-stu-id="187bb-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="187bb-106">Gibt an, ob das Telefon derzeit mit TAPI verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="187bb-106">Specifies whether the phone is currently connected to TAPI.</span></span> <span data-ttu-id="187bb-107">**True** , wenn eine Verbindung hergestellt wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="187bb-107">**TRUE** if connected, **FALSE** otherwise.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="187bb-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**phonestatus \_ -Flags angehalten**</span><span class="sxs-lookup"><span data-stu-id="187bb-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="187bb-109">Gibt an, ob TAPI das Telefongerät bearbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="187bb-109">Specifies whether TAPI's manipulation of the phone device is suspended.</span></span> <span data-ttu-id="187bb-110">**True** , wenn angehalten, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="187bb-110">**TRUE** if suspended, **FALSE** otherwise.</span></span> <span data-ttu-id="187bb-111">Die Verwendung eines Telefon Geräts für eine Anwendung kann vorübergehend angehalten werden, wenn der Switch das Telefon auf eine Weise ändern möchte, die keine Störungen der Anwendung tolerieren kann.</span><span class="sxs-lookup"><span data-stu-id="187bb-111">An application's use of a phone device can be temporarily suspended when the switch wants to manipulate the phone in a way that cannot tolerate interference from the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="187bb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="187bb-112">Remarks</span></span>

<span data-ttu-id="187bb-113">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="187bb-113">No extensibility.</span></span> <span data-ttu-id="187bb-114">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="187bb-114">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="187bb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="187bb-115">Requirements</span></span>



| <span data-ttu-id="187bb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="187bb-116">Requirement</span></span> | <span data-ttu-id="187bb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="187bb-117">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="187bb-118">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="187bb-118">TAPI version</span></span><br/> | <span data-ttu-id="187bb-119">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="187bb-119">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="187bb-120">Header</span><span class="sxs-lookup"><span data-stu-id="187bb-120">Header</span></span><br/>       | <dl> <span data-ttu-id="187bb-121"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="187bb-121"><dt>Tapi.h</dt></span></span> </dl> |



 

 




