---
description: Ändert den TPM-Besitzer Autorisierungs Wert.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Changebesitzauth-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128760"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="70476-103">Changebesitzauth-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="70476-103">ChangeOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="70476-104">Mit der **changebesitzauth** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse wird der TPM-Besitzer Autorisierungs Wert geändert.</span><span class="sxs-lookup"><span data-stu-id="70476-104">The **ChangeOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class changes the TPM owner authorization value.</span></span>

## <a name="syntax"></a><span data-ttu-id="70476-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70476-105">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="70476-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70476-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70476-107">*Oldownerauth* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="70476-107">*OldOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70476-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="70476-108">Type: **string**</span></span>

<span data-ttu-id="70476-109">Eine Zeichenfolge, die den aktuellen TPM-Besitzer Autorisierungs Wert des Geräts benennt.</span><span class="sxs-lookup"><span data-stu-id="70476-109">A string that names the current TPM owner authorization value of the device.</span></span> <span data-ttu-id="70476-110">Verwenden Sie die [**convertdebesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um ein Kennwort in diesen Autorisierungs Wert zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="70476-110">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="70476-111">Der *oldownerauth* -Parameter wurde nicht angegeben, oder es wird eine leere Zeichenfolge bereitgestellt. diese Methode ruft den Wert aus der Registrierung ab, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="70476-111">The *OldOwnerAuth* parameter is not supplied or an empty string is provided, this method gets the value from the registry if present.</span></span>

</dd> <dt>

<span data-ttu-id="70476-112">" *Netwownerauth* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="70476-112">*NewOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70476-113">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="70476-113">Type: **string**</span></span>

<span data-ttu-id="70476-114">Eine Zeichenfolge, die den neuen TPM-Besitzer Autorisierungs Wert benennt.</span><span class="sxs-lookup"><span data-stu-id="70476-114">A string that names the new TPM owner authorization value.</span></span> <span data-ttu-id="70476-115">Verwenden Sie die [**convertdebesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um ein Kennwort in diesen Autorisierungs Wert zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="70476-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="70476-116">Der Parameter " *netwownerauth* " darf nicht leer oder **NULL sein.**</span><span class="sxs-lookup"><span data-stu-id="70476-116">The *NewOwnerAuth* parameter cannot be empty or **NULL.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70476-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70476-117">Return value</span></span>

<span data-ttu-id="70476-118">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70476-118">Type: **uint32**</span></span>

<span data-ttu-id="70476-119">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70476-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="70476-120">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="70476-120">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="70476-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="70476-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="70476-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70476-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70476-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="70476-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                              | <span data-ttu-id="70476-124">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="70476-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="70476-125"><dt>**TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="70476-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>                   | <span data-ttu-id="70476-126">Der aktuelle TPM-Besitzer Autorisierungs Wert ist falsch.</span><span class="sxs-lookup"><span data-stu-id="70476-126">The current TPM owner authorization value is incorrect.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="70476-127"><dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="70476-127"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl>      | <span data-ttu-id="70476-128">Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="70476-128">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="70476-129">Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="70476-129">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="70476-130"><dt>**F \_ E \_ AD- \_ Schema \_ nicht \_ installiert**</dt> <dt>2150694922 (0x8031000a)</dt></span><span class="sxs-lookup"><span data-stu-id="70476-130"><dt>**FVE\_E\_AD\_SCHEMA\_NOT\_INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt></span></span> </dl> | <span data-ttu-id="70476-131">Wiederherstellungs Informationen können nicht im Netzwerk gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="70476-131">Cannot save recovery information to the network.</span></span> <span data-ttu-id="70476-132">Der Computer wurde so konfiguriert, dass Wiederherstellungs Informationen in Active Directory Domain Services gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="70476-132">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="70476-133">Anweisungen zum Einrichten von Active Directory finden Sie [unter BitLocker-Laufwerkverschlüsselung Configuration Guide: Sichern von BitLocker-und TPM-Wiederherstellungs Informationen in Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="70476-133">For instructions on how to set up Active Directory, see [BitLocker Drive Encryption Configuration Guide: Backing Up BitLocker and TPM Recovery Information to Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span></span><br/> |
| <dl> <span data-ttu-id="70476-134"><dt>**Verbindungs**</dt> Fehler <dt>2147943755 (0x8007054b)</dt></span><span class="sxs-lookup"><span data-stu-id="70476-134"><dt>**Connection Failed**</dt> <dt>2147943755 (0x8007054B)</dt></span></span> </dl>                  | <span data-ttu-id="70476-135">Wiederherstellungs Informationen können nicht im Netzwerk gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="70476-135">Cannot save recovery information to the network.</span></span> <span data-ttu-id="70476-136">Der Computer wurde so konfiguriert, dass Wiederherstellungs Informationen in Active Directory Domain Services gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="70476-136">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="70476-137">Eine Netzwerkverbindung ist erforderlich, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="70476-137">A network connection is required to continue.</span></span><br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="70476-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70476-138">Remarks</span></span>

<span data-ttu-id="70476-139">Die **changebesitzauth** -Methode sichert die neue TPM-Besitzer Autorisierung, um Active Directory Domain Services, wenn die entsprechenden Gruppenrichtlinie Einstellungen konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="70476-139">The **ChangeOwnerAuth** method backs up the new TPM owner authorization to Active Directory Domain Services if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="70476-140">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="70476-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="70476-141">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="70476-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="70476-142">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="70476-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="70476-143">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="70476-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70476-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70476-144">Requirements</span></span>



| <span data-ttu-id="70476-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70476-145">Requirement</span></span> | <span data-ttu-id="70476-146">Wert</span><span class="sxs-lookup"><span data-stu-id="70476-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="70476-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70476-147">Minimum supported client</span></span><br/> | <span data-ttu-id="70476-148">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70476-148">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="70476-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70476-149">Minimum supported server</span></span><br/> | <span data-ttu-id="70476-150">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70476-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="70476-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="70476-151">Namespace</span></span><br/>                | <span data-ttu-id="70476-152">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="70476-152">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="70476-153">MOF</span><span class="sxs-lookup"><span data-stu-id="70476-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70476-154"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="70476-154"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="70476-155">DLL</span><span class="sxs-lookup"><span data-stu-id="70476-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70476-156"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70476-156"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70476-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70476-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70476-158">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="70476-158">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
