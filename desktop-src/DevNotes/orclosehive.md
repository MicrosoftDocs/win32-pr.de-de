---
description: Schließt die angegebene Offline Registrierungs Struktur und gibt für die Hive zugeordnete Arbeitsspeicher frei.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Orclosehive-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370297"
---
# <a name="orclosehive-function"></a><span data-ttu-id="807e8-103">Orclosehive-Funktion</span><span class="sxs-lookup"><span data-stu-id="807e8-103">ORCloseHive function</span></span>

<span data-ttu-id="807e8-104">Schließt die angegebene Offline Registrierungs Struktur und gibt für die Hive zugeordnete Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="807e8-104">Closes the specified offline registry hive and frees memory allocated for the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="807e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="807e8-105">Syntax</span></span>


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="807e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="807e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="807e8-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="807e8-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="807e8-108">Ein Handle für den Stamm Schlüssel der zu schließenden Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="807e8-108">A handle to the root key of the offline registry hive to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="807e8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="807e8-109">Return value</span></span>

<span data-ttu-id="807e8-110">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="807e8-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="807e8-111">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="807e8-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="807e8-112">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="807e8-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="807e8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="807e8-113">Remarks</span></span>

<span data-ttu-id="807e8-114">Die **orclosehive** -Funktion gibt den gesamten Arbeitsspeicher frei, der von den Offline Registrierungsfunktionen für die angegebene Hive reserviert wurde.</span><span class="sxs-lookup"><span data-stu-id="807e8-114">The **ORCloseHive** function frees all memory allocated by the offline registry functions on behalf of the specified hive.</span></span>

<span data-ttu-id="807e8-115">Um Änderungen an der Struktur beizubehalten, rufen Sie die [**orsavehive**](orsavehive.md) -Funktion auf, bevor Sie **orclosehive** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="807e8-115">To preserve changes to the hive, call the [**ORSaveHive**](orsavehive.md) function before calling **ORCloseHive**.</span></span>

## <a name="requirements"></a><span data-ttu-id="807e8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="807e8-116">Requirements</span></span>



| <span data-ttu-id="807e8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="807e8-117">Requirement</span></span> | <span data-ttu-id="807e8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="807e8-118">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="807e8-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="807e8-119">Redistributable</span></span><br/> | <span data-ttu-id="807e8-120">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="807e8-120">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="807e8-121">Header</span><span class="sxs-lookup"><span data-stu-id="807e8-121">Header</span></span><br/>          | <dl> <span data-ttu-id="807e8-122"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-122"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="807e8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="807e8-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="807e8-124"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-124"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="807e8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="807e8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="807e8-126">**Oropenhive**</span><span class="sxs-lookup"><span data-stu-id="807e8-126">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="807e8-127">**Orsavehive**</span><span class="sxs-lookup"><span data-stu-id="807e8-127">**ORSaveHive**</span></span>](orsavehive.md)
</dt> </dl>

 

 
