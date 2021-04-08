---
description: Die \_ Benachrichtigung spfilenotififileopverzögert wird von setupinstallfileex oder setupcommitfilequeue an eine Rückruf Routine gesendet, wenn ein Datei Vorgang verzögert wurde, weil die Datei verwendet wurde. Der Vorgang wird beim nächsten Neustart des Systems verarbeitet.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: SPFILENOTIFY_FILEOPDELAYED Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864192"
---
# <a name="spfilenotify_fileopdelayed-message"></a><span data-ttu-id="79364-104">\_Spfilenotifitififileopverzögerte Nachricht</span><span class="sxs-lookup"><span data-stu-id="79364-104">SPFILENOTIFY\_FILEOPDELAYED message</span></span>

<span data-ttu-id="79364-105">Die Benachrichtigung **\_ spfilenotififileopverzögert** wird von [**setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) oder [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) an eine Rückruf Routine gesendet, wenn ein Datei Vorgang verzögert wurde, weil die Datei verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="79364-105">The **SPFILENOTIFY\_FILEOPDELAYED** notification is sent by [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) or [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to a callback routine when a file operation was delayed because the file was in use.</span></span> <span data-ttu-id="79364-106">Der Vorgang wird beim nächsten Neustart des Systems verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="79364-106">The operation will be processed the next time the system is rebooted.</span></span>


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="79364-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="79364-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79364-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="79364-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="79364-109">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="79364-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

<span data-ttu-id="79364-110">Wenn es sich bei dem verzögerten Vorgang um einen Datei Kopiervorgang handelt, enthält die [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="79364-110">If the delayed operation is a file copy operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="79364-111">FilePath-Member</span><span class="sxs-lookup"><span data-stu-id="79364-111">FILEPATHS member</span></span> | <span data-ttu-id="79364-112">Wert</span><span class="sxs-lookup"><span data-stu-id="79364-112">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="79364-113">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="79364-113">**Win32Error**</span></span>   | <span data-ttu-id="79364-114">kein \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="79364-114">NO\_ERROR</span></span>                            |
| <span data-ttu-id="79364-115">**Flags**</span><span class="sxs-lookup"><span data-stu-id="79364-115">**Flags**</span></span>        | <span data-ttu-id="79364-116">fileOp- \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="79364-116">FILEOP\_COPY</span></span>                         |
| <span data-ttu-id="79364-117">**Quelle**</span><span class="sxs-lookup"><span data-stu-id="79364-117">**Source**</span></span>       | <span data-ttu-id="79364-118">Der vollständige Pfad der temporären Datei.</span><span class="sxs-lookup"><span data-stu-id="79364-118">Full path of the temporary file.</span></span>     |
| <span data-ttu-id="79364-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="79364-119">**Target**</span></span>       | <span data-ttu-id="79364-120">Vollständiger Pfad der eigentlichen Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="79364-120">Full path of the actual target file.</span></span> |



 

<span data-ttu-id="79364-121">Diese temporäre Datei wird in das Zielverzeichnis kopiert, wenn das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="79364-121">This temporary file will be copied to the target directory when the system is rebooted.</span></span> <span data-ttu-id="79364-122">Die Setup Funktionen generieren automatisch einen Pfad für die temporäre Datei.</span><span class="sxs-lookup"><span data-stu-id="79364-122">The setup functions automatically generate a path for the temporary file.</span></span>

<span data-ttu-id="79364-123">Wenn es sich bei dem verzögerten Vorgang um einen Datei Löschvorgang handelt, enthält die [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="79364-123">If the delayed operation is a file delete operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="79364-124">FilePath-Member</span><span class="sxs-lookup"><span data-stu-id="79364-124">FILEPATHS member</span></span> | <span data-ttu-id="79364-125">Wert</span><span class="sxs-lookup"><span data-stu-id="79364-125">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="79364-126">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="79364-126">**Win32Error**</span></span>   | <span data-ttu-id="79364-127">kein \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="79364-127">NO\_ERROR</span></span>                            |
| <span data-ttu-id="79364-128">**Flags**</span><span class="sxs-lookup"><span data-stu-id="79364-128">**Flags**</span></span>        | <span data-ttu-id="79364-129">fileOp \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="79364-129">FILEOP\_DELETE</span></span>                       |
| <span data-ttu-id="79364-130">**Quelle**</span><span class="sxs-lookup"><span data-stu-id="79364-130">**Source**</span></span>       | <span data-ttu-id="79364-131">NULL</span><span class="sxs-lookup"><span data-stu-id="79364-131">NULL</span></span>                                 |
| <span data-ttu-id="79364-132">**Target**</span><span class="sxs-lookup"><span data-stu-id="79364-132">**Target**</span></span>       | <span data-ttu-id="79364-133">Vollständiger Pfad der zu löschenden Datei.</span><span class="sxs-lookup"><span data-stu-id="79364-133">Full path of the file to be deleted.</span></span> |



 

</dd> <dt>

<span data-ttu-id="79364-134">*Param2*</span><span class="sxs-lookup"><span data-stu-id="79364-134">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="79364-135">Wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="79364-135">Is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79364-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79364-136">Return value</span></span>

<span data-ttu-id="79364-137">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="79364-137">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="79364-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79364-138">Requirements</span></span>



| <span data-ttu-id="79364-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79364-139">Requirement</span></span> | <span data-ttu-id="79364-140">Wert</span><span class="sxs-lookup"><span data-stu-id="79364-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79364-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79364-141">Minimum supported client</span></span><br/> | <span data-ttu-id="79364-142">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79364-142">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="79364-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79364-143">Minimum supported server</span></span><br/> | <span data-ttu-id="79364-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79364-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79364-145">Header</span><span class="sxs-lookup"><span data-stu-id="79364-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="79364-146"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="79364-146"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79364-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="79364-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79364-148">Übersicht</span><span class="sxs-lookup"><span data-stu-id="79364-148">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="79364-149">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="79364-149">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="79364-150">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="79364-150">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="79364-151">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="79364-151">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="79364-152">**Setupinstallfile**</span><span class="sxs-lookup"><span data-stu-id="79364-152">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="79364-153">**Setupinstallfileex**</span><span class="sxs-lookup"><span data-stu-id="79364-153">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="79364-154">**Setupinstallfrominf-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="79364-154">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




