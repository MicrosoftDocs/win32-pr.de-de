---
description: Löscht einen Unterschlüssel und seine Werte aus einer Offline Registrierungs Struktur.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Ordeletekey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367768"
---
# <a name="ordeletekey-function"></a><span data-ttu-id="c7f10-103">Ordeletekey-Funktion</span><span class="sxs-lookup"><span data-stu-id="c7f10-103">ORDeleteKey function</span></span>

<span data-ttu-id="c7f10-104">Löscht einen Unterschlüssel und seine Werte aus einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="c7f10-104">Deletes a subkey and its values from an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7f10-105">Syntax</span></span>


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a><span data-ttu-id="c7f10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7f10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7f10-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7f10-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f10-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="c7f10-108">A handle to an open registry key in an offline registry hive.</span></span> <span data-ttu-id="c7f10-109">Dieses Handle wird von der [**orkreatekey**](orcreatekey.md) -Funktion oder der [**oropenkey**](oropenkey.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c7f10-109">This handle is returned by the [**ORCreateKey**](orcreatekey.md) or [**OROpenKey**](oropenkey.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c7f10-110">*lpsubkey* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c7f10-110">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f10-111">Der Name des zu löschenden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c7f10-111">The name of the key to be deleted.</span></span> <span data-ttu-id="c7f10-112">Dabei muss es sich um einen Unterschlüssel des Schlüssels handeln, der von *behandelt* wird, es können jedoch keine Unterschlüssel vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c7f10-112">It must be a subkey of the key that *Handle* identifies, but it cannot have subkeys.</span></span>

<span data-ttu-id="c7f10-113">Wenn der Unterschlüssel nicht vorhanden ist, gibt die Funktion einen Fehler zurück, der \_ nicht \_ gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c7f10-113">If the subkey does not exist, the function returns ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="c7f10-114">Wenn dieser Parameter **null** ist, löscht die Funktion den Schlüssel, der durch den *handle* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c7f10-114">If this parameter is **NULL**, the function deletes the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="c7f10-115">Wenn der vom *handle* -Parameter angegebene Schlüssel der Stamm Schlüssel der Hive ist, gibt die Funktion einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="c7f10-115">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="c7f10-116">Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="c7f10-116">Key names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7f10-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7f10-117">Return value</span></span>

<span data-ttu-id="c7f10-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c7f10-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c7f10-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c7f10-119">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="c7f10-120">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7f10-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="c7f10-121">Folgende Fehlercodes sind möglich:</span><span class="sxs-lookup"><span data-stu-id="c7f10-121">Possible error codes include the following:</span></span>

-   <span data-ttu-id="c7f10-122">Wenn der angegebene Unterschlüssel nicht vorhanden ist, gibt die Funktion die Fehler \_ Datei \_ nicht gefunden zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="c7f10-122">If the specified subkey does not exist, the function returns ERROR\_FILE\_NOT\_FOUND.</span></span>
-   <span data-ttu-id="c7f10-123">Wenn der angegebene Unterschlüssel der Stamm Schlüssel der Registrierungs Struktur ist, gibt die Funktion einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="c7f10-123">If the specified subkey is the root key of the registry hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>
-   <span data-ttu-id="c7f10-124">Wenn der angegebene Unterschlüssel über Unterschlüssel verfügt, gibt die Funktion einen untergeordneten Schlüssel zurück \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c7f10-124">If the specified subkey has subkeys, the function returns ERROR\_KEY\_HAS\_CHILDREN.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7f10-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7f10-125">Remarks</span></span>

<span data-ttu-id="c7f10-126">Wenn der angegebene Registrierungsschlüssel vorhanden ist, wird er als gelöscht markiert.</span><span class="sxs-lookup"><span data-stu-id="c7f10-126">If the specified registry key exists, it is marked as deleted.</span></span> <span data-ttu-id="c7f10-127">Ein gelöschter Schlüssel wird erst entfernt, wenn das letzte Handle geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c7f10-127">A deleted key is not removed until the last handle to it is closed.</span></span>

<span data-ttu-id="c7f10-128">Der zu löschende Schlüssel darf keine Unterschlüssel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c7f10-128">The key to be deleted must not have subkeys.</span></span> <span data-ttu-id="c7f10-129">Um einen Schlüssel und alle zugehörigen Unterschlüssel zu löschen, verwenden Sie die Funktion " [**orenkey**](orenumkey.md) ", um die Unterschlüssel aufzulisten und Sie einzeln zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c7f10-129">To delete a key and all its subkeys, use the [**OREnumKey**](orenumkey.md) function to enumerate the subkeys and delete them individually.</span></span>

<span data-ttu-id="c7f10-130">Nur die [**orclosekey**](orclosekey.md) -Funktion kann für einen gelöschten Schlüssel aufgerufen werden. alle anderen offline Registrierungs Vorgänge können nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c7f10-130">Only the [**ORCloseKey**](orclosekey.md) function may be called on a deleted key; all other offline registry operations fail.</span></span> <span data-ttu-id="c7f10-131">Wenn der gelöschte Schlüssel explizit durch Aufrufen von [**orcreatekey**](orcreatekey.md)erstellt wurde, werden die dem Schlüssel zugeordneten Ressourcen freigegeben, wenn das letzte Handle für den gelöschten Schlüssel geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c7f10-131">If the deleted key was explicitly created by calling [**ORCreateKey**](orcreatekey.md), resources associated with the key are released when the last handle to the deleted key is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7f10-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7f10-132">Requirements</span></span>



| <span data-ttu-id="c7f10-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7f10-133">Requirement</span></span> | <span data-ttu-id="c7f10-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c7f10-134">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f10-135">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c7f10-135">Redistributable</span></span><br/> | <span data-ttu-id="c7f10-136">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c7f10-136">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="c7f10-137">Header</span><span class="sxs-lookup"><span data-stu-id="c7f10-137">Header</span></span><br/>          | <dl> <span data-ttu-id="c7f10-138"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7f10-138"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7f10-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c7f10-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="c7f10-140"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7f10-140"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7f10-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7f10-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f10-142">**Orclosekey**</span><span class="sxs-lookup"><span data-stu-id="c7f10-142">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="c7f10-143">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="c7f10-143">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="c7f10-144">**Orenkey**</span><span class="sxs-lookup"><span data-stu-id="c7f10-144">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="c7f10-145">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="c7f10-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
