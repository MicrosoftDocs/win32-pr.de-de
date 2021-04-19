---
description: Signalisiert, dass ein DVD-Navigator-Befehl begonnen hat.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0fb723b220bf8aa12baa7133c9985225d6051921
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360298"
---
# <a name="ec_dvd_cmd_start"></a><span data-ttu-id="bcc0f-103">Start der EC- \_ DVD- \_ cmd \_</span><span class="sxs-lookup"><span data-stu-id="bcc0f-103">EC\_DVD\_CMD\_START</span></span>

<span data-ttu-id="bcc0f-104">Signalisiert, dass ein [DVD-Navigator](dvd-navigator-filter.md) -Befehl begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="bcc0f-104">Signals that a [DVD Navigator](dvd-navigator-filter.md) command has begun.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcc0f-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcc0f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc0f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="bcc0f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bcc0f-107">Befehls Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="bcc0f-107">Command identifier.</span></span> <span data-ttu-id="bcc0f-108">Übergeben Sie diesen Parameter an die [**IDvdInfo2:: getcmdfromevent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) -Methode, um einen [**idvdcmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) -Schnittstellen Zeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bcc0f-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="bcc0f-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bcc0f-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bcc0f-110">**HRESULT** -Wert, der den Status des Befehls angibt.</span><span class="sxs-lookup"><span data-stu-id="bcc0f-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcc0f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcc0f-111">Remarks</span></span>

<span data-ttu-id="bcc0f-112">Dieses Ereignis wird nur ausgelöst, wenn die Anwendung das **Flag \_ \_ \_ sendevents für das DVD-cmd-Flag** in einer [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Methode festlegt, die ein [**DVD- \_ cmd- \_ Flags**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) -Flag annimmt.</span><span class="sxs-lookup"><span data-stu-id="bcc0f-112">This event is only fired if your application sets the **DVD\_CMD\_FLAG\_SendEvents** flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="bcc0f-113">Dieses Ereignis wird in der Titel Domäne ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="bcc0f-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc0f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcc0f-114">Requirements</span></span>



| <span data-ttu-id="bcc0f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcc0f-115">Requirement</span></span> | <span data-ttu-id="bcc0f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="bcc0f-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc0f-117">Header</span><span class="sxs-lookup"><span data-stu-id="bcc0f-117">Header</span></span><br/> | <dl> <span data-ttu-id="bcc0f-118"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcc0f-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc0f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcc0f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc0f-120">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bcc0f-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="bcc0f-121">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="bcc0f-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bcc0f-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="bcc0f-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="bcc0f-123">Synchronisieren von DVD-Befehlen</span><span class="sxs-lookup"><span data-stu-id="bcc0f-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




