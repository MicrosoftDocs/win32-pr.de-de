---
description: Entfernt einen benannten Wert aus dem angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Ordeletevalue-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372693"
---
# <a name="ordeletevalue-function"></a><span data-ttu-id="a10d3-103">Ordeletevalue-Funktion</span><span class="sxs-lookup"><span data-stu-id="a10d3-103">ORDeleteValue function</span></span>

<span data-ttu-id="a10d3-104">Entfernt einen benannten Wert aus dem angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="a10d3-104">Removes a named value from the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a10d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a10d3-105">Syntax</span></span>


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a><span data-ttu-id="a10d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a10d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a10d3-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a10d3-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a10d3-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="a10d3-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="a10d3-109">*lpvaluename* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a10d3-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a10d3-110">Der zu entfernende Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="a10d3-110">The registry value to be removed.</span></span> <span data-ttu-id="a10d3-111">Wenn dieser Parameter **null** oder eine leere Zeichenfolge ist, wird der von der [**orsetvalue**](orsetvalue.md) -Funktion festgelegte unbenannte Standardwert entfernt.</span><span class="sxs-lookup"><span data-stu-id="a10d3-111">If this parameter is **NULL** or an empty string, the default unnamed value set by the [**ORSetValue**](orsetvalue.md) function is removed.</span></span>

<span data-ttu-id="a10d3-112">Bei Werten Namen wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="a10d3-112">Value names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a10d3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a10d3-113">Return value</span></span>

<span data-ttu-id="a10d3-114">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a10d3-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a10d3-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a10d3-115">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="a10d3-116">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a10d3-116">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a10d3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a10d3-117">Requirements</span></span>



| <span data-ttu-id="a10d3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a10d3-118">Requirement</span></span> | <span data-ttu-id="a10d3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a10d3-119">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a10d3-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a10d3-120">Redistributable</span></span><br/> | <span data-ttu-id="a10d3-121">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a10d3-121">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="a10d3-122">Header</span><span class="sxs-lookup"><span data-stu-id="a10d3-122">Header</span></span><br/>          | <dl> <span data-ttu-id="a10d3-123"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a10d3-123"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="a10d3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a10d3-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="a10d3-125"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a10d3-125"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a10d3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a10d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a10d3-127">**Orsetvalue**</span><span class="sxs-lookup"><span data-stu-id="a10d3-127">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
