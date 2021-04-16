---
title: WINBIO_EVENT Konstanten (winbio \_ types. h)
description: Geben Sie die zu überwachenden Ereignis Benachrichtigungs Typen für Dienstanbieter an.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517474"
---
# <a name="winbio_event-constants"></a><span data-ttu-id="4089a-103">Winbio- \_ Ereignis Konstanten</span><span class="sxs-lookup"><span data-stu-id="4089a-103">WINBIO\_EVENT Constants</span></span>

<span data-ttu-id="4089a-104">Die folgenden Konstanten können in der [**winbioregistereventmonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) -Funktion verwendet werden, um die Typen der zu überwachenden Ereignis Benachrichtigungen für den Dienstanbieter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4089a-104">The following constants can be used in the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to specify the types of service provider event notifications to monitor.</span></span>



| <span data-ttu-id="4089a-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="4089a-105">Constant</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="4089a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4089a-106">Description</span></span>                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <span data-ttu-id="4089a-107"><dt>**winbio- \_ Ereignis \_ FP \_ nicht beansprucht**</dt></span><span class="sxs-lookup"><span data-stu-id="4089a-107"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED**</dt></span></span> </dl>                             | <span data-ttu-id="4089a-108">Der Sensor hat einen Fingerring erkannt, der nicht von der Anwendung angefordert wurde, oder das Fenster, das gerade den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="4089a-108">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="4089a-109">Der Windows-Biometrieframework Ruft die Rückruffunktion auf, um anzugeben, dass ein Finger schwenken aufgetreten ist, aber nicht versucht, den Fingerabdruck zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4089a-109">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.</span></span><br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <span data-ttu-id="4089a-110"><dt>**winbio- \_ Ereignis \_ FP \_ nicht beansprucht- \_ Identifizierung**</dt></span><span class="sxs-lookup"><span data-stu-id="4089a-110"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY**</dt></span></span> </dl> | <span data-ttu-id="4089a-111">Der Sensor hat einen Fingerring erkannt, der nicht von der Anwendung angefordert wurde, oder das Fenster, das gerade den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="4089a-111">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="4089a-112">Der Windows-Biometrieframework versucht, den Fingerabdruck zu identifizieren, und übergibt das Ergebnis dieses Prozesses an Ihre Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="4089a-112">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="4089a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4089a-113">Requirements</span></span>



| <span data-ttu-id="4089a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4089a-114">Requirement</span></span> | <span data-ttu-id="4089a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4089a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4089a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4089a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4089a-117">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4089a-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4089a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4089a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4089a-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4089a-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4089a-120">Header</span><span class="sxs-lookup"><span data-stu-id="4089a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4089a-121"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4089a-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4089a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4089a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4089a-123">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="4089a-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





