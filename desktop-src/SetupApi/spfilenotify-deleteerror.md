---
description: Die spfilenotify \_ deleteerror-Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Löschvorgangs ein Fehler auftritt.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: SPFILENOTIFY_DELETEERROR Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050520"
---
# <a name="spfilenotify_deleteerror-message"></a><span data-ttu-id="9af22-103">Spfilenotify \_ deleteerror-Meldung</span><span class="sxs-lookup"><span data-stu-id="9af22-103">SPFILENOTIFY\_DELETEERROR message</span></span>

<span data-ttu-id="9af22-104">Die **spfilenotify \_ deleteerror** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Löschvorgangs ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="9af22-104">The **SPFILENOTIFY\_DELETEERROR** notification is sent to the callback routine if an error occurs during a file delete operation.</span></span>


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="9af22-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9af22-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af22-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="9af22-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="9af22-107">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9af22-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9af22-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="9af22-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="9af22-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9af22-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af22-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9af22-110">Return value</span></span>

<span data-ttu-id="9af22-111">Die Rückruf Routine muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9af22-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="9af22-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9af22-112">Return code</span></span>                                                                                  | <span data-ttu-id="9af22-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9af22-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9af22-114"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="9af22-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="9af22-115">Die Warteschlangen Verarbeitung sollte abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="9af22-115">Queue processing should be canceled.</span></span> <span data-ttu-id="9af22-116">[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt 0 (null) zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt erweiterte Fehlerinformationen zurück, wie z. b. \_ den Fehler abgebrochen (wenn der Benutzer abgebrochen hat) oder einen Fehler \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9af22-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="9af22-117"><dt>**fileOp- \_ Wiederholung**</dt></span><span class="sxs-lookup"><span data-stu-id="9af22-117"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="9af22-118">Der Benutzer versucht erneut, den Löschvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9af22-118">The user is attempting the delete operation again.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="9af22-119"><dt>**fileOp-über \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="9af22-119"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="9af22-120">Der Benutzer wird den Datei Löschvorgang übersprungen.</span><span class="sxs-lookup"><span data-stu-id="9af22-120">The user is skipping the file delete operation.</span></span><br/>                                                                                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="9af22-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9af22-121">Requirements</span></span>



| <span data-ttu-id="9af22-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9af22-122">Requirement</span></span> | <span data-ttu-id="9af22-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9af22-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9af22-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9af22-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9af22-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9af22-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9af22-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9af22-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9af22-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9af22-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9af22-128">Header</span><span class="sxs-lookup"><span data-stu-id="9af22-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af22-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9af22-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af22-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9af22-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af22-131">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9af22-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="9af22-132">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="9af22-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="9af22-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="9af22-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="9af22-134">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="9af22-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="9af22-135">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="9af22-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

