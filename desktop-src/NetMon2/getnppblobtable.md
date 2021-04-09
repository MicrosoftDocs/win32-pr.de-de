---
description: Die getnppblobtable-Funktion Ruft eine NPP-BLOB-Tabelle ab, die die Register-NICs auf dem lokalen Computer darstellt.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Getnppblobtable-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866267"
---
# <a name="getnppblobtable-function"></a><span data-ttu-id="411f3-103">Getnppblobtable-Funktion</span><span class="sxs-lookup"><span data-stu-id="411f3-103">GetNPPBlobTable function</span></span>

<span data-ttu-id="411f3-104">Die **getnppblobtable** -Funktion Ruft eine NPP-BLOB-Tabelle ab, die die Register-NICs auf dem lokalen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="411f3-104">The **GetNPPBlobTable** function retrieves an NPP BLOB table that represents the register NICs on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="411f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="411f3-105">Syntax</span></span>


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a><span data-ttu-id="411f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="411f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="411f3-107">*hfilterblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="411f3-107">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="411f3-108">Handle für ein filterblob, das die in der Tabelle zurückgegebenen NPP-BLOBs einschränkt.</span><span class="sxs-lookup"><span data-stu-id="411f3-108">Handle to a filter BLOB that limits the NPP BLOBs returned in the table.</span></span>

</dd> <dt>

<span data-ttu-id="411f3-109">*ppblobtable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="411f3-109">*ppBlobTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411f3-110">Zeiger auf eine [BLOB- \_ Tabellen](blob-table.md) Struktur, die mindestens einen BLOB-Zeiger enthält.</span><span class="sxs-lookup"><span data-stu-id="411f3-110">Pointer to a [BLOB\_TABLE](blob-table.md) structure that contains at least one BLOB pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="411f3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="411f3-111">Return value</span></span>

<span data-ttu-id="411f3-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="411f3-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="411f3-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="411f3-113">If the function is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="411f3-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="411f3-114">Return code</span></span>                                                                                                | <span data-ttu-id="411f3-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411f3-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="411f3-116"><dt>**nmerr \_ keine \_ NPP- \_ dll**</dt></span><span class="sxs-lookup"><span data-stu-id="411f3-116"><dt>**NMERR\_NO\_NPP\_DLL**</dt></span></span> </dl>         | <span data-ttu-id="411f3-117">Es wurden keine DLLs im NPP-Verzeichnis gefunden.</span><span class="sxs-lookup"><span data-stu-id="411f3-117">No DLLs were found in the NPP directory.</span></span><br/>                    |
| <dl> <span data-ttu-id="411f3-118"><dt>**nmerr \_ keine \_ gültigen \_ NPP- \_ DLLs**</dt></span><span class="sxs-lookup"><span data-stu-id="411f3-118"><dt>**NMERR\_NO\_VALID\_NPP\_DLLS**</dt></span></span> </dl> | <span data-ttu-id="411f3-119">Keine der DLLs im NPP-Verzeichnis waren gültige NPP-DLLs.</span><span class="sxs-lookup"><span data-stu-id="411f3-119">None of the DLLs in the NPP directory were valid NPP DLLs.</span></span><br/>  |
| <dl> <span data-ttu-id="411f3-120"><dt>**nmerr \_ keine \_ übereinstimmenden \_ NPPs**</dt></span><span class="sxs-lookup"><span data-stu-id="411f3-120"><dt>**NMERR\_NO\_MATCHING\_NPPS**</dt></span></span> </dl>   | <span data-ttu-id="411f3-121">Es wurden NPP-BLOB ermittelt, aber der Filter Test wurde nicht erfolgreich durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="411f3-121">NPP BLOBs were discovered, but none passed the filter test.</span></span><br/> |
| <dl> <span data-ttu-id="411f3-122"><dt>**nmerr \_ \_ von \_ Memor**</dt></span><span class="sxs-lookup"><span data-stu-id="411f3-122"><dt>**NMERR\_OUT\_OF\_MEMOR**</dt></span></span> </dl>       | <span data-ttu-id="411f3-123">Netzwerkmonitor konnte keinen Arbeitsspeicher zuordnen.</span><span class="sxs-lookup"><span data-stu-id="411f3-123">Network Monitor was not able to allocate memory.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="411f3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="411f3-124">Remarks</span></span>

<span data-ttu-id="411f3-125">Das von *hfilterblob* benannte BLOB kann auch ein spezielles BLOB sein.</span><span class="sxs-lookup"><span data-stu-id="411f3-125">The BLOB named by *hFilterBlob* can also be a special BLOB.</span></span>

<span data-ttu-id="411f3-126">Wenn Sie das-Flag im filterblob auf **true** festlegen, kann die zurückgegebene BLOB-Tabelle auch spezielle BLOBs enthalten.</span><span class="sxs-lookup"><span data-stu-id="411f3-126">If you set the flag in the filter BLOB to **TRUE**, the returned BLOB table can also include special BLOBs .</span></span>

<span data-ttu-id="411f3-127">Wenn das von *hfilterblob* benannte BLOB ein spezielles BLOB ist, wird die Netzwerkmonitor-Benutzeroberfläche versuchen, Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="411f3-127">If the BLOB named by *hFilterBlob* is a special BLOB, the Network Monitor UI will attempt to process it.</span></span> <span data-ttu-id="411f3-128">Nehmen wir beispielsweise an, dass ein vorheriger-Rückruf ein spezielles BLOB aus dem Remote-NPP zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="411f3-128">For example, suppose that a previous call returns a special BLOB from the remote NPP.</span></span> <span data-ttu-id="411f3-129">Die Anwendung fügt das erforderliche Tag, den Computernamen, ein \_ .</span><span class="sxs-lookup"><span data-stu-id="411f3-129">The application inserts the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="411f3-130">Der Finder übergibt dann dieses BLOB an den NPP-Remote Computer, der dann eine Tabelle mit den NPP-BLOBs zurückgibt, die dem Computernamen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="411f3-130">The finder then passes this BLOB to the remote NPP, which then returns a table of the NPP BLOBs associated with the machine name.</span></span>

<span data-ttu-id="411f3-131">Um alle zurückgegebenen BLOBs und die BLOB-Tabelle zu zerstören, ist der Aufrufer für den Aufruf der **destroyblob** -Funktion verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="411f3-131">To destroy all returned BLOBs and the BLOB table, the caller is responsible for calling the **DestroyBlob** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="411f3-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="411f3-132">Requirements</span></span>



| <span data-ttu-id="411f3-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="411f3-133">Requirement</span></span> | <span data-ttu-id="411f3-134">Wert</span><span class="sxs-lookup"><span data-stu-id="411f3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="411f3-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="411f3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="411f3-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="411f3-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="411f3-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="411f3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="411f3-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="411f3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="411f3-139">Header</span><span class="sxs-lookup"><span data-stu-id="411f3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="411f3-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="411f3-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="411f3-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="411f3-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="411f3-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="411f3-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="411f3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="411f3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="411f3-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="411f3-144"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




