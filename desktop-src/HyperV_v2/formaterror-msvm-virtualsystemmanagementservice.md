---
description: Gibt eine formatierte Fehlermeldungs Zeichenfolge für das angegebene Array von eingebetteten MSVM- \_ Fehler Instanzen zurück.
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Formaterror-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346974"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="38254-103">Formaterror-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="38254-103">FormatError method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="38254-104">Gibt eine formatierte Fehlermeldungs Zeichenfolge für das angegebene Array von eingebetteten [**MSVM- \_ Fehler**](msvm-error.md) Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="38254-104">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="38254-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38254-105">Syntax</span></span>


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="38254-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38254-107">*Fehler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38254-107">*Errors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38254-108">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="38254-108">Type: **string\[\]**</span></span>

<span data-ttu-id="38254-109">Ein Array von Zeichen folgen mit [**MSVM- \_ Fehler**](msvm-error.md) Instanzen, die zum Generieren der Ausgabe Fehlermeldung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38254-109">An array of strings containing [**Msvm\_Error**](msvm-error.md) instances used to generate the output error message.</span></span>

</dd> <dt>

<span data-ttu-id="38254-110">*ErrorMessage* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="38254-110">*ErrorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38254-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38254-111">Type: **string**</span></span>

<span data-ttu-id="38254-112">Bei Ausgabe eine Zeichenfolge, die die verketteten Fehlermeldungen enthält, die von den [**MSVM- \_ Fehler**](msvm-error.md) Instanzen dargestellt werden, die im *Errors* -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="38254-112">On output, a string that contains the concatenated error messages represented by the [**Msvm\_Error**](msvm-error.md) instances passed in the *Errors* parameter.</span></span> <span data-ttu-id="38254-113">Jede Fehler Zeichenfolge wird durch ein Zeilen Zeilenpaar (" \\ n") getrennt.</span><span class="sxs-lookup"><span data-stu-id="38254-113">Each error string is separated by a pair of newline characters ('\\n').</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38254-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38254-114">Return value</span></span>

<span data-ttu-id="38254-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38254-115">Type: **uint32**</span></span>

<span data-ttu-id="38254-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="38254-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="38254-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="38254-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="38254-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="38254-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="38254-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="38254-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="38254-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="38254-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="38254-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="38254-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="38254-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="38254-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="38254-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="38254-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="38254-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="38254-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="38254-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="38254-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="38254-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="38254-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="38254-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="38254-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="38254-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="38254-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="38254-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="38254-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="38254-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38254-130">Remarks</span></span>

<span data-ttu-id="38254-131">Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="38254-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="38254-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="38254-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="38254-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38254-133">Requirements</span></span>



| <span data-ttu-id="38254-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38254-134">Requirement</span></span> | <span data-ttu-id="38254-135">Wert</span><span class="sxs-lookup"><span data-stu-id="38254-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38254-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38254-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38254-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38254-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="38254-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38254-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38254-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38254-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38254-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="38254-140">Namespace</span></span><br/>                | <span data-ttu-id="38254-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="38254-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="38254-142">MOF</span><span class="sxs-lookup"><span data-stu-id="38254-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38254-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="38254-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38254-144">DLL</span><span class="sxs-lookup"><span data-stu-id="38254-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38254-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38254-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38254-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38254-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38254-147">**Formaterror (v1)**</span><span class="sxs-lookup"><span data-stu-id="38254-147">**FormatError (V1)**</span></span>](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="38254-148">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="38254-148">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

