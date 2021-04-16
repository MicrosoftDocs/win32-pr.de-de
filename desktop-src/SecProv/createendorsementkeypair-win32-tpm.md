---
description: Erstellt ein 2048-Bit-Endorsement Key-paar auf dem TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Methode "kreateendorsegmentkeypair" der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525691"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a><span data-ttu-id="8fedf-103">Methode "kreateendorsegmentkeypair" der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="8fedf-103">CreateEndorsementKeyPair method of the Win32\_Tpm class</span></span>

<span data-ttu-id="8fedf-104">Die Methode " **kreateendorsegmentkeypair** " der [**Win32- \_ TPM**](win32-tpm.md) -Klasse erstellt ein 2048-Bit-Endorsement Key-paar auf dem TPM.</span><span class="sxs-lookup"><span data-stu-id="8fedf-104">The **CreateEndorsementKeyPair** method of the [**Win32\_Tpm**](win32-tpm.md) class creates an 2048-bit endorsement key pair on the TPM.</span></span> <span data-ttu-id="8fedf-105">Das Endorsement Key-Paar muss verfügbar sein, damit die [**TakeOwnership**](takeownership-win32-tpm.md) -Methode erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="8fedf-105">The endorsement key pair must be available for the [**TakeOwnership**](takeownership-win32-tpm.md) method to run successfully.</span></span> <span data-ttu-id="8fedf-106">Sie können mit der [**isendorsementkeyplunpresent**](isendorsementkeypairpresent-win32-tpm.md) -Methode ermitteln, ob der Endorsement Key bereits auf dem TPM vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8fedf-106">You can use the [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) method to detect whether the endorsement key already exists on the TPM.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fedf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fedf-107">Syntax</span></span>


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a><span data-ttu-id="8fedf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fedf-108">Parameters</span></span>

<span data-ttu-id="8fedf-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8fedf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fedf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fedf-110">Return value</span></span>

<span data-ttu-id="8fedf-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8fedf-111">Type: **uint32**</span></span>

<span data-ttu-id="8fedf-112">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8fedf-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="8fedf-113">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fedf-113">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="8fedf-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="8fedf-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="8fedf-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fedf-115">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="8fedf-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8fedf-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="8fedf-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8fedf-117">The method was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="8fedf-118"><dt> **TPM \_ E \_ deaktiviert \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt></span><span class="sxs-lookup"><span data-stu-id="8fedf-118"><dt>**TPM\_E\_DISABLED\_CMD** </dt> <dt>2150105096 (0x80280008)</dt></span></span> </dl> | <span data-ttu-id="8fedf-119">Ein Endorsement Key-Paar ist bereits auf diesem TPM vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8fedf-119">An endorsement key pair already exists on this TPM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8fedf-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fedf-120">Remarks</span></span>

<span data-ttu-id="8fedf-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8fedf-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8fedf-122">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="8fedf-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8fedf-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8fedf-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8fedf-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8fedf-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fedf-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fedf-125">Requirements</span></span>



| <span data-ttu-id="8fedf-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fedf-126">Requirement</span></span> | <span data-ttu-id="8fedf-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8fedf-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fedf-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fedf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8fedf-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fedf-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8fedf-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fedf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8fedf-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fedf-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8fedf-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fedf-132">Namespace</span></span><br/>                | <span data-ttu-id="8fedf-133">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="8fedf-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="8fedf-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8fedf-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fedf-135"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8fedf-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fedf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8fedf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fedf-137"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fedf-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fedf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fedf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fedf-139">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="8fedf-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
