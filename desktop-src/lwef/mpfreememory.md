---
title: Mpfrememory-Funktion (mpclient. h)
description: Gibt Arbeitsspeicher für den Malware Schutz-Manager frei.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Mpfrememory-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741009"
---
# <a name="mpfreememory-function"></a><span data-ttu-id="9227b-104">Mpfrememory-Funktion</span><span class="sxs-lookup"><span data-stu-id="9227b-104">MpFreeMemory function</span></span>

<span data-ttu-id="9227b-105">Gibt Arbeitsspeicher für den Malware Schutz-Manager frei.</span><span class="sxs-lookup"><span data-stu-id="9227b-105">Frees memory for the malware protection manager.</span></span> <span data-ttu-id="9227b-106">Alle Puffer, die von Malware Schutzfunktionen zugeordnet und zurückgegeben werden, müssen vom Aufrufer mithilfe dieser Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9227b-106">All buffers allocated and returned by malware protection functions must be freed by the caller using this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9227b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9227b-107">Syntax</span></span>


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="9227b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9227b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9227b-109">*pmemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9227b-109">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9227b-110">Typ: **pVoid**</span><span class="sxs-lookup"><span data-stu-id="9227b-110">Type: **PVOID**</span></span>

<span data-ttu-id="9227b-111">Ein Zeiger auf den Arbeitsspeicher, der von einer Malware Schutzfunktion zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9227b-111">A pointer to memory allocated by a malware protection function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9227b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9227b-112">Return value</span></span>

<span data-ttu-id="9227b-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9227b-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9227b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9227b-114">Remarks</span></span>

<span data-ttu-id="9227b-115">Um die Speicherverwaltung für Clients zu vereinfachen, definiert der Malware Schutz-Manager auch Makros, um Speicher freizugeben, der mit verschiedenen von Malware Schutzfunktionen zurückgegebenen Strukturen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9227b-115">To facilitate memory management for clients, the malware protection manager also defines macros to free memory associated with various structures returned by malware protection functions.</span></span> <span data-ttu-id="9227b-116">Die folgenden Makros sind in der Header Datei mpmemfree. h definiert:</span><span class="sxs-lookup"><span data-stu-id="9227b-116">The following macros are defined in the header file mpmemfree.h:</span></span>



| <span data-ttu-id="9227b-117">Name</span><span class="sxs-lookup"><span data-stu-id="9227b-117">Name</span></span>                            | <span data-ttu-id="9227b-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9227b-118">Description</span></span>                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9227b-119">mpresource- \_ Informationen \_ frei</span><span class="sxs-lookup"><span data-stu-id="9227b-119">MPRESOURCE\_INFO\_FREE</span></span>          | <span data-ttu-id="9227b-120">Gibt zugeordnete [**mpresource- \_ Informationen**](mpresource-info.md)frei.</span><span class="sxs-lookup"><span data-stu-id="9227b-120">Frees an allocated [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>                  |
| <span data-ttu-id="9227b-121">mpthreat- \_ Informationen \_ frei</span><span class="sxs-lookup"><span data-stu-id="9227b-121">MPTHREAT\_INFO\_FREE</span></span>            | <span data-ttu-id="9227b-122">Gibt zugeordnete [**mpthreat- \_ Informationen**](mpthreat-info.md)frei.</span><span class="sxs-lookup"><span data-stu-id="9227b-122">Frees an allocated [**MPTHREAT\_INFO**](mpthreat-info.md).</span></span>                      |
| <span data-ttu-id="9227b-123">lokalisierte mpthreat- \_ \_ Informationen \_ kostenlos</span><span class="sxs-lookup"><span data-stu-id="9227b-123">MPTHREAT\_LOCALIZED\_INFO\_FREE</span></span> | <span data-ttu-id="9227b-124">Gibt eine zugeordnete, [**mpthreat \_ lokalisierte \_ Information**](mpthreat-localized-info.md)frei.</span><span class="sxs-lookup"><span data-stu-id="9227b-124">Frees an allocated [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9227b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9227b-125">Requirements</span></span>



| <span data-ttu-id="9227b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9227b-126">Requirement</span></span> | <span data-ttu-id="9227b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9227b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9227b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9227b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9227b-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9227b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9227b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9227b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9227b-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9227b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9227b-132">Header</span><span class="sxs-lookup"><span data-stu-id="9227b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9227b-133"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9227b-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9227b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9227b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9227b-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9227b-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9227b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9227b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9227b-137">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="9227b-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="9227b-138">**mpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="9227b-138">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="9227b-139">**mpthreat- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="9227b-139">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="9227b-140">**lokalisierte mpthreat- \_ \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="9227b-140">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





