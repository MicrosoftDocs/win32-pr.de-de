---
description: Gibt an, ob das numerische Kennwort den speziellen Formatierungs Anforderungen für diesen Authentifizierungs Wert entspricht.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Isnumericalpasswordvalid-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349548"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="718aa-103">Isnumericalpasswordvalid-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="718aa-103">IsNumericalPasswordValid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="718aa-104">Die **isnumericalpasswordvalid-** Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob das numerische Kennwort die speziellen Formatierungs Anforderungen für diesen Authentifizierungs Wert erfüllt.</span><span class="sxs-lookup"><span data-stu-id="718aa-104">The **IsNumericalPasswordValid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the numerical password meets the special format requirements for this authentication value.</span></span>

## <a name="syntax"></a><span data-ttu-id="718aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="718aa-105">Syntax</span></span>


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a><span data-ttu-id="718aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="718aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="718aa-107">*Numericalpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="718aa-107">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718aa-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="718aa-108">Type: **string**</span></span>

<span data-ttu-id="718aa-109">Eine Zeichenfolge, die das numerische Kennwort angibt.</span><span class="sxs-lookup"><span data-stu-id="718aa-109">A string that specifies the numerical password.</span></span>

<span data-ttu-id="718aa-110">Das numerische Kennwort muss 48 Ziffern enthalten.</span><span class="sxs-lookup"><span data-stu-id="718aa-110">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="718aa-111">Diese Ziffern können in 8 Gruppen mit 6 Ziffern aufgeteilt werden, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummen Wert für die Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="718aa-111">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="718aa-112">Jede Gruppe von 6 Ziffern muss von 11 teilbar sein und muss kleiner als 720896 sein.</span><span class="sxs-lookup"><span data-stu-id="718aa-112">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="718aa-113">Wenn eine Gruppe von sechs Ziffern als x1, x2, X3, X4, x5 und x6 bezeichnet wird, wird die Ziffer "Prüfsumme x6" als "– x1 + x2 – X3 + X4 – x5 mod 11" berechnet.</span><span class="sxs-lookup"><span data-stu-id="718aa-113">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="718aa-114">Die Gruppen von Ziffern können optional durch ein Leerzeichen oder einen Bindestrich getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="718aa-114">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="718aa-115">"Xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oder "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" kann daher auch gültige numerische Kenn Wörter enthalten.</span><span class="sxs-lookup"><span data-stu-id="718aa-115">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> <dt>

<span data-ttu-id="718aa-116">*Isnumericalpasswordvalid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="718aa-116">*IsNumericalPasswordValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="718aa-117">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="718aa-117">Type: **boolean**</span></span>

<span data-ttu-id="718aa-118">Ein boolescher Wert, der true ist, wenn das numerische Kennwort den speziellen Formatanforderungen für diesen Authentifizierungs Wert entspricht; andernfalls ist der Wert false.</span><span class="sxs-lookup"><span data-stu-id="718aa-118">A Boolean value that is true if the numerical password meets the special format requirements for this authentication value, otherwise the value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="718aa-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="718aa-119">Return value</span></span>

<span data-ttu-id="718aa-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="718aa-120">Type: **uint32**</span></span>

<span data-ttu-id="718aa-121">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="718aa-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="718aa-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="718aa-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="718aa-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="718aa-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="718aa-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="718aa-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="718aa-125">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="718aa-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="718aa-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="718aa-126">Remarks</span></span>

<span data-ttu-id="718aa-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="718aa-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="718aa-128">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="718aa-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="718aa-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="718aa-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="718aa-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="718aa-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="718aa-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="718aa-131">Requirements</span></span>



| <span data-ttu-id="718aa-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="718aa-132">Requirement</span></span> | <span data-ttu-id="718aa-133">Wert</span><span class="sxs-lookup"><span data-stu-id="718aa-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="718aa-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="718aa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="718aa-135">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="718aa-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="718aa-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="718aa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="718aa-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="718aa-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="718aa-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="718aa-138">Namespace</span></span><br/>                | <span data-ttu-id="718aa-139">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="718aa-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="718aa-140">MOF</span><span class="sxs-lookup"><span data-stu-id="718aa-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="718aa-141"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="718aa-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="718aa-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="718aa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="718aa-143">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="718aa-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
