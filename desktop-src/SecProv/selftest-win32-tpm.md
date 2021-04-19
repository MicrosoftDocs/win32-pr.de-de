---
description: Führt einen Selbsttest des TPM aus und gibt das Ergebnis zurück.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Selftest-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348370"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a><span data-ttu-id="627f3-103">Selftest-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="627f3-103">SelfTest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="627f3-104">Die **Selftest** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse führt einen Selbsttest für das TPM aus und gibt das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="627f3-104">The **SelfTest** method of the [**Win32\_Tpm**](win32-tpm.md) class performs a self-test of the TPM and returns the result.</span></span>

<span data-ttu-id="627f3-105">Ein TPM-Self-Test wird automatisch ausgeführt, wenn der Computer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="627f3-105">A TPM self-test runs automatically when the computer starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="627f3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="627f3-106">Syntax</span></span>


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="627f3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="627f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="627f3-108">*Selftestresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="627f3-108">*SelfTestResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="627f3-109">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="627f3-109">Type: **uint8\[\]**</span></span>

<span data-ttu-id="627f3-110">Ein Bytearray, das das Selbsttest Ergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="627f3-110">An array of bytes that contains the self-test result.</span></span> <span data-ttu-id="627f3-111">Das Format dieses Parameters ist Hersteller spezifisch.</span><span class="sxs-lookup"><span data-stu-id="627f3-111">The format of this parameter is manufacturer-specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="627f3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="627f3-112">Return value</span></span>

<span data-ttu-id="627f3-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="627f3-113">Type: **uint32**</span></span>

<span data-ttu-id="627f3-114">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="627f3-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="627f3-115">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="627f3-115">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="627f3-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="627f3-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="627f3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="627f3-117">Description</span></span>                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="627f3-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="627f3-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="627f3-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="627f3-119">The method ran successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="627f3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="627f3-120">Remarks</span></span>

<span data-ttu-id="627f3-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="627f3-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="627f3-122">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="627f3-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="627f3-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="627f3-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="627f3-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="627f3-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="627f3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="627f3-125">Requirements</span></span>



| <span data-ttu-id="627f3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="627f3-126">Requirement</span></span> | <span data-ttu-id="627f3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="627f3-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="627f3-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="627f3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="627f3-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="627f3-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="627f3-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="627f3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="627f3-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="627f3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="627f3-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="627f3-132">Namespace</span></span><br/>                | <span data-ttu-id="627f3-133">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="627f3-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="627f3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="627f3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="627f3-135"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="627f3-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="627f3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="627f3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="627f3-137"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="627f3-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="627f3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="627f3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627f3-139">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="627f3-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
