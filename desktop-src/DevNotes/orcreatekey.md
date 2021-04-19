---
description: Erstellt den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur. Wenn der Schlüssel bereits vorhanden ist, wird er von der Funktion geöffnet.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Orkreatekey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369226"
---
# <a name="orcreatekey-function"></a><span data-ttu-id="0611e-104">Orkreatekey-Funktion</span><span class="sxs-lookup"><span data-stu-id="0611e-104">ORCreateKey function</span></span>

<span data-ttu-id="0611e-105">Erstellt den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="0611e-105">Creates the specified registry key in an offline registry hive.</span></span> <span data-ttu-id="0611e-106">Wenn der Schlüssel bereits vorhanden ist, wird er von der Funktion geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0611e-106">If the key already exists, the function opens it.</span></span>

## <a name="syntax"></a><span data-ttu-id="0611e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0611e-107">Syntax</span></span>


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a><span data-ttu-id="0611e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0611e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0611e-109">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0611e-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0611e-110">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="0611e-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="0611e-111">*lpsubkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0611e-111">*lpSubKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0611e-112">Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen eines unter Schlüssels enthält, der von dieser Funktion geöffnet oder erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0611e-112">A pointer to a Unicode string that contains the name of a subkey that this function opens or creates.</span></span> <span data-ttu-id="0611e-113">Der *lpsubkey* -Parameter muss einen Unterschlüssel des Schlüssels angeben, der durch den *handle* -Parameter identifiziert wird. Es kann bis zu 32 Ebenen tief in der Registrierungs Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="0611e-113">The *lpSubKey* parameter must specify a subkey of the key identified by the *Handle* parameter; it can be up to 32 levels deep in the registry tree.</span></span> <span data-ttu-id="0611e-114">Weitere Informationen zu Schlüsselnamen finden Sie unter [Struktur der Registrierung](../sysinfo/structure-of-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="0611e-114">For more information about key names, see [Structure of the Registry](../sysinfo/structure-of-the-registry.md).</span></span>

<span data-ttu-id="0611e-115">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0611e-115">This parameter cannot be **NULL**.</span></span>

<span data-ttu-id="0611e-116">Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0611e-116">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="0611e-117">*lpclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0611e-117">*lpClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0611e-118">Die Klasse (Objekttyp) dieses Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="0611e-118">The class (object type) of this key.</span></span> <span data-ttu-id="0611e-119">Dieser Parameter kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="0611e-119">This parameter may be ignored.</span></span> <span data-ttu-id="0611e-120">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="0611e-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0611e-121">*dwOptions* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0611e-121">*dwOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0611e-122">Dieser Parameter kann 0 oder einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="0611e-122">This parameter can be 0 or one of the following values.</span></span>



| <span data-ttu-id="0611e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0611e-123">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="0611e-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0611e-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <span data-ttu-id="0611e-125"><dt>**Reg \_ Option \_ Create \_ Link**</dt> <dt>0x00000002l</dt></span><span class="sxs-lookup"><span data-stu-id="0611e-125"><dt>**REG\_OPTION\_CREATE\_LINK**</dt> <dt>0x00000002L</dt></span></span> </dl>    | <span data-ttu-id="0611e-126">Der Schlüssel ist eine symbolische Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="0611e-126">The key is a symbolic link.</span></span> <span data-ttu-id="0611e-127">Der Zielpfad wird dem L-Wert "symboliclinkvalue" des Schlüssels zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0611e-127">The target path is assigned to the L"SymbolicLinkValue" value of the key.</span></span> <span data-ttu-id="0611e-128">Der Zielpfad muss ein absoluter Registrierungs Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="0611e-128">The target path must be an absolute registry path.</span></span> <span data-ttu-id="0611e-129">Wenn diese Option festgelegt ist, muss auch die **reg \_ Option \_ nicht \_ flüchtig** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0611e-129">If this option is set, **REG\_OPTION\_NON\_VOLATILE** must also be set.</span></span> <br/> <span data-ttu-id="0611e-130">Wenn der *lpsubkey* -Parameter einen vorhandenen Schlüssel angibt, muss er mit der **reg- \_ Option \_ Create \_ Link** erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="0611e-130">If the *lpSubKey* parameter specifies an existing key, it must have been created with **REG\_OPTION\_CREATE\_LINK**.</span></span><br/> <span data-ttu-id="0611e-131">Symbolische Verknüpfungen für die Registrierung sollten nur verwendet werden, wenn die Anwendungs Kompatibilität absolut notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="0611e-131">Registry symbolic links should be used only when absolutely necessary for application compatibility.</span></span> <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <span data-ttu-id="0611e-132"><dt>**Reg \_ Option \_ nicht \_ flüchtig**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="0611e-132"><dt>**REG\_OPTION\_NON\_VOLATILE**</dt> <dt>0x00000000L</dt></span></span> </dl> | <span data-ttu-id="0611e-133">Der Schlüssel ist nicht flüchtig. Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="0611e-133">The key is not volatile; this is the default.</span></span> <span data-ttu-id="0611e-134">Die Informationen werden in einer Datei gespeichert und beibehalten, wenn das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0611e-134">The information is stored in a file and is preserved when the system is restarted.</span></span> <span data-ttu-id="0611e-135">Die [**orsavehive**](orsavehive.md) -Funktion speichert Schlüssel, die nicht flüchtig sind.</span><span class="sxs-lookup"><span data-stu-id="0611e-135">The [**ORSaveHive**](orsavehive.md) function saves keys that are not volatile.</span></span><br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="0611e-136">*psecuritydescriptor* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0611e-136">*pSecurityDescriptor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0611e-137">Ein Zeiger auf eine [Sicherheits \_ deskriptorstruktur](/windows/win32/api/winnt/ns-winnt-security_descriptor) , die eine Sicherheits Beschreibung für den neuen Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="0611e-137">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that contains a security descriptor for the new key.</span></span> <span data-ttu-id="0611e-138">Wenn *psecuritydescriptor* den Wert **null** hat, erhält der Schlüssel eine Standard Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="0611e-138">If *pSecurityDescriptor* is **NULL**, the key gets a default security descriptor.</span></span> <span data-ttu-id="0611e-139">Die ACLs in einer Standard Sicherheits Beschreibung für einen Schlüssel werden von seinem direkten übergeordneten Schlüssel geerbt.</span><span class="sxs-lookup"><span data-stu-id="0611e-139">The ACLs in a default security descriptor for a key are inherited from its direct parent key.</span></span>

</dd> <dt>

<span data-ttu-id="0611e-140">*phkResult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0611e-140">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0611e-141">Ein Zeiger auf eine Variable, die ein Handle für den geöffneten oder erstellten Schlüssel empfängt.</span><span class="sxs-lookup"><span data-stu-id="0611e-141">A pointer to a variable that receives a handle to the opened or created key.</span></span> <span data-ttu-id="0611e-142">Verwenden Sie die [**orclosekey**](orclosekey.md) -Funktion, um den Schlüssel zu schließen, nachdem Sie die Verwendung des Handles abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="0611e-142">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> <dt>

<span data-ttu-id="0611e-143">*pdwdisposition* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="0611e-143">*pdwDisposition* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0611e-144">Ein Zeiger auf eine Variable, die einen der folgenden Dispositions Werte empfängt.</span><span class="sxs-lookup"><span data-stu-id="0611e-144">A pointer to a variable that receives one of the following disposition values.</span></span>



| <span data-ttu-id="0611e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="0611e-145">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="0611e-146">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0611e-146">Meaning</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <span data-ttu-id="0611e-147"><dt>**Reg \_ \_Neuer \_ Schlüssel**</dt> <dt>0x00000001l</dt> erstellt</span><span class="sxs-lookup"><span data-stu-id="0611e-147"><dt>**REG\_CREATED\_NEW\_KEY**</dt> <dt>0x00000001L</dt></span></span> </dl>             | <span data-ttu-id="0611e-148">Der Schlüssel ist nicht vorhanden und wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="0611e-148">The key did not exist and was created.</span></span><br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <span data-ttu-id="0611e-149"><dt>**Reg \_ Der \_ vorhandene \_ Schlüssel**</dt> <dt>0x00000002l</dt> wurde geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0611e-149"><dt>**REG\_OPENED\_EXISTING\_KEY**</dt> <dt>0x00000002L</dt></span></span> </dl> | <span data-ttu-id="0611e-150">Der Schlüssel war vorhanden und wurde einfach geöffnet, ohne geändert zu werden.</span><span class="sxs-lookup"><span data-stu-id="0611e-150">The key existed and was simply opened without being changed.</span></span><br/> |



 

<span data-ttu-id="0611e-151">Wenn *pdwdisposition* auf **null** festgelegt ist, werden keine Disposition-Informationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0611e-151">If *pdwDisposition* is **NULL**, no disposition information is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0611e-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0611e-152">Return value</span></span>

<span data-ttu-id="0611e-153">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0611e-153">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0611e-154">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0611e-154">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="0611e-155">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0611e-155">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="0611e-156">Wenn der *dwOptions* -Parameter mit der **reg- \_ Option \_ Create \_ Link** festgelegt ist, aber die **reg- \_ Option \_ nicht \_ flüchtig** auf Clear festgelegt ist oder wenn das zurück zugegende Handle ein Handle für den Stamm Schlüssel der Hive ist, gibt die Funktion den \_ ungültigen Parameter Error zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="0611e-156">If the *dwOptions* parameter is set with **REG\_OPTION\_CREATE\_LINK** but **REG\_OPTION\_NON\_VOLATILE** is clear, or if the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="0611e-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0611e-157">Remarks</span></span>

<span data-ttu-id="0611e-158">Der Schlüssel, der von der **orkreatekey** -Funktion erstellt wird, weist keine Werte auf.</span><span class="sxs-lookup"><span data-stu-id="0611e-158">The key that the **ORCreateKey** function creates has no values.</span></span> <span data-ttu-id="0611e-159">Eine Anwendung kann die [**orsetvalue**](orsetvalue.md) -Funktion verwenden, um Schlüsselwerte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0611e-159">An application can use the [**ORSetValue**](orsetvalue.md) function to set key values.</span></span>

<span data-ttu-id="0611e-160">Die **orkreatekey** -Funktion kann nicht verwendet werden, um den Stamm Schlüssel in einer Offline Registrierungs Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0611e-160">The **ORCreateKey** function cannot be used to create the root key in an offline registry hive.</span></span> <span data-ttu-id="0611e-161">Verwenden Sie die [**orkreatehive**](orcreatehive.md) -Funktion, um den Stamm Schlüssel zu erstellen, und rufen Sie ein Handle für den Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="0611e-161">Use the [**ORCreateHive**](orcreatehive.md) function to create the root key and obtain a handle to the key.</span></span>

<span data-ttu-id="0611e-162">Die Offline Registrierung unterstützt das Speichern einzelner Schlüssel nicht.</span><span class="sxs-lookup"><span data-stu-id="0611e-162">The offline registry does not support saving individual keys.</span></span> <span data-ttu-id="0611e-163">Verwenden Sie die [**orsavehive**](orsavehive.md) -Funktion, um einen Schlüssel und dessen Unterschlüssel in einer Hive zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0611e-163">Use the [**ORSaveHive**](orsavehive.md) function to save a key and its subkeys in a hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="0611e-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0611e-164">Requirements</span></span>



| <span data-ttu-id="0611e-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0611e-165">Requirement</span></span> | <span data-ttu-id="0611e-166">Wert</span><span class="sxs-lookup"><span data-stu-id="0611e-166">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0611e-167">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0611e-167">Redistributable</span></span><br/> | <span data-ttu-id="0611e-168">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0611e-168">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="0611e-169">Header</span><span class="sxs-lookup"><span data-stu-id="0611e-169">Header</span></span><br/>          | <dl> <span data-ttu-id="0611e-170"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0611e-170"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="0611e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="0611e-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="0611e-172"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0611e-172"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0611e-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0611e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0611e-174">**Orclosekey**</span><span class="sxs-lookup"><span data-stu-id="0611e-174">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="0611e-175">**Orkreatehive**</span><span class="sxs-lookup"><span data-stu-id="0611e-175">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="0611e-176">**Ordeletekey**</span><span class="sxs-lookup"><span data-stu-id="0611e-176">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="0611e-177">**Orsavehive**</span><span class="sxs-lookup"><span data-stu-id="0611e-177">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="0611e-178">Sicherheits \_ Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0611e-178">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
