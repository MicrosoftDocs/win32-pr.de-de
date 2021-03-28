---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, wenn der Benutzer auf das Symbol eines Dialog Felds doppelklickt, das von der Anwendung unterstützt wird.
title: CPL_DBLCLK Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993726"
---
# <a name="cpl_dblclk-message"></a><span data-ttu-id="84082-103">CPL- \_ dblclk-Meldung</span><span class="sxs-lookup"><span data-stu-id="84082-103">CPL\_DBLCLK message</span></span>

<span data-ttu-id="84082-104">Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, wenn der Benutzer auf das Symbol eines Dialog Felds doppelklickt, das von der Anwendung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="84082-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the user double-clicks the icon of a dialog box supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="84082-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="84082-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84082-106">*uappnum*</span><span class="sxs-lookup"><span data-stu-id="84082-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="84082-107">Die Dialogfeld Nummer.</span><span class="sxs-lookup"><span data-stu-id="84082-107">The dialog box number.</span></span> <span data-ttu-id="84082-108">Diese Zahl muss zwischen null und einem Wert liegen, der als Antwort auf die [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht (CPL \_ GetCount – 1) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="84082-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="84082-109">*ldata*</span><span class="sxs-lookup"><span data-stu-id="84082-109">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="84082-110">Der Wert, der von der System Steuerungsanwendung in den **lpdata** -Member der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur für das Dialogfeld geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="84082-110">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="84082-111">Die Anwendung lädt den **lpdata** -Member als Antwort auf die CPL-Nachrichten-oder- [**cpl \_**](cpl-newinquire.md) -Nachricht. [**\_**](cpl-inquire.md)</span><span class="sxs-lookup"><span data-stu-id="84082-111">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84082-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84082-112">Return value</span></span>

<span data-ttu-id="84082-113">Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, ist der Rückgabewert 0 (null). Andernfalls ist der Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="84082-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, the return value is zero; otherwise, it is nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="84082-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84082-114">Remarks</span></span>

<span data-ttu-id="84082-115">Als Antwort auf diese Nachricht muss eine System Steuerungsanwendung das entsprechende Dialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="84082-115">In response to this message, a Control Panel application must display the corresponding dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="84082-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="84082-116">Requirements</span></span>



| <span data-ttu-id="84082-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84082-117">Requirement</span></span> | <span data-ttu-id="84082-118">Wert</span><span class="sxs-lookup"><span data-stu-id="84082-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84082-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84082-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84082-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84082-120">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="84082-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84082-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84082-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84082-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84082-123">Header</span><span class="sxs-lookup"><span data-stu-id="84082-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="84082-124"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="84082-124"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84082-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="84082-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84082-126">**CPL- \_ Auswahl**</span><span class="sxs-lookup"><span data-stu-id="84082-126">**CPL\_SELECT**</span></span>](cpl-select.md)
</dt> </dl>

 

 
