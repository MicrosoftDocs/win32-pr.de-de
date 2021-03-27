---
description: Wird einmal an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, bevor die DLL mit der System Steuerungsanwendung freigegeben wird.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: CPL_EXIT Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214435"
---
# <a name="cpl_exit-message"></a><span data-ttu-id="988a5-103">CPL-Beendigungs \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="988a5-103">CPL\_EXIT message</span></span>

<span data-ttu-id="988a5-104">Wird einmal an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, bevor die DLL mit der System Steuerungsanwendung freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="988a5-104">Sent once to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application before the DLL containing the Control Panel application is released.</span></span>

## <a name="parameters"></a><span data-ttu-id="988a5-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="988a5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="988a5-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="988a5-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="988a5-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="988a5-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="988a5-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="988a5-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="988a5-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="988a5-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="988a5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="988a5-110">Return value</span></span>

<span data-ttu-id="988a5-111">Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="988a5-111">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="988a5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="988a5-112">Remarks</span></span>

<span data-ttu-id="988a5-113">Diese Meldung wird gesendet, nachdem die letzte Nachricht zum [**\_ Anhalten der CPL**](cpl-stop.md) gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="988a5-113">This message is sent after the last [**CPL\_STOP**](cpl-stop.md) message is sent.</span></span>

<span data-ttu-id="988a5-114">Als Antwort auf diese Nachricht muss eine System Steuerungsanwendung jeglichen zugeordneten Arbeitsspeicher freigeben und Cleanup auf globaler Ebene durchführen.</span><span class="sxs-lookup"><span data-stu-id="988a5-114">In response to this message, a Control Panel application must free any memory that it has allocated and perform global-level cleanup.</span></span>

## <a name="requirements"></a><span data-ttu-id="988a5-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="988a5-115">Requirements</span></span>



| <span data-ttu-id="988a5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="988a5-116">Requirement</span></span> | <span data-ttu-id="988a5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="988a5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="988a5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="988a5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="988a5-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="988a5-119">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="988a5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="988a5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="988a5-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="988a5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="988a5-122">Header</span><span class="sxs-lookup"><span data-stu-id="988a5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="988a5-123"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="988a5-123"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="988a5-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="988a5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="988a5-125">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="988a5-125">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
