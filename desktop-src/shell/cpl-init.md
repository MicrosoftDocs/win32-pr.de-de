---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, um Sie zur Ausführung einer globalen Initialisierung aufzufordern, insbesondere für die Speicher Belegung.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: CPL_INIT Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977353"
---
# <a name="cpl_init-message"></a><span data-ttu-id="ab40c-103">CPL- \_ Init-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ab40c-103">CPL\_INIT message</span></span>

<span data-ttu-id="ab40c-104">Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, um Sie zur Ausführung einer globalen Initialisierung aufzufordern, insbesondere für die Speicher Belegung.</span><span class="sxs-lookup"><span data-stu-id="ab40c-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to prompt it to perform global initialization, especially memory allocation.</span></span>


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a><span data-ttu-id="ab40c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab40c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab40c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab40c-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ab40c-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ab40c-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ab40c-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab40c-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ab40c-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ab40c-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab40c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab40c-110">Return value</span></span>

<span data-ttu-id="ab40c-111">Wenn die Initialisierung erfolgreich ist, sollte die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion ungleich 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ab40c-111">If initialization succeeds, the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function should return nonzero.</span></span> <span data-ttu-id="ab40c-112">Andernfalls sollte NULL zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ab40c-112">Otherwise, it should return zero.</span></span>

<span data-ttu-id="ab40c-113">Wenn [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) NULL zurückgibt, beendet die steuernde Anwendung die Kommunikation und gibt die dll frei, die die System Steuerungsanwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="ab40c-113">If [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) returns zero, the controlling application ends communication and releases the DLL containing the Control Panel application.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab40c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab40c-114">Remarks</span></span>

<span data-ttu-id="ab40c-115">Da dies die einzige Möglichkeit ist, dass eine System Steuerungsanwendung einen Fehlerzustand signalisieren kann, sollte die Anwendung Arbeitsspeicher als Reaktion auf diese Nachricht zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ab40c-115">Because this is the only way a Control Panel application can signal an error condition, the application should allocate memory in response to this message.</span></span>

<span data-ttu-id="ab40c-116">Diese Nachricht wird unmittelbar nach dem Laden der dll, die die Anwendung enthält, gesendet.</span><span class="sxs-lookup"><span data-stu-id="ab40c-116">This message is sent immediately after the DLL containing the application is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab40c-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ab40c-117">Requirements</span></span>



| <span data-ttu-id="ab40c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab40c-118">Requirement</span></span> | <span data-ttu-id="ab40c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ab40c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab40c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab40c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab40c-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab40c-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ab40c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab40c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab40c-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab40c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab40c-124">Header</span><span class="sxs-lookup"><span data-stu-id="ab40c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab40c-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab40c-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab40c-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab40c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab40c-127">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="ab40c-127">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
