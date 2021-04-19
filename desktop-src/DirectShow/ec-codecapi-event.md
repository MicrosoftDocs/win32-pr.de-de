---
description: 'Das EC \_ codecapi- \_ Ereignis Ereignis wird von einem Encoder gesendet, um ein Codierungs Ereignis zu signalisieren. Der Client registriert sich für das encoderereignis, indem er die icodecapi:: RegisterForEvent-Methode aufrufen.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372075"
---
# <a name="ec_codecapi_event"></a><span data-ttu-id="e7620-104">EC \_ codecapi- \_ Ereignis</span><span class="sxs-lookup"><span data-stu-id="e7620-104">EC\_CODECAPI\_EVENT</span></span>

<span data-ttu-id="e7620-105">Das EC \_ codecapi- \_ Ereignis Ereignis wird von einem Encoder gesendet, um ein Codierungs Ereignis zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="e7620-105">The EC\_CODECAPI\_EVENT event is sent by an encoder to signal an encoding event.</span></span> <span data-ttu-id="e7620-106">Der Client registriert sich für das encoderereignis, indem er die [**icodecapi:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7620-106">The client registers for encoder event by calling the [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7620-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7620-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7620-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e7620-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e7620-109">Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="e7620-109">User data.</span></span> <span data-ttu-id="e7620-110">Der Wert dieses Parameters ist der Zeiger, den der Aufrufer im *UserData* -Parameter der [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) -Methode angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e7620-110">The value of this parameter is the pointer that the caller specified in the *userData* parameter of the [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

</dd> <dt>

<span data-ttu-id="e7620-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e7620-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e7620-112">Ein Zeiger auf die Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e7620-112">Pointer to the event data.</span></span> <span data-ttu-id="e7620-113">Diese Daten werden vom Encoder zugeordnet und müssen von der Anwendung freigegeben werden, indem die **CoTaskMemFree** -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7620-113">This data is allocated by the encoder and must be freed by the application, using the **CoTaskMemFree** function.</span></span> <span data-ttu-id="e7620-114">Der Datenblock beginnt mit einer [**codecapieventdata**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) -Struktur. Wandeln Sie den *lParam2* -Parameter in einen Zeiger auf diese-Struktur um.</span><span class="sxs-lookup"><span data-stu-id="e7620-114">The data block starts with a [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) structure; cast the *lParam2* parameter to a pointer to this structure.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e7620-115">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="e7620-115">Default Action</span></span>

<span data-ttu-id="e7620-116">Keine Standardaktion.</span><span class="sxs-lookup"><span data-stu-id="e7620-116">No default action.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7620-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7620-117">Requirements</span></span>



| <span data-ttu-id="e7620-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7620-118">Requirement</span></span> | <span data-ttu-id="e7620-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e7620-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7620-120">Header</span><span class="sxs-lookup"><span data-stu-id="e7620-120">Header</span></span><br/> | <dl> <span data-ttu-id="e7620-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7620-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7620-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7620-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7620-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="e7620-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e7620-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e7620-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




