---
description: Listet geschützte Dateien auf.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Sfcgetfiles-Funktion (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865976"
---
# <a name="sfcgetfiles-function"></a><span data-ttu-id="565a7-103">Sfcgetfiles-Funktion</span><span class="sxs-lookup"><span data-stu-id="565a7-103">SfcGetFiles function</span></span>

<span data-ttu-id="565a7-104">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="565a7-104">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="565a7-105">Die Unterstützung für diese Funktion wurde in Windows Vista und Windows Server 2008 entfernt.</span><span class="sxs-lookup"><span data-stu-id="565a7-105">Support for this function was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="565a7-106">Verwenden Sie stattdessen die in [WRP-Funktionen](wfp-functions.md) aufgeführten unterstützten Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="565a7-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="565a7-107">Listet geschützte Dateien auf.</span><span class="sxs-lookup"><span data-stu-id="565a7-107">Lists protected files.</span></span>

## <a name="syntax"></a><span data-ttu-id="565a7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="565a7-108">Syntax</span></span>


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a><span data-ttu-id="565a7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="565a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="565a7-110">" *Protfiledata* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="565a7-110">*ProtFileData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="565a7-111">Ein Zeiger auf eine [**pprotect- \_ Datei \_ Eintrags**](pprotect-file-entry.md) Struktur, die die Liste der geschützten Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="565a7-111">A pointer to a [**PPROTECT\_FILE\_ENTRY**](pprotect-file-entry.md) structure that contains the protected files list.</span></span>

</dd> <dt>

<span data-ttu-id="565a7-112">*Dateianzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="565a7-112">*FileCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="565a7-113">Ein Zeiger auf einen Speicherort, der einen Ulong-Wert enthält, der die Anzahl der geschützten Dateien ist.</span><span class="sxs-lookup"><span data-stu-id="565a7-113">A pointer to a location containing a ULONG value that is the number of protected files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="565a7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="565a7-114">Return value</span></span>

<span data-ttu-id="565a7-115">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert Status \_ Success.</span><span class="sxs-lookup"><span data-stu-id="565a7-115">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span> <span data-ttu-id="565a7-116">Wenn die Funktion fehlschlägt, wird der entsprechende NTSTATUS-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="565a7-116">If the function fails, it returns the appropriate NTSTATUS error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="565a7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="565a7-117">Requirements</span></span>



| <span data-ttu-id="565a7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="565a7-118">Requirement</span></span> | <span data-ttu-id="565a7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="565a7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="565a7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="565a7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="565a7-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="565a7-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="565a7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="565a7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="565a7-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="565a7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="565a7-124">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="565a7-124">End of client support</span></span><br/>    | <span data-ttu-id="565a7-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="565a7-125">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="565a7-126">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="565a7-126">End of server support</span></span><br/>    | <span data-ttu-id="565a7-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="565a7-127">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="565a7-128">Header</span><span class="sxs-lookup"><span data-stu-id="565a7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="565a7-129"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="565a7-129"><dt>Sfcfiles.h</dt></span></span> </dl>   |
| <span data-ttu-id="565a7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="565a7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="565a7-131"><dt>Sfcfiles.dll</dt></span><span class="sxs-lookup"><span data-stu-id="565a7-131"><dt>Sfcfiles.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="565a7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="565a7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="565a7-133">**pprotect- \_ Datei \_ Eintrag**</span><span class="sxs-lookup"><span data-stu-id="565a7-133">**PPROTECT\_FILE\_ENTRY**</span></span>](pprotect-file-entry.md)
</dt> </dl>

 

 




