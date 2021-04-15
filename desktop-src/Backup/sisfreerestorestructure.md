---
title: Sisfreerestorestruktur-Funktion (Sisbkup. h)
description: Gibt den für die angegebene SIS-Wiederherstellungs Struktur zugeordneten Arbeitsspeicher frei und führt Tasks aus, die den SIS-Filter vorbereiten, um die während des Wiederherstellungs Vorgangs erstellten Links ordnungsgemäß einzurichten.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Sicherung der sisfreerestorestruktur-Funktion
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478729"
---
# <a name="sisfreerestorestructure-function"></a><span data-ttu-id="7a4bf-104">Sisfreerestorestruktur-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a4bf-104">SisFreeRestoreStructure function</span></span>

<span data-ttu-id="7a4bf-105">Die **sisfreerestorestruktur** -Funktion gibt den für die angegebene SIS-Wiederherstellungs Struktur zugeordneten Arbeitsspeicher frei und führt Tasks aus, die den SIS-Filter für die ordnungsgemäße Einrichtung der während des Wiederherstellungs Vorgangs erstellten Verknüpfungen vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="7a4bf-105">The **SisFreeRestoreStructure** function frees the memory allocated for the specified SIS restore structure, and performs tasks that prepare the SIS filter to properly set up the links created during the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a4bf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a4bf-106">Syntax</span></span>


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a><span data-ttu-id="7a4bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a4bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a4bf-108">*sisrestorestruktur* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a4bf-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a4bf-109">Zeiger auf eine SIS-Wiederherstellungs Struktur, die von [**siscreaterestorestruktur**](siscreaterestorestructure.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7a4bf-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a4bf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a4bf-110">Return value</span></span>

<span data-ttu-id="7a4bf-111">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="7a4bf-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="7a4bf-112">Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7a4bf-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a4bf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a4bf-113">Remarks</span></span>

<span data-ttu-id="7a4bf-114">Der Zugriff auf die SIS-Links, bevor der Aufrufen dieser Funktion abgeschlossen wird, kann zu einer Volumeüberprüfung oder einem partiellen Lesevorgang für den Inhalt des Links führen.</span><span class="sxs-lookup"><span data-stu-id="7a4bf-114">Accessing the SIS links before the call to this function completes can result in a volume check or a partial read of the link's contents.</span></span>

<span data-ttu-id="7a4bf-115">Beachten Sie, dass es nicht sicher geht, dass dies nur den Arbeitsspeicher zuweist.</span><span class="sxs-lookup"><span data-stu-id="7a4bf-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="7a4bf-116">Diese Funktion kann z. b. auch zusätzliche administrative Vorgänge für die SIS-Architektur ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a4bf-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="7a4bf-117">Daher wird diese Funktion auch dann aufgerufen, wenn der Wiederherstellungs Vorgang sofort beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a4bf-117">Therefore, call this function even if your restore operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a4bf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a4bf-118">Requirements</span></span>



| <span data-ttu-id="7a4bf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a4bf-119">Requirement</span></span> | <span data-ttu-id="7a4bf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7a4bf-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4bf-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a4bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4bf-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a4bf-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7a4bf-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a4bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4bf-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a4bf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7a4bf-125">Header</span><span class="sxs-lookup"><span data-stu-id="7a4bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a4bf-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a4bf-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a4bf-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a4bf-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a4bf-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a4bf-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="7a4bf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7a4bf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a4bf-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a4bf-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a4bf-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a4bf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a4bf-132">**Siscreaterestorestruktur**</span><span class="sxs-lookup"><span data-stu-id="7a4bf-132">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> </dl>

 

