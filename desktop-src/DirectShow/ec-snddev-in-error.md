---
description: Ein Gerätefehler ist in einem audioerfassungs Filter aufgetreten.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352092"
---
# <a name="ec_snddev_in_error"></a><span data-ttu-id="f50cd-103">\_Fehler bei EC snddev. \_ \_</span><span class="sxs-lookup"><span data-stu-id="f50cd-103">EC\_SNDDEV\_IN\_ERROR</span></span>

<span data-ttu-id="f50cd-104">Ein Gerätefehler ist in einem audioerfassungs Filter aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f50cd-104">A device error has occurred in an audio capture filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="f50cd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f50cd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f50cd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f50cd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f50cd-107">DWORD-Wert aus dem " [**snddev \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) "-enumerierten Typ, der angibt, wie auf das Gerät zugegriffen wurde, als der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f50cd-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f50cd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f50cd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f50cd-109">DWORD-Wert, der den Fehler angibt, der vom Sound-Geräte Rückruf zurückgegeben wurde</span><span class="sxs-lookup"><span data-stu-id="f50cd-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="f50cd-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="f50cd-110">Default Action</span></span>

<span data-ttu-id="f50cd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f50cd-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f50cd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f50cd-112">Requirements</span></span>



| <span data-ttu-id="f50cd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f50cd-113">Requirement</span></span> | <span data-ttu-id="f50cd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f50cd-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f50cd-115">Header</span><span class="sxs-lookup"><span data-stu-id="f50cd-115">Header</span></span><br/> | <dl> <span data-ttu-id="f50cd-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="f50cd-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f50cd-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f50cd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f50cd-118">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="f50cd-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f50cd-119">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f50cd-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




