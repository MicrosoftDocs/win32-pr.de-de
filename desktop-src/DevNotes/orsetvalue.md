---
description: Legt die Daten für den Wert eines angegebenen Registrierungsschlüssels in einer Offline Registrierungs Struktur fest.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Orsetvalue-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371755"
---
# <a name="orsetvalue-function"></a><span data-ttu-id="e82c6-103">Orsetvalue-Funktion</span><span class="sxs-lookup"><span data-stu-id="e82c6-103">ORSetValue function</span></span>

<span data-ttu-id="e82c6-104">Legt die Daten für den Wert eines angegebenen Registrierungsschlüssels in einer Offline Registrierungs Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="e82c6-104">Sets the data for the value of a specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e82c6-105">Syntax</span></span>


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="e82c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e82c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e82c6-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e82c6-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e82c6-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="e82c6-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="e82c6-109">*lpvaluename* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e82c6-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e82c6-110">Der Name des festzulegenden Werts.</span><span class="sxs-lookup"><span data-stu-id="e82c6-110">The name of the value to be set.</span></span> <span data-ttu-id="e82c6-111">Wenn ein Wert mit diesem Namen im Schlüssel nicht bereits vorhanden ist, fügt die Funktion ihn dem Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="e82c6-111">If a value with this name is not already present in the key, the function adds it to the key.</span></span>

<span data-ttu-id="e82c6-112">Wenn *lpvaluename* **null** oder eine leere Zeichenfolge ("") ist, legt die Funktion den Typ und die Daten für den unbenannten oder Standardwert des Schlüssels fest.</span><span class="sxs-lookup"><span data-stu-id="e82c6-112">If *lpValueName* is **NULL** or an empty string, "", the function sets the type and data for the key's unnamed or default value.</span></span>

<span data-ttu-id="e82c6-113">Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="e82c6-113">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="e82c6-114">Registrierungsschlüssel haben keine Standardwerte, Sie können jedoch einen unbenannten Wert aufweisen, der einen beliebigen Typ aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="e82c6-114">Registry keys do not have default values, but they can have one unnamed value, which can be of any type.</span></span>

</dd> <dt>

<span data-ttu-id="e82c6-115">*dwType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e82c6-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e82c6-116">Der Typ der Daten, auf die durch den *lpdata* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e82c6-116">The type of data pointed to by the *lpData* parameter.</span></span> <span data-ttu-id="e82c6-117">Eine Liste der möglichen Typen finden Sie unter [Registrierungs Werttypen](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="e82c6-117">For a list of the possible types, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="e82c6-118">*lpdata* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e82c6-118">*lpData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e82c6-119">Die zu speichernden Daten.</span><span class="sxs-lookup"><span data-stu-id="e82c6-119">The data to be stored.</span></span>

<span data-ttu-id="e82c6-120">Bei Zeichen folgen basierten Typen, z. b. reg \_ SZ, muss die Zeichenfolge mit Null enden.</span><span class="sxs-lookup"><span data-stu-id="e82c6-120">For string-based types, such as REG\_SZ, the string must be null-terminated.</span></span> <span data-ttu-id="e82c6-121">Für den reg \_ \_ MultiSZ-Datentyp muss die Zeichenfolge mit zwei NULL-Zeichen beendet werden.</span><span class="sxs-lookup"><span data-stu-id="e82c6-121">For the REG\_MULTI\_SZ data type, the string must be terminated with two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="e82c6-122">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e82c6-122">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e82c6-123">Die Größe der Informationen, auf die durch den *lpdata* -Parameter verwiesen wird (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="e82c6-123">The size of the information pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="e82c6-124">Wenn die Daten vom Typ reg \_ SZ, reg \_ Expand \_ SZ oder reg \_ \_ MultiSZ sind, müssen *cbData* die Größe des abschließenden NULL-Zeichens oder der Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e82c6-124">If the data is of type REG\_SZ, REG\_EXPAND\_SZ, or REG\_MULTI\_SZ, *cbData* must include the size of the terminating null character or characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e82c6-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e82c6-125">Return value</span></span>

<span data-ttu-id="e82c6-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e82c6-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e82c6-127">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e82c6-127">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="e82c6-128">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e82c6-128">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e82c6-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e82c6-129">Remarks</span></span>

<span data-ttu-id="e82c6-130">Wert Größen werden durch den verfügbaren Arbeitsspeicher begrenzt.</span><span class="sxs-lookup"><span data-stu-id="e82c6-130">Value sizes are limited by available memory.</span></span> <span data-ttu-id="e82c6-131">Lange Werte (mehr als 2048 Bytes) müssen als Dateien mit den Dateinamen gespeichert werden, die in der Registrierung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e82c6-131">Long values (more than 2048 bytes) should be stored as files with the file names stored in the registry.</span></span> <span data-ttu-id="e82c6-132">Dadurch kann die Registrierung effizient durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e82c6-132">This helps the registry perform efficiently.</span></span> <span data-ttu-id="e82c6-133">Anwendungs Elemente wie Symbole, Bitmaps und ausführbare Dateien sollten als Dateien gespeichert und nicht in der Registrierung abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e82c6-133">Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.</span></span>

## <a name="requirements"></a><span data-ttu-id="e82c6-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e82c6-134">Requirements</span></span>



| <span data-ttu-id="e82c6-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e82c6-135">Requirement</span></span> | <span data-ttu-id="e82c6-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e82c6-136">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e82c6-137">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e82c6-137">Redistributable</span></span><br/> | <span data-ttu-id="e82c6-138">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e82c6-138">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="e82c6-139">Header</span><span class="sxs-lookup"><span data-stu-id="e82c6-139">Header</span></span><br/>          | <dl> <span data-ttu-id="e82c6-140"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e82c6-140"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="e82c6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e82c6-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="e82c6-142"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e82c6-142"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e82c6-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e82c6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82c6-144">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="e82c6-144">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="e82c6-145">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="e82c6-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
