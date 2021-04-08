---
title: Sisfrebackupstructure-Funktion (Sisbkup. h)
description: Gibt die angegebene SIS-Sicherungs Struktur frei.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Sisfrebackupstructure-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740696"
---
# <a name="sisfreebackupstructure-function"></a><span data-ttu-id="16286-104">Sisfrebackupstructure-Funktion</span><span class="sxs-lookup"><span data-stu-id="16286-104">SisFreeBackupStructure function</span></span>

<span data-ttu-id="16286-105">Die **sisfrebackupstructure** -Funktion gibt die angegebene SIS-Sicherungs Struktur frei.</span><span class="sxs-lookup"><span data-stu-id="16286-105">The **SisFreeBackupStructure** function frees the specified SIS backup structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="16286-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16286-106">Syntax</span></span>


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a><span data-ttu-id="16286-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="16286-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16286-108">*sisbackupstructure* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16286-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16286-109">Ein Zeiger auf die SIS-Sicherungs Struktur, die von [**siscreatebackupstructure**](siscreatebackupstructure.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="16286-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16286-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16286-110">Return value</span></span>

<span data-ttu-id="16286-111">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="16286-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="16286-112">Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="16286-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="16286-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16286-113">Remarks</span></span>

<span data-ttu-id="16286-114">Diese Funktion sollte aufgerufen werden, nachdem der Sicherungs Vorgang für das durch den Wert des Parameters *sisbackupstructure* identifizierte Volume abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="16286-114">This function should be called after the backup operation is completed for the volume identified by the value of the *sisBackupStructure* parameter.</span></span>

<span data-ttu-id="16286-115">Beachten Sie, dass es nicht sicher geht, dass dies nur den Arbeitsspeicher zuweist.</span><span class="sxs-lookup"><span data-stu-id="16286-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="16286-116">Diese Funktion kann z. b. auch zusätzliche administrative Vorgänge für die SIS-Architektur ausführen.</span><span class="sxs-lookup"><span data-stu-id="16286-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="16286-117">Daher wird diese Funktion auch dann aufgerufen, wenn der Sicherungs Vorgang sofort danach beendet wird.</span><span class="sxs-lookup"><span data-stu-id="16286-117">Therefore, call this function even if your backup operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="16286-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16286-118">Requirements</span></span>



| <span data-ttu-id="16286-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16286-119">Requirement</span></span> | <span data-ttu-id="16286-120">Wert</span><span class="sxs-lookup"><span data-stu-id="16286-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16286-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16286-121">Minimum supported client</span></span><br/> | <span data-ttu-id="16286-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16286-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="16286-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16286-123">Minimum supported server</span></span><br/> | <span data-ttu-id="16286-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16286-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="16286-125">Header</span><span class="sxs-lookup"><span data-stu-id="16286-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16286-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="16286-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="16286-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="16286-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="16286-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16286-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="16286-129">DLL</span><span class="sxs-lookup"><span data-stu-id="16286-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16286-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16286-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16286-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16286-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16286-132">**Siscreatebackupstructure**</span><span class="sxs-lookup"><span data-stu-id="16286-132">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

