---
description: Sucht nach der angegebenen ausführbaren Datei.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: Sdbgetmatchingexe-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861051"
---
# <a name="sdbgetmatchingexe-function"></a><span data-ttu-id="34f33-103">Sdbgetmatchingexe-Funktion</span><span class="sxs-lookup"><span data-stu-id="34f33-103">SdbGetMatchingExe function</span></span>

<span data-ttu-id="34f33-104">Sucht nach der angegebenen ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="34f33-104">Searches for the specified executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34f33-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a><span data-ttu-id="34f33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34f33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34f33-107">*hsdb* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="34f33-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34f33-108">Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="34f33-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="34f33-109">*szpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34f33-109">*szPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34f33-110">Der Pfad der ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="34f33-110">The path of the executable.</span></span>

</dd> <dt>

<span data-ttu-id="34f33-111">*szModuleName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="34f33-111">*szModuleName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34f33-112">Der Modulname.</span><span class="sxs-lookup"><span data-stu-id="34f33-112">The module name.</span></span>

</dd> <dt>

<span data-ttu-id="34f33-113">*pszenvironment* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="34f33-113">*pszEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34f33-114">Die Umgebungsvariablen, die als Such Kontext verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34f33-114">The environment variables to be used as search context.</span></span>

</dd> <dt>

<span data-ttu-id="34f33-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34f33-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34f33-116">Dieser Parameter kann 0 oder **sdbgmef \_ Ignore \_ Environment** (0x1) sein.</span><span class="sxs-lookup"><span data-stu-id="34f33-116">This parameter can be 0 or **SDBGMEF\_IGNORE\_ENVIRONMENT** (0x1).</span></span>

</dd> <dt>

<span data-ttu-id="34f33-117">*pqueryresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="34f33-117">*pQueryResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34f33-118">Eine [**sdbqueryresult**](sdbqueryresult.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="34f33-118">An [**SDBQUERYRESULT**](sdbqueryresult.md) structure.</span></span> <span data-ttu-id="34f33-119">Wenn keine Entsprechung gefunden wird, enthält die Struktur **tagref \_ null**.</span><span class="sxs-lookup"><span data-stu-id="34f33-119">If no match is found, the structure contains **TAGREF\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34f33-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34f33-120">Return value</span></span>

<span data-ttu-id="34f33-121">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="34f33-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="34f33-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34f33-122">Remarks</span></span>

<span data-ttu-id="34f33-123">Wenn Sie die zurückgegebene [**tagref**](tagref.md)abgeschlossen haben, können Sie Sie mit der [**sdbreleasematchingexe**](sdbreleasematchingexe.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="34f33-123">When you have finished with the returned [**TAGREF**](tagref.md), free it using the [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f33-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34f33-124">Requirements</span></span>



| <span data-ttu-id="34f33-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34f33-125">Requirement</span></span> | <span data-ttu-id="34f33-126">Wert</span><span class="sxs-lookup"><span data-stu-id="34f33-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34f33-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34f33-127">Minimum supported client</span></span><br/> | <span data-ttu-id="34f33-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34f33-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="34f33-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34f33-129">Minimum supported server</span></span><br/> | <span data-ttu-id="34f33-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34f33-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="34f33-131">DLL</span><span class="sxs-lookup"><span data-stu-id="34f33-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34f33-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34f33-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34f33-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34f33-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f33-134">**Sdbinitdatabase**</span><span class="sxs-lookup"><span data-stu-id="34f33-134">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="34f33-135">**Sdbreleasematchingexe**</span><span class="sxs-lookup"><span data-stu-id="34f33-135">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> </dl>

 

 




