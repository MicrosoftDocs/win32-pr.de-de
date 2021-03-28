---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, wenn die Steuerungsanwendung der Systemsteuerung geschlossen wird. Die steuernde Anwendung sendet die Nachricht einmal für jedes Dialogfeld, das von der Anwendung unterstützt wird.
title: CPL_STOP Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977337"
---
# <a name="cpl_stop-message"></a><span data-ttu-id="8be4f-104">CPL- \_ Stoppmeldung</span><span class="sxs-lookup"><span data-stu-id="8be4f-104">CPL\_STOP message</span></span>

<span data-ttu-id="8be4f-105">Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, wenn die Steuerungsanwendung der Systemsteuerung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="8be4f-105">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the controlling application of the Control Panel closes.</span></span> <span data-ttu-id="8be4f-106">Die steuernde Anwendung sendet die Nachricht einmal für jedes Dialogfeld, das von der Anwendung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8be4f-106">The controlling application sends the message once for each dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="8be4f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8be4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be4f-108">*uappnum*</span><span class="sxs-lookup"><span data-stu-id="8be4f-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="8be4f-109">Die Dialogfeld Nummer.</span><span class="sxs-lookup"><span data-stu-id="8be4f-109">The dialog box number.</span></span>

</dd> <dt>

<span data-ttu-id="8be4f-110">*ldata*</span><span class="sxs-lookup"><span data-stu-id="8be4f-110">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="8be4f-111">Der Wert, der von der System Steuerungsanwendung in den **lpdata** -Member der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur für das Dialogfeld geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="8be4f-111">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="8be4f-112">Die Anwendung lädt den **lpdata** -Member als Antwort auf die CPL-Nachrichten-oder- [**cpl \_**](cpl-newinquire.md) -Nachricht. [**\_**](cpl-inquire.md)</span><span class="sxs-lookup"><span data-stu-id="8be4f-112">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be4f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8be4f-113">Return value</span></span>

<span data-ttu-id="8be4f-114">Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8be4f-114">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8be4f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8be4f-115">Remarks</span></span>

<span data-ttu-id="8be4f-116">Als Antwort auf diese Nachricht muss eine System Steuerungsanwendung für das angegebene Dialogfeld Eine Bereinigung durchführen.</span><span class="sxs-lookup"><span data-stu-id="8be4f-116">In response to this message, a Control Panel application must perform cleanup for the given dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be4f-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8be4f-117">Requirements</span></span>



| <span data-ttu-id="8be4f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8be4f-118">Requirement</span></span> | <span data-ttu-id="8be4f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8be4f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8be4f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8be4f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8be4f-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8be4f-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8be4f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8be4f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8be4f-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8be4f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8be4f-124">Header</span><span class="sxs-lookup"><span data-stu-id="8be4f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8be4f-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8be4f-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be4f-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8be4f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be4f-127">**CPL- \_ Exit**</span><span class="sxs-lookup"><span data-stu-id="8be4f-127">**CPL\_EXIT**</span></span>](cpl-exit.md)
</dt> <dt>

[<span data-ttu-id="8be4f-128">**CPL- \_ GetCount**</span><span class="sxs-lookup"><span data-stu-id="8be4f-128">**CPL\_GETCOUNT**</span></span>](cpl-getcount.md)
</dt> </dl>

 

 
