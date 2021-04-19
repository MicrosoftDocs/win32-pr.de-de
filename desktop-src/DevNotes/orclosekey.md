---
description: Schließt ein Handle für den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: Orclosekey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372694"
---
# <a name="orclosekey-function"></a><span data-ttu-id="eb102-103">Orclosekey-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb102-103">ORCloseKey function</span></span>

<span data-ttu-id="eb102-104">Schließt ein Handle für den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="eb102-104">Closes a handle to the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb102-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb102-105">Syntax</span></span>


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="eb102-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb102-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb102-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb102-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb102-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="eb102-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb102-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb102-109">Return value</span></span>

<span data-ttu-id="eb102-110">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="eb102-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="eb102-111">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb102-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="eb102-112">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb102-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="eb102-113">Wenn der angegebene Schlüssel der Stamm Schlüssel der Registrierungs Struktur ist, schlägt die Funktion mit einem \_ ungültigen \_ Parameter fehl.</span><span class="sxs-lookup"><span data-stu-id="eb102-113">If the specified key is the root key of the registry hive, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb102-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb102-114">Remarks</span></span>

<span data-ttu-id="eb102-115">Das Handle für einen angegebenen Schlüssel sollte nicht verwendet werden, nachdem es geschlossen wurde, da es nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="eb102-115">The handle for a specified key should not be used after it has been closed, because it will no longer be valid.</span></span> <span data-ttu-id="eb102-116">Schlüssel Handles sollten nicht länger als erforderlich geöffnet bleiben.</span><span class="sxs-lookup"><span data-stu-id="eb102-116">Key handles should not be left open any longer than necessary.</span></span>

<span data-ttu-id="eb102-117">Verwenden Sie die [**orclosehive**](orclosehive.md) -Funktion, um eine Offline Registrierungs Struktur zu schließen.</span><span class="sxs-lookup"><span data-stu-id="eb102-117">Use the [**ORCloseHive**](orclosehive.md) function to close an offline registry hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb102-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb102-118">Requirements</span></span>



| <span data-ttu-id="eb102-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb102-119">Requirement</span></span> | <span data-ttu-id="eb102-120">Wert</span><span class="sxs-lookup"><span data-stu-id="eb102-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb102-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="eb102-121">Redistributable</span></span><br/> | <span data-ttu-id="eb102-122">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="eb102-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="eb102-123">Header</span><span class="sxs-lookup"><span data-stu-id="eb102-123">Header</span></span><br/>          | <dl> <span data-ttu-id="eb102-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb102-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb102-125">DLL</span><span class="sxs-lookup"><span data-stu-id="eb102-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="eb102-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb102-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb102-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb102-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb102-128">**Orclosehive**</span><span class="sxs-lookup"><span data-stu-id="eb102-128">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="eb102-129">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="eb102-129">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="eb102-130">**Ordeletekey**</span><span class="sxs-lookup"><span data-stu-id="eb102-130">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="eb102-131">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="eb102-131">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
