---
description: Ruft Informationen über den derzeit geladenen Satz von Modulen für das System ab.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: "\"Auxklibquerymoduleinformation\"-Funktion (AUX \\_ KLIB. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357969"
---
# <a name="auxklibquerymoduleinformation-function"></a><span data-ttu-id="be83d-103">"Auxklibquerymoduleinformation"-Funktion</span><span class="sxs-lookup"><span data-stu-id="be83d-103">AuxKlibQueryModuleInformation function</span></span>

<span data-ttu-id="be83d-104">Ruft Informationen über den derzeit geladenen Satz von Modulen für das System ab.</span><span class="sxs-lookup"><span data-stu-id="be83d-104">Retrieves information about the currently loaded set of modules for the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="be83d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be83d-105">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a><span data-ttu-id="be83d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be83d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be83d-107">*BufferSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="be83d-107">*BufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be83d-108">Bei Eingabe die Größe des *QueryInfo* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="be83d-108">On input, the size of the *QueryInfo* buffer, in bytes.</span></span> <span data-ttu-id="be83d-109">Bei Ausgabe wird die tatsächlich erforderliche Größe empfangen.</span><span class="sxs-lookup"><span data-stu-id="be83d-109">On output, receives the actual required size.</span></span> <span data-ttu-id="be83d-110">Da die Liste der Systemmodule zwischen Aufrufen geändert werden kann, kann dieser Wert auch zwischen Aufrufen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="be83d-110">Because the system module list can change between calls, this value can also change between calls.</span></span>

</dd> <dt>

<span data-ttu-id="be83d-111">*Element Size* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be83d-111">*ElementSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be83d-112">Die Größe eines Array Elements in Byte.</span><span class="sxs-lookup"><span data-stu-id="be83d-112">The size, in bytes, of an array element.</span></span> <span data-ttu-id="be83d-113">Diese Größe bestimmt das Format der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="be83d-113">This size determines the format of the output.</span></span>

</dd> <dt>

<span data-ttu-id="be83d-114">*QueryInfo* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="be83d-114">*QueryInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be83d-115">Ein Zeiger auf einen Puffer, der die Modul Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="be83d-115">A pointer to a buffer that receives the module information.</span></span> <span data-ttu-id="be83d-116">Diese Informationen werden in einem Array zurückgegeben, dessen Elemente eine der folgenden Strukturen sind: [**aux \_ Module \_ Basic \_ Info**](aux-module-basic-info-struct.md) oder [**\_ \_ Erweiterte \_ Informationen des aux-Moduls**](aux-module-extended-info-struct.md).</span><span class="sxs-lookup"><span data-stu-id="be83d-116">This information is returned in an array whose elements are one of the following structures: [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) or [**AUX\_MODULE\_EXTENDED\_INFO**](aux-module-extended-info-struct.md).</span></span> <span data-ttu-id="be83d-117">Die jeweilige verwendete-Struktur hängt von der angegebenen Elementgröße ab.</span><span class="sxs-lookup"><span data-stu-id="be83d-117">The specific structure used depends on the specified element size.</span></span>

<span data-ttu-id="be83d-118">Wenn dieser Parameter **null** ist, gibt die Funktion die erforderliche Puffergröße zurück.</span><span class="sxs-lookup"><span data-stu-id="be83d-118">If this parameter is **NULL**, the function returns the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be83d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be83d-119">Return value</span></span>

<span data-ttu-id="be83d-120">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert Status \_ Success.</span><span class="sxs-lookup"><span data-stu-id="be83d-120">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="be83d-121">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der in "NTSTATUS. h" definierten Statuscodes sein, die im WDK verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="be83d-121">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="be83d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be83d-122">Remarks</span></span>

<span data-ttu-id="be83d-123">Sie müssen die Funktion " [**auxklibinitialize**](auxklibinitialize-func.md) " aufrufen, bevor Sie diese Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="be83d-123">You must call the [**AuxKlibInitialize**](auxklibinitialize-func.md) function before calling this function.</span></span>

<span data-ttu-id="be83d-124">Die Objektbibliothek, die diese API implementiert, kann [hier](https://www.microsoft.com/?ref=go)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="be83d-124">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="be83d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be83d-125">Requirements</span></span>



| <span data-ttu-id="be83d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be83d-126">Requirement</span></span> | <span data-ttu-id="be83d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="be83d-127">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be83d-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="be83d-128">Redistributable</span></span><br/> | <span data-ttu-id="be83d-129">Windows-Erweiterungs-API-Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="be83d-129">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="be83d-130">Header</span><span class="sxs-lookup"><span data-stu-id="be83d-130">Header</span></span><br/>          | <dl> <span data-ttu-id="be83d-131"><dt>AUX \_ KLIB. h</dt></span><span class="sxs-lookup"><span data-stu-id="be83d-131"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="be83d-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be83d-132">Library</span></span><br/>         | <dl> <span data-ttu-id="be83d-133"><dt>AUX \_ KLIB. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be83d-133"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be83d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be83d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be83d-135">**"Auxklibinitialize"**</span><span class="sxs-lookup"><span data-stu-id="be83d-135">**AuxKlibInitialize**</span></span>](auxklibinitialize-func.md)
</dt> <dt>

[<span data-ttu-id="be83d-136">**\_ \_ grundlegende \_ Informationen zu aux-Modulen**</span><span class="sxs-lookup"><span data-stu-id="be83d-136">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> <dt>

[<span data-ttu-id="be83d-137">**\_ \_ Erweiterte \_ Informationen des aux-Moduls**</span><span class="sxs-lookup"><span data-stu-id="be83d-137">**AUX\_MODULE\_EXTENDED\_INFO**</span></span>](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




