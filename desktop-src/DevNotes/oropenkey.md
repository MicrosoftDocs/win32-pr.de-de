---
description: Öffnet den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Oropenkey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358709"
---
# <a name="oropenkey-function"></a><span data-ttu-id="3e180-103">Oropenkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="3e180-103">OROpenKey function</span></span>

<span data-ttu-id="3e180-104">Öffnet den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="3e180-104">Opens the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e180-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e180-105">Syntax</span></span>


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="3e180-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e180-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e180-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="3e180-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="3e180-109">*lpsubkeyname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3e180-109">*lpSubKeyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-110">Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen des zu öffnenden Registrierungsschlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="3e180-110">A pointer to a UNICODE string that contains the name of the registry key to be opened.</span></span> <span data-ttu-id="3e180-111">Dieser Schlüssel muss ein Unterschlüssel des Schlüssels sein, der durch den *handle* -Parameter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3e180-111">This key must be a subkey of the key identified by the *Handle* parameter.</span></span>

<span data-ttu-id="3e180-112">Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="3e180-112">Key names are not case sensitive.</span></span>

<span data-ttu-id="3e180-113">Wenn dieser Parameter **null** ist oder ein Zeiger auf eine leere Zeichenfolge ist, gibt die Funktion das gleiche Handle zurück, das übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3e180-113">If this parameter is **NULL** or a pointer to an empty string, the function returns the same handle that was passed in.</span></span> <span data-ttu-id="3e180-114">Wenn der vom *handle* -Parameter angegebene Schlüssel der Stamm Schlüssel der Hive ist, gibt die Funktion einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="3e180-114">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="3e180-115">Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="3e180-115">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e180-116">*phkResult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e180-116">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-117">Ein Zeiger auf eine Variable, die ein Handle für den geöffneten Schlüssel empfängt.</span><span class="sxs-lookup"><span data-stu-id="3e180-117">A pointer to a variable that receives a handle to the opened key.</span></span> <span data-ttu-id="3e180-118">Verwenden Sie die [**orclosekey**](orclosekey.md) -Funktion, um den Schlüssel zu schließen, nachdem Sie die Verwendung des Handles abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="3e180-118">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e180-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e180-119">Return value</span></span>

<span data-ttu-id="3e180-120">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3e180-120">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3e180-121">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3e180-121">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="3e180-122">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3e180-122">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="3e180-123">Wenn das zurück zugegende Handle ein Handle für den Stamm Schlüssel der Hive wäre, gibt die Funktion einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="3e180-123">If the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="3e180-124">Wenn der angegebene Schlüssel als gelöscht markiert wurde, gibt diese Funktion den \_ gelöschten Fehler Schlüssel zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="3e180-124">If the specified key has been marked as deleted, this function returns ERROR\_KEY\_DELETED.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e180-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e180-125">Remarks</span></span>

<span data-ttu-id="3e180-126">Die **oropenkey** -Funktion kann nicht verwendet werden, um den Stamm Schlüssel in einer Offline Registrierungs Struktur zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3e180-126">The **OROpenKey** function cannot be used to open the root key in an offline registry hive.</span></span> <span data-ttu-id="3e180-127">Zum Abrufen eines Handles für den Stamm Schlüssel einer Hive verwenden Sie die [**oropenhive**](oropenhive.md) -Funktion, um die Struktur in den Arbeitsspeicher zu laden.</span><span class="sxs-lookup"><span data-stu-id="3e180-127">To obtain a handle to the root key of a hive, use the [**OROpenHive**](oropenhive.md) function to load the hive into memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e180-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e180-128">Requirements</span></span>



| <span data-ttu-id="3e180-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e180-129">Requirement</span></span> | <span data-ttu-id="3e180-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3e180-130">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e180-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3e180-131">Redistributable</span></span><br/> | <span data-ttu-id="3e180-132">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3e180-132">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="3e180-133">Header</span><span class="sxs-lookup"><span data-stu-id="3e180-133">Header</span></span><br/>          | <dl> <span data-ttu-id="3e180-134"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e180-134"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e180-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3e180-135">DLL</span></span><br/>             | <dl> <span data-ttu-id="3e180-136"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e180-136"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e180-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e180-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e180-138">**Orclosekey**</span><span class="sxs-lookup"><span data-stu-id="3e180-138">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="3e180-139">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="3e180-139">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="3e180-140">**Ordeletekey**</span><span class="sxs-lookup"><span data-stu-id="3e180-140">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="3e180-141">**Oropenhive**</span><span class="sxs-lookup"><span data-stu-id="3e180-141">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
