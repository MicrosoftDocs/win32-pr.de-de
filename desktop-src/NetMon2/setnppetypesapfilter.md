---
description: Legt den BLOB-ETYPE/SAP-Filter fest.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Setnppeer Type esapfilter-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344959"
---
# <a name="setnppetypesapfilter-function"></a><span data-ttu-id="8cd85-103">Setnppeer Type esapfilter-Funktion</span><span class="sxs-lookup"><span data-stu-id="8cd85-103">SetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="8cd85-104">Die **setnppeer Type esapfilter** -Funktion legt den BLOB-ETYPE/SAP-Filter fest.</span><span class="sxs-lookup"><span data-stu-id="8cd85-104">The **SetNPPEtypeSapFilter** function sets the BLOB Etype/Sap filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd85-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cd85-105">Syntax</span></span>


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8cd85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cd85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cd85-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd85-108">Ein Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="8cd85-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="8cd85-109">*NSAPs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-109">*nSaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd85-110">Die Anzahl der SAPS.</span><span class="sxs-lookup"><span data-stu-id="8cd85-110">The number of SAPs.</span></span>

</dd> <dt>

<span data-ttu-id="8cd85-111">" *ntypes* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-111">*nEtypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd85-112">Die Anzahl der ETYPEs in der ETYPE-Tabelle, die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8cd85-112">The number of Etypes in the Etype table being set.</span></span>

</dd> <dt>

<span data-ttu-id="8cd85-113">*lpsaptable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-113">*lpSapTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd85-114">Ein Zeiger auf die festgelegte SAP-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8cd85-114">A pointer to the SAP table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="8cd85-115">*lpeer typetable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-115">*lpEtypeTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd85-116">Ein Zeiger auf die ETYPE-Tabelle, die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8cd85-116">A pointer to the Etype table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="8cd85-117">*Filterflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-117">*FilterFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd85-118">Die Filterflags, die festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8cd85-118">The filter flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="8cd85-119">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd85-120">Das Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="8cd85-120">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cd85-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cd85-121">Return value</span></span>

<span data-ttu-id="8cd85-122">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8cd85-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8cd85-123">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="8cd85-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cd85-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cd85-124">Requirements</span></span>



| <span data-ttu-id="8cd85-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cd85-125">Requirement</span></span> | <span data-ttu-id="8cd85-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8cd85-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd85-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cd85-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd85-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8cd85-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cd85-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd85-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cd85-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8cd85-131">Header</span><span class="sxs-lookup"><span data-stu-id="8cd85-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cd85-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cd85-132"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="8cd85-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8cd85-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="8cd85-134"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cd85-134"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="8cd85-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8cd85-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cd85-136"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cd85-136"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cd85-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cd85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd85-138">Getnpettypesapfilter</span><span class="sxs-lookup"><span data-stu-id="8cd85-138">GetNPPEtypeSapFilter</span></span>](getnppetypesapfilter.md)
</dt> </dl>

 

 




