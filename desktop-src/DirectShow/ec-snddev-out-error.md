---
description: Ein Gerätefehler ist in einem audiorendererfilter aufgetreten.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1182aaba7bb30ad27511b47ba8e4432d8fd33da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373952"
---
# <a name="ec_snddev_out_error"></a><span data-ttu-id="b5057-103">EC \_ snddev \_ out- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="b5057-103">EC\_SNDDEV\_OUT\_ERROR</span></span>

<span data-ttu-id="b5057-104">Ein Gerätefehler ist in einem audiorendererfilter aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b5057-104">A device error has occurred in an audio renderer filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5057-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5057-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5057-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b5057-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b5057-107">DWORD-Wert aus dem " [**snddev \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) "-enumerierten Typ, der angibt, wie auf das Gerät zugegriffen wurde, als der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b5057-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b5057-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b5057-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b5057-109">DWORD-Wert, der den Fehler angibt, der vom Sound-Geräte Rückruf zurückgegeben wurde</span><span class="sxs-lookup"><span data-stu-id="b5057-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b5057-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="b5057-110">Default Action</span></span>

<span data-ttu-id="b5057-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5057-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5057-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5057-112">Requirements</span></span>



| <span data-ttu-id="b5057-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5057-113">Requirement</span></span> | <span data-ttu-id="b5057-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b5057-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5057-115">Header</span><span class="sxs-lookup"><span data-stu-id="b5057-115">Header</span></span><br/> | <dl> <span data-ttu-id="b5057-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5057-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5057-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5057-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5057-118">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="b5057-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b5057-119">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b5057-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




