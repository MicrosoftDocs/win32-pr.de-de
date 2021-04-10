---
description: Ruft die Attributdaten für die angegebene Datei ab.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: Sdbgetfileattribute-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125624"
---
# <a name="sdbgetfileattributes-function"></a><span data-ttu-id="ae2f2-103">Sdbgetfileattribute-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae2f2-103">SdbGetFileAttributes function</span></span>

<span data-ttu-id="ae2f2-104">Ruft die Attributdaten für die angegebene Datei ab.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-104">Retrieves the attribute data for the specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae2f2-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a><span data-ttu-id="ae2f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae2f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2f2-107">*lpwszfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae2f2-107">*lpwszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2f2-108">Der Pfad zur Datei.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-108">The path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="ae2f2-109">*ppattrinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae2f2-109">*ppAttrInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2f2-110">Ein Array von [**attrinfo**](attrinfo.md) -Strukturen, die die Attributdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-110">An array of [**ATTRINFO**](attrinfo.md) structures that contain the attribute data.</span></span>

</dd> <dt>

<span data-ttu-id="ae2f2-111">*lpdwattrcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae2f2-111">*lpdwAttrCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2f2-112">Die Anzahl der Attribute.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-112">The number of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2f2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae2f2-113">Return value</span></span>

<span data-ttu-id="ae2f2-114">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-114">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2f2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae2f2-115">Remarks</span></span>

<span data-ttu-id="ae2f2-116">Wenn Sie mit den Daten fertig sind, können Sie Sie mit der [**sdbfreefileattribute**](sdbfreefileattributes.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-116">When you have finished with the data, free it using the [**SdbFreeFileAttributes**](sdbfreefileattributes.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2f2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae2f2-117">Requirements</span></span>



| <span data-ttu-id="ae2f2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae2f2-118">Requirement</span></span> | <span data-ttu-id="ae2f2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ae2f2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2f2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2f2-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae2f2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ae2f2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2f2-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae2f2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ae2f2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ae2f2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae2f2-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae2f2-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2f2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae2f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2f2-127">**Sdbformatattribute**</span><span class="sxs-lookup"><span data-stu-id="ae2f2-127">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="ae2f2-128">**Sdbfrefileattribute**</span><span class="sxs-lookup"><span data-stu-id="ae2f2-128">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> </dl>

 

 




