---
title: Sisrestoredcommonstorefile-Funktion (Sisbkup. h)
description: Meldet an die SIS-Architektur, dass eine Common Store-Datei geschrieben wurde.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Sisrestoredcommonstorefile-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949606"
---
# <a name="sisrestoredcommonstorefile-function"></a><span data-ttu-id="d8fdc-104">Sisrestoredcommonstorefile-Funktion</span><span class="sxs-lookup"><span data-stu-id="d8fdc-104">SisRestoredCommonStoreFile function</span></span>

<span data-ttu-id="d8fdc-105">Die **sisrestoredcommonstorefile** -Funktion meldet der SIS-Architektur, dass eine Common Store-Datei geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-105">The **SisRestoredCommonStoreFile** function reports to the SIS architecture that a common-store file has been written.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8fdc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8fdc-106">Syntax</span></span>


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a><span data-ttu-id="d8fdc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8fdc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8fdc-108">*sisrestorestruktur* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8fdc-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8fdc-109">Zeiger auf eine SIS-Wiederherstellungs Struktur, die von [**siscreaterestorestruktur**](siscreaterestorestructure.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8fdc-110">*commonstorefilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8fdc-110">*commonStoreFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8fdc-111">Der Name der wiederhergestellten Common-Store-Datei.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-111">Name of the restored common-store file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8fdc-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8fdc-112">Return value</span></span>

<span data-ttu-id="d8fdc-113">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d8fdc-113">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="d8fdc-114">Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-114">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8fdc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8fdc-115">Remarks</span></span>

<span data-ttu-id="d8fdc-116">Diese Funktion sollte aufgerufen werden, nachdem Sie eine Datei mit dem allgemeinen Speicher wieder hergestellt haben.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-116">This function should be called after you have restored a common-store file.</span></span> <span data-ttu-id="d8fdc-117">Die SIS-Architektur wird benachrichtigt, dass eine neue Common Store-Datei geschrieben wurde, sodass die SIS-Architektur interne Wartungs Tasks ausführen kann, wie z. b. das Initialisieren der internen Datenstrukturen oder das Beheben der Links zur Common-Store-Datei.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-117">It notifies the SIS architecture that a new common-store file has been written, so that the SIS architecture can perform internal maintenance tasks such as initializing its internal data structures or fixing the links to the common-store file.</span></span>

<span data-ttu-id="d8fdc-118">Beim Wiederherstellungs Vorgang sollten nur die von [**sisrestoredlink**](sisrestoredlink.md)gemeldeten Dateien für den gemeinsamen Speicher wieder hergestellt werden, auch wenn auf dem Sicherungsmedium weitere Dateien für den gemeinsamen Speicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-118">Your restore operation should restore only common-store files reported by [**SisRestoredLink**](sisrestoredlink.md), even if there are additional common-store files on the backup media.</span></span> <span data-ttu-id="d8fdc-119">Mit dem Wiederherstellungs Vorgang können die SIS-Links und die Dateien des Common Stores in beliebiger Reihenfolge wieder hergestellt werden. Er muss jedoch **sisrestoredlink** aufgerufen werden, nachdem er einen beliebigen Link wieder hergestellt hat, und diese Funktion muss aufgerufen werden, nachdem eine beliebige Common-Store-Datei wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-119">Your restore operation can restore the SIS links and common-store files in any order it chooses; however, it must call **SisRestoredLink** after it restores any link, and it must call this function after it restores any common-store file.</span></span> <span data-ttu-id="d8fdc-120">Da der Wiederherstellungs Vorgang nicht ermitteln kann, welche Dateien des Common Stores wieder hergestellt werden, bis die Dateinamen als Ergebnis der Wiederherstellung eines Links gemeldet werden, stellt der Wiederherstellungs Vorgang immer eine Common-Store-Datei wieder her, nachdem mindestens ein Link, auf den verwiesen wird, wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-120">Because your restore operation cannot identify which common-store files will be restored until the file names are reported to it as a result of restoring a link, your restore operation will always restore a common-store file after at least one link referring to it is restored.</span></span> <span data-ttu-id="d8fdc-121">Sie können jedoch zusätzliche SIS-Links wiederherstellen, die auf diese Datei mit dem gemeinsamen Speicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="d8fdc-121">However, you can then restore additional SIS links that point to that common-store file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8fdc-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8fdc-122">Requirements</span></span>



| <span data-ttu-id="d8fdc-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8fdc-123">Requirement</span></span> | <span data-ttu-id="d8fdc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d8fdc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fdc-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8fdc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d8fdc-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8fdc-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d8fdc-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8fdc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d8fdc-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8fdc-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d8fdc-129">Header</span><span class="sxs-lookup"><span data-stu-id="d8fdc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8fdc-130"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8fdc-130"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8fdc-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d8fdc-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8fdc-132"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8fdc-132"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8fdc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d8fdc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8fdc-134"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8fdc-134"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8fdc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8fdc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8fdc-136">**Siscreaterestorestruktur**</span><span class="sxs-lookup"><span data-stu-id="d8fdc-136">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="d8fdc-137">**Sisrestoredlink**</span><span class="sxs-lookup"><span data-stu-id="d8fdc-137">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

