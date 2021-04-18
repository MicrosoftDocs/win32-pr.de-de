---
description: Die getnppeer Type esapfilter-Funktion Ruft den ETYPE/SAP-Filter aus einem angegebenen BLOB ab.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Getnppeer Type esapfilter-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351170"
---
# <a name="getnppetypesapfilter-function"></a><span data-ttu-id="d5926-103">Getnppeer Type esapfilter-Funktion</span><span class="sxs-lookup"><span data-stu-id="d5926-103">GetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="d5926-104">Die **getnppeer Type esapfilter** -Funktion Ruft den ETYPE/SAP-Filter aus einem angegebenen BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="d5926-104">The **GetNPPEtypeSapFilter** function retrieves the Etype/Sap filter from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5926-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5926-105">Syntax</span></span>


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d5926-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5926-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5926-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5926-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5926-108">Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="d5926-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="d5926-109">*pnsaps* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5926-109">*pnSaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5926-110">Ein Zeiger auf die zurückgegebene Anzahl von Protokollen in der SAP-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d5926-110">Pointer to the returned number of protocols in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="d5926-111">*pnettypes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5926-111">*pnEtypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5926-112">Ein Zeiger auf die zurückgegebene Anzahl von ETYPEs in der ETYPE-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d5926-112">Pointer to the returned number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="d5926-113">*ppsaptable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5926-113">*ppSapTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5926-114">Zeiger auf die zurückgegebene SAP-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d5926-114">Pointer to the returned SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="d5926-115">*ppeer typetable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5926-115">*ppEtypeTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5926-116">Ein Zeiger auf die zurückgegebene ETYPE-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d5926-116">Pointer to the returned Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="d5926-117">*pfilterflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5926-117">*pFilterFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5926-118">Zeiger auf die zurückgegebenen Filterflags.</span><span class="sxs-lookup"><span data-stu-id="d5926-118">Pointer to the returned filter flags.</span></span>

</dd> <dt>

<span data-ttu-id="d5926-119">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5926-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5926-120">Handle für einen fehlerblob, der den Speicherort im ursprünglichen BLOB angibt, an dem der Fehler (falls vorhanden) aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d5926-120">Handle to an error BLOB, which specifies the location in the original BLOB where the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5926-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5926-121">Return value</span></span>

<span data-ttu-id="d5926-122">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d5926-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d5926-123">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="d5926-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5926-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5926-124">Remarks</span></span>

<span data-ttu-id="d5926-125">Die ETYPE/SAP-Informationen werden in der Kategorie **config** des Abschnitts NPP- **Besitzer** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d5926-125">The Etype/Sap information is stored in the **Config** category of the NPP **Owner** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5926-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5926-126">Requirements</span></span>



| <span data-ttu-id="d5926-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5926-127">Requirement</span></span> | <span data-ttu-id="d5926-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d5926-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5926-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5926-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d5926-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5926-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d5926-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5926-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d5926-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5926-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5926-133">Header</span><span class="sxs-lookup"><span data-stu-id="d5926-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5926-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5926-134"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="d5926-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5926-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5926-136"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5926-136"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5926-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d5926-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5926-138"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5926-138"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5926-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5926-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5926-140">Setnppeer Type esapfilter</span><span class="sxs-lookup"><span data-stu-id="d5926-140">SetNPPEtypeSapFilter</span></span>](setnppetypesapfilter.md)
</dt> </dl>

 

 




