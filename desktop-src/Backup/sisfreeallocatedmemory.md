---
title: Sisfrezupedmemory-Funktion (Sisbkup. h)
description: Gibt durch SIS-API-Funktionen zugeordnete Speicher frei.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Sisfrezugeredmemory-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858760"
---
# <a name="sisfreeallocatedmemory-function"></a><span data-ttu-id="26958-104">Sisfrezugeredmemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="26958-104">SisFreeAllocatedMemory function</span></span>

<span data-ttu-id="26958-105">Die Funktion " **sisfrezugenspeicher** " gibt durch SIS-API-Funktionen zugewiesene Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="26958-105">The **SisFreeAllocatedMemory** function frees memory allocated by SIS API functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="26958-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="26958-106">Syntax</span></span>


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a><span data-ttu-id="26958-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="26958-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26958-108">*zustellspeicherplatz* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26958-108">*allocatedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26958-109">Zeiger auf den Arbeitsspeicher, der von der SIS-API zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="26958-109">Pointer to the memory allocated by the SIS API.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26958-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26958-110">Return value</span></span>

<span data-ttu-id="26958-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="26958-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26958-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26958-112">Remarks</span></span>

<span data-ttu-id="26958-113">Nachdem der Aufruf dieser Funktion abgeschlossen ist, kann der Aufrufer nicht mehr auf den freigegebenen Speicher zugreifen.</span><span class="sxs-lookup"><span data-stu-id="26958-113">After the call to this function completes, the caller may no longer access the freed memory.</span></span>

<span data-ttu-id="26958-114">Dieser Befehl sollte verwendet werden, um den zugeordneten Arbeitsspeicher für die Parameter Zeichenfolgen von *commonstorerootpathname* , die von " [**siscreatebackupstructure**](siscreatebackupstructure.md) " und " [**siscreaterestorestruktur**](siscreaterestorestructure.md)" zurückgegeben werden, und das Array von Zeichen folgen, das die Namen der allgemeinen Speicherdateien enthält, die von **siscreatebackupstructure**, [**siscsfilestobackupforlink**](siscsfilestobackupforlink.md), **siscreaterestorestruktur** und [**sisrestoredlink**](sisrestoredlink.md)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26958-114">This call should be used to deallocate the memory allocated for the *commonStoreRootPathname* parameter strings returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md) and [**SisCreateRestoreStructure**](siscreaterestorestructure.md), and the array of strings containing common-store file names returned from **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure**, and [**SisRestoredLink**](sisrestoredlink.md).</span></span> <span data-ttu-id="26958-115">Im letzteren Fall muss das Array selbst freigegeben werden, indem **sisfrezugedmemory** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="26958-115">In the latter case, the array itself also must be freed by calling **SisFreeAllocatedMemory**.</span></span>

## <a name="requirements"></a><span data-ttu-id="26958-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26958-116">Requirements</span></span>



| <span data-ttu-id="26958-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26958-117">Requirement</span></span> | <span data-ttu-id="26958-118">Wert</span><span class="sxs-lookup"><span data-stu-id="26958-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26958-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26958-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26958-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26958-120">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="26958-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26958-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26958-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26958-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="26958-123">Header</span><span class="sxs-lookup"><span data-stu-id="26958-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="26958-124"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="26958-124"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="26958-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26958-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="26958-126"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26958-126"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="26958-127">DLL</span><span class="sxs-lookup"><span data-stu-id="26958-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26958-128"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26958-128"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26958-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26958-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26958-130">**Siscreatebackupstructure**</span><span class="sxs-lookup"><span data-stu-id="26958-130">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="26958-131">**Siscreaterestorestruktur**</span><span class="sxs-lookup"><span data-stu-id="26958-131">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="26958-132">**Siscsfilestobackupforlink**</span><span class="sxs-lookup"><span data-stu-id="26958-132">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="26958-133">**Sisrestoredlink**</span><span class="sxs-lookup"><span data-stu-id="26958-133">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

 





