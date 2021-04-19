---
description: Ruft die virtuellen Flags für den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur ab.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: Orgetvirtualflags-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 36c41bb9e510a107689790162e03e3bb86c8de1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370175"
---
# <a name="orgetvirtualflags-function"></a><span data-ttu-id="a5e11-103">Orgetvirtualflags-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5e11-103">ORGetVirtualFlags function</span></span>

<span data-ttu-id="a5e11-104">Ruft die virtuellen Flags für den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="a5e11-104">Retrieves the virtual flags on the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5e11-105">Syntax</span></span>


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a5e11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5e11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e11-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5e11-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e11-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="a5e11-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="a5e11-109">*pdwflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a5e11-109">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e11-110">Ein Zeiger auf eine Variable, die die für den Schlüssel festgelegten virtualisierungsflags empfängt.</span><span class="sxs-lookup"><span data-stu-id="a5e11-110">A pointer to a variable to receive the virtualization flags set for the key.</span></span> <span data-ttu-id="a5e11-111">Nachdem die Funktion zurückgegeben wurde, kann dieser Parameter einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a5e11-111">After the function returns, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a5e11-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a5e11-112">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="a5e11-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a5e11-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <span data-ttu-id="a5e11-114"><dt>**Reg \_ Schlüssel \_ \_ \_ nicht**</dt> unbeaufsichtigt Fehler <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a5e11-114"><dt>**REG\_KEY\_DONT\_SILENT\_FAIL**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="a5e11-115">Wenn dieses Flag festgelegt ist und ein Öffnungsvorgang für einen Schlüssel mit aktivierter Virtualisierung fehlschlägt, versucht die Registrierung nicht, den Schlüssel erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a5e11-115">If this flag is set and an Open operation fails on a key that has virtualization enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="a5e11-116">Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel mit dem maximal \_ zulässigen Zugriff erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a5e11-116">If this flag is clear, the registry attempts to reopen the key with MAXIMUM\_ALLOWED access.</span></span><br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <span data-ttu-id="a5e11-117"><dt>**Reg \_ Schlüssel \_ nicht \_ virtualisieren**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a5e11-117"><dt>**REG\_KEY\_DONT\_VIRTUALIZE**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="a5e11-118">Wenn dieses Flag festgelegt ist und ein Create Key-Vorgang fehlschlägt, da der Aufrufer nicht über den Key \_ Create \_ Sub Key-Schlüssel \_ für den übergeordneten Schlüssel verfügt, schlägt die Registrierung den Erstellungs Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="a5e11-118">If this flag is set and a Create Key operation fails because the caller does not have the KEY\_CREATE\_SUB\_KEY right on the parent key, the registry fails the Create operation.</span></span> <span data-ttu-id="a5e11-119">Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel im virtuellen Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a5e11-119">If this flag is clear, the registry attempts to create the key in the virtual store.</span></span> <span data-ttu-id="a5e11-120">Der Aufrufer muss über die Berechtigung zum Lesen des Schlüssels \_ für den übergeordneten Schlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="a5e11-120">The caller must have the KEY\_READ right on the parent key.</span></span><br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <span data-ttu-id="a5e11-121"><dt>**Reg \_ Key \_ recurse- \_ Flag**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a5e11-121"><dt>**REG\_KEY\_RECURSE\_FLAG**</dt> <dt>8</dt></span></span> </dl>              | <span data-ttu-id="a5e11-122">Wenn dieses Flag festgelegt ist, werden registrierungsvirtualisierungsflags aus dem übergeordneten Schlüssel weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="a5e11-122">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="a5e11-123">Wenn dieses Flag eindeutig ist, werden die registrierungsvirtualisierungsflags nicht weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="a5e11-123">If this flag is clear, registry virtualization flags are not propagated.</span></span><br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5e11-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5e11-124">Return value</span></span>

<span data-ttu-id="a5e11-125">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a5e11-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a5e11-126">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a5e11-126">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="a5e11-127">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a5e11-127">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e11-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5e11-128">Remarks</span></span>

<span data-ttu-id="a5e11-129">Die Registrierungsvirtualisierung ist eine zwischen Anwendungskompatibilitäts-Technologie, die es ermöglicht, Registrierungs Schreibvorgänge mit globaler Auswirkung an benutzerspezifische Speicherorte umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="a5e11-129">Registry virtualization is an interim application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="a5e11-130">Diese Umleitung ist für Anwendungen transparent, die aus der Registrierung lesen oder in diese schreiben.</span><span class="sxs-lookup"><span data-stu-id="a5e11-130">This redirection is transparent to applications reading from or writing to the registry.</span></span>

<span data-ttu-id="a5e11-131">Die Registrierungsvirtualisierung wird ab Windows Vista unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5e11-131">Registry virtualization is supported starting with Windows Vista.</span></span> <span data-ttu-id="a5e11-132">Microsoft beabsichtigt jedoch, Sie aus zukünftigen Versionen des Windows-Betriebssystems zu entfernen, da mehr Anwendungen mit Windows Vista kompatibel gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="a5e11-132">However, Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista.</span></span> <span data-ttu-id="a5e11-133">Daher sollten Anwendungen nicht vom Verhalten der Registrierungsvirtualisierung im System abhängen.</span><span class="sxs-lookup"><span data-stu-id="a5e11-133">Therefore, applications should not depend on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="a5e11-134">Die Registrierungsvirtualisierung ist nur für Folgendes aktiviert:</span><span class="sxs-lookup"><span data-stu-id="a5e11-134">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="a5e11-135">interaktive 32-Bit-Prozesse</span><span class="sxs-lookup"><span data-stu-id="a5e11-135">32-bit interactive processes</span></span>
-   <span data-ttu-id="a5e11-136">Schlüssel in **HKEY \_ - \_ \\ Software für lokale Computer**</span><span class="sxs-lookup"><span data-stu-id="a5e11-136">Keys in **HKEY\_LOCAL\_MACHINE\\Software**</span></span>
-   <span data-ttu-id="a5e11-137">Schlüssel, in die ein Administrator schreiben kann</span><span class="sxs-lookup"><span data-stu-id="a5e11-137">Keys that an administrator can write to</span></span>

<span data-ttu-id="a5e11-138">Weitere Informationen finden Sie unter [Registrierungsvirtualisierung](../sysinfo/registry-virtualization.md).</span><span class="sxs-lookup"><span data-stu-id="a5e11-138">For more information, see [Registry Virtualization](../sysinfo/registry-virtualization.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e11-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5e11-139">Requirements</span></span>



| <span data-ttu-id="a5e11-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5e11-140">Requirement</span></span> | <span data-ttu-id="a5e11-141">Wert</span><span class="sxs-lookup"><span data-stu-id="a5e11-141">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e11-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a5e11-142">Redistributable</span></span><br/> | <span data-ttu-id="a5e11-143">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a5e11-143">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="a5e11-144">Header</span><span class="sxs-lookup"><span data-stu-id="a5e11-144">Header</span></span><br/>          | <dl> <span data-ttu-id="a5e11-145"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5e11-145"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5e11-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a5e11-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="a5e11-147"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5e11-147"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5e11-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5e11-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e11-149">**Orsetvirtualflags**</span><span class="sxs-lookup"><span data-stu-id="a5e11-149">**ORSetVirtualFlags**</span></span>](orsetvirtualflags.md)
</dt> <dt>

[<span data-ttu-id="a5e11-150">Registrierungsvirtualisierung</span><span class="sxs-lookup"><span data-stu-id="a5e11-150">Registry Virtualization</span></span>](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
