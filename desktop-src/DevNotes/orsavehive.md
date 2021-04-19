---
description: Schreibt die angegebene Offline Registrierungs Struktur in eine Datei.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Orsavehive-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370564"
---
# <a name="orsavehive-function"></a><span data-ttu-id="21c0e-103">Orsavehive-Funktion</span><span class="sxs-lookup"><span data-stu-id="21c0e-103">ORSaveHive function</span></span>

<span data-ttu-id="21c0e-104">Schreibt die angegebene Offline Registrierungs Struktur in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="21c0e-104">Writes the specified offline registry hive to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="21c0e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21c0e-105">Syntax</span></span>


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="21c0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21c0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21c0e-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21c0e-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c0e-108">Ein Handle für die zu speichernde Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="21c0e-108">A handle to the offline registry hive to save.</span></span>

</dd> <dt>

<span data-ttu-id="21c0e-109">*lphivepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21c0e-109">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c0e-110">Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen der Hive-Registrierungsdatei angibt.</span><span class="sxs-lookup"><span data-stu-id="21c0e-110">A pointer to a Unicode string that specifies the name of the registry hive file.</span></span> <span data-ttu-id="21c0e-111">Dabei kann es sich nicht um den Namen einer vorhandenen Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="21c0e-111">This cannot be the name of an existing file.</span></span>

</dd> <dt>

<span data-ttu-id="21c0e-112">*dwOSMajorVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21c0e-112">*dwOsMajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c0e-113">Die Hauptversionsnummer des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="21c0e-113">The major version number of the operating system.</span></span> <span data-ttu-id="21c0e-114">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="21c0e-114">This member can be one of the following values.</span></span>



| <span data-ttu-id="21c0e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="21c0e-115">Value</span></span>                                                                        | <span data-ttu-id="21c0e-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="21c0e-116">Meaning</span></span>                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21c0e-117"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="21c0e-117"><dt>5</dt></span></span> </dl> | <span data-ttu-id="21c0e-118">Wenn *dwOSMinorVersion* den Wert 1 hat, ist das Betriebssystem Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21c0e-118">If *dwOsMinorVersion* is 1, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="21c0e-119">Wenn *dwOSMinorVersion* 2 ist, ist das Betriebssystem Windows Server 2003 R2, Windows Server 2003 oder Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="21c0e-119">If *dwOsMinorVersion* is 2, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span><br/> |
| <dl> <span data-ttu-id="21c0e-120"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="21c0e-120"><dt>6</dt></span></span> </dl> | <span data-ttu-id="21c0e-121">Wenn *dwOSMinorVersion* den Wert 0 hat, ist das Betriebssystem Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="21c0e-121">If *dwOsMinorVersion* is 0, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/> <span data-ttu-id="21c0e-122">Wenn *dwOSMinorVersion* den Wert 1 hat, ist das Betriebssystem Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="21c0e-122">If *dwOsMinorVersion* is 1, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="21c0e-123">*dwOSMinorVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21c0e-123">*dwOsMinorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c0e-124">Die neben Versionsnummer des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="21c0e-124">The minor version number of the operating system.</span></span> <span data-ttu-id="21c0e-125">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="21c0e-125">This member can be one of the following values.</span></span>



| <span data-ttu-id="21c0e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="21c0e-126">Value</span></span>                                                                        | <span data-ttu-id="21c0e-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="21c0e-127">Meaning</span></span>                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21c0e-128"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="21c0e-128"><dt>0</dt></span></span> </dl> | <span data-ttu-id="21c0e-129">Wenn *dwOSMajorVersion* den Wert 6 hat, ist das Betriebssystem Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="21c0e-129">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="21c0e-130"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="21c0e-130"><dt>1</dt></span></span> </dl> | <span data-ttu-id="21c0e-131">Wenn *dwOSMajorVersion* den Wert 5 hat, ist das Betriebssystem Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21c0e-131">If *dwOsMajorVersion* is 5, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="21c0e-132">Wenn *dwOSMajorVersion* den Wert 6 hat, ist das Betriebssystem Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="21c0e-132">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="21c0e-133"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="21c0e-133"><dt>2</dt></span></span> </dl> | <span data-ttu-id="21c0e-134">Wenn *dwOSMajorVersion* den Wert 5 hat, ist das Betriebssystem Windows Server 2003 R2, Windows Server 2003 oder Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="21c0e-134">If *dwOsMajorVersion* is 5, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span> <br/> <span data-ttu-id="21c0e-135">Wenn *dwOSMajorVersion* den Wert 6 hat, muss der *dwOSMinorVersion* -Parameter den Wert 0 oder 1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="21c0e-135">If *dwOsMajorVersion* is 6, the *dwOsMinorVersion* parameter must be 0 or 1.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21c0e-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21c0e-136">Return value</span></span>

<span data-ttu-id="21c0e-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="21c0e-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="21c0e-138">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="21c0e-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="21c0e-139">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="21c0e-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="21c0e-140">Folgende Fehlercodes sind möglich:</span><span class="sxs-lookup"><span data-stu-id="21c0e-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="21c0e-141">Wenn der Aufrufer nicht über die erforderlichen Zugriffsrechte zum Schreiben der Datei verfügt, gibt die Funktion den Fehler \_ Zugriff \_ verweigert zurück.</span><span class="sxs-lookup"><span data-stu-id="21c0e-141">If the caller does not have the necessary access rights to write the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="21c0e-142">Wenn die angegebene Datei bereits vorhanden ist, gibt die Funktion einen Fehler zurück \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="21c0e-142">If the specified file already exists, the function returns ERROR\_ALREADY\_EXISTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="21c0e-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21c0e-143">Remarks</span></span>

<span data-ttu-id="21c0e-144">Die **orsavehive** -Funktion muss verwendet werden, um an einer Offline Registrierungs Struktur vorgenommene Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="21c0e-144">The **ORSaveHive** function must be used to save changes made to an offline registry hive.</span></span> <span data-ttu-id="21c0e-145">Änderungen werden nicht beibehalten, bis **orsavehive** aufgerufen wird, um die Struktur in einer Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="21c0e-145">Changes are not preserved until **ORSaveHive** is called to save the hive to a file.</span></span>

<span data-ttu-id="21c0e-146">Die Parameter *dwOSMajorVersion* und *dwOSMinorVersion* geben das Zielformat der Hive-Registrierungsdatei an.</span><span class="sxs-lookup"><span data-stu-id="21c0e-146">The *dwOsMajorVersion* and *dwOsMinorVersion* parameters together specify the target format of the registry hive file.</span></span> <span data-ttu-id="21c0e-147">In der folgenden Tabelle werden die aktuellen Versionsnummern des Betriebssystems zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="21c0e-147">The following table summarizes the most recent operating system version numbers.</span></span>



| <span data-ttu-id="21c0e-148">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="21c0e-148">Operating system</span></span>                    | <span data-ttu-id="21c0e-149">Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="21c0e-149">Version number</span></span> |
|-------------------------------------|----------------|
| <span data-ttu-id="21c0e-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21c0e-150">Windows Server 2008 R2</span></span>              | <span data-ttu-id="21c0e-151">6.1</span><span class="sxs-lookup"><span data-stu-id="21c0e-151">6.1</span></span>            |
| <span data-ttu-id="21c0e-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="21c0e-152">Windows 7</span></span>                           | <span data-ttu-id="21c0e-153">6.1</span><span class="sxs-lookup"><span data-stu-id="21c0e-153">6.1</span></span>            |
| <span data-ttu-id="21c0e-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21c0e-154">Windows Server 2008</span></span>                 | <span data-ttu-id="21c0e-155">6.0</span><span class="sxs-lookup"><span data-stu-id="21c0e-155">6.0</span></span>            |
| <span data-ttu-id="21c0e-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21c0e-156">Windows Vista</span></span>                       | <span data-ttu-id="21c0e-157">6.0</span><span class="sxs-lookup"><span data-stu-id="21c0e-157">6.0</span></span>            |
| <span data-ttu-id="21c0e-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21c0e-158">Windows Server 2003 R2</span></span>              | <span data-ttu-id="21c0e-159">5,2</span><span class="sxs-lookup"><span data-stu-id="21c0e-159">5.2</span></span>            |
| <span data-ttu-id="21c0e-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21c0e-160">Windows Server 2003</span></span>                 | <span data-ttu-id="21c0e-161">5,2</span><span class="sxs-lookup"><span data-stu-id="21c0e-161">5.2</span></span>            |
| <span data-ttu-id="21c0e-162">Windows XP Professional x64 Edition</span><span class="sxs-lookup"><span data-stu-id="21c0e-162">Windows XP Professional x64 Edition</span></span> | <span data-ttu-id="21c0e-163">5,2</span><span class="sxs-lookup"><span data-stu-id="21c0e-163">5.2</span></span>            |
| <span data-ttu-id="21c0e-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="21c0e-164">Windows XP</span></span>                          | <span data-ttu-id="21c0e-165">5,1</span><span class="sxs-lookup"><span data-stu-id="21c0e-165">5.1</span></span>            |



 

<span data-ttu-id="21c0e-166">Verwenden Sie die Funktion [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) zum Abrufen von Informationen zum aktuellen Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="21c0e-166">Use the [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function to retrieve information about the current operating system.</span></span>

<span data-ttu-id="21c0e-167">Die **orsavehive** -Funktion sperrt die Registrierungs Struktur, während Sie die Struktur in die Datei schreibt, schließt dann die Datei und gibt die Sperre frei.</span><span class="sxs-lookup"><span data-stu-id="21c0e-167">The **ORSaveHive** function locks the registry hive while it is writing the hive to the file, then closes the file and releases the lock.</span></span> <span data-ttu-id="21c0e-168">Die Registrierungs Struktur verbleibt im Arbeitsspeicher, bis Sie durch Aufrufen der [**orclosehive**](orclosehive.md) -Funktion geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="21c0e-168">The registry hive remains in memory until it is closed by calling the [**ORCloseHive**](orclosehive.md) function.</span></span> <span data-ttu-id="21c0e-169">Es ist möglich, Änderungen an der Registrierungs Struktur vorzunehmen, während Sie geöffnet ist. um diese Änderungen beizubehalten, muss die Struktur jedoch in einer neuen Datei gespeichert werden, da die **orsavehive** -Funktion eine vorhandene Datei nicht überschreibt.</span><span class="sxs-lookup"><span data-stu-id="21c0e-169">It is possible to make further changes to the registry hive while it is open; however, to preserve these changes the hive must be saved to a new file, because the **ORSaveHive** function will not overwrite an existing file.</span></span>

<span data-ttu-id="21c0e-170">Die **orsavehive** -Funktion kann verwendet werden, um einen Teil der Offline Registrierungs Struktur zu speichern.</span><span class="sxs-lookup"><span data-stu-id="21c0e-170">The **ORSaveHive** function can be used to save part of the offline registry hive.</span></span> <span data-ttu-id="21c0e-171">Der im *handle* -Parameter angegebene Schlüssel wird zum Stamm Schlüssel einer Struktur, die aus dem angegebenen Schlüssel und den zugehörigen unter Schlüsseln besteht.</span><span class="sxs-lookup"><span data-stu-id="21c0e-171">The key specified in the *Handle* parameter becomes the root key of a hive that consists of the specified key and all of its subkeys.</span></span>

## <a name="requirements"></a><span data-ttu-id="21c0e-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21c0e-172">Requirements</span></span>



| <span data-ttu-id="21c0e-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21c0e-173">Requirement</span></span> | <span data-ttu-id="21c0e-174">Wert</span><span class="sxs-lookup"><span data-stu-id="21c0e-174">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21c0e-175">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="21c0e-175">Redistributable</span></span><br/> | <span data-ttu-id="21c0e-176">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="21c0e-176">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="21c0e-177">Header</span><span class="sxs-lookup"><span data-stu-id="21c0e-177">Header</span></span><br/>          | <dl> <span data-ttu-id="21c0e-178"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="21c0e-178"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="21c0e-179">DLL</span><span class="sxs-lookup"><span data-stu-id="21c0e-179">DLL</span></span><br/>             | <dl> <span data-ttu-id="21c0e-180"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21c0e-180"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21c0e-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21c0e-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c0e-182">GetVersionEx</span><span class="sxs-lookup"><span data-stu-id="21c0e-182">GetVersionEx</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[<span data-ttu-id="21c0e-183">**Orclosehive**</span><span class="sxs-lookup"><span data-stu-id="21c0e-183">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="21c0e-184">**Oropenhive**</span><span class="sxs-lookup"><span data-stu-id="21c0e-184">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
