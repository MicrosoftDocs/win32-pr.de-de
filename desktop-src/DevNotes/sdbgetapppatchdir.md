---
description: Ruft das System-AppPatch-Verzeichnis ab.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: Sdbgetapppatchdir-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125635"
---
# <a name="sdbgetapppatchdir-function"></a><span data-ttu-id="badd7-103">Sdbgetapppatchdir-Funktion</span><span class="sxs-lookup"><span data-stu-id="badd7-103">SdbGetAppPatchDir function</span></span>

<span data-ttu-id="badd7-104">Ruft das System-AppPatch-Verzeichnis ab.</span><span class="sxs-lookup"><span data-stu-id="badd7-104">Retrieves the system AppPatch directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="badd7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="badd7-105">Syntax</span></span>


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a><span data-ttu-id="badd7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="badd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="badd7-107">*hsdb* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="badd7-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="badd7-108">Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="badd7-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="badd7-109">*szapppatchpath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="badd7-109">*szAppPatchPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="badd7-110">Der resultierende Pfad.</span><span class="sxs-lookup"><span data-stu-id="badd7-110">The resulting path.</span></span>

</dd> <dt>

<span data-ttu-id="badd7-111">*cchsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="badd7-111">*cchSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="badd7-112">Die Größe des *szapppatchpath* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="badd7-112">The size of the *szAppPatchPath* buffer, in characters.</span></span> <span data-ttu-id="badd7-113">Wenn die Funktion fehlschlägt, wird dieser Parameter auf die leere Zeichenfolge ("") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="badd7-113">If the function fails, this parameter is set to the empty string ("").</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="badd7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="badd7-114">Return value</span></span>

<span data-ttu-id="badd7-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="badd7-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="badd7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="badd7-116">Requirements</span></span>



| <span data-ttu-id="badd7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="badd7-117">Requirement</span></span> | <span data-ttu-id="badd7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="badd7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="badd7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="badd7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="badd7-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="badd7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="badd7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="badd7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="badd7-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="badd7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="badd7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="badd7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="badd7-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="badd7-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="badd7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="badd7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="badd7-126">**Sdbinitdatabase**</span><span class="sxs-lookup"><span data-stu-id="badd7-126">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




