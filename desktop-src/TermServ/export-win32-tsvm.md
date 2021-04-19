---
title: Export-Methode der Win32_TSVm-Klasse
description: Ruft die Überwachungsinformationen für die Sitzung der virtuellen Maschine ab.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Export Methode Remotedesktopdienste
- Export Methode Remotedesktopdienste, Win32_TSVm Klasse
- Win32_TSVm-Klasse Remotedesktopdienste, Export-Methode
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339544"
---
# <a name="export-method-of-the-win32_tsvm-class"></a><span data-ttu-id="b3186-106">Export-Methode der Win32-Klasse "t- \_ VM"</span><span class="sxs-lookup"><span data-stu-id="b3186-106">Export method of the Win32\_TSVm class</span></span>

<span data-ttu-id="b3186-107">Ruft die Überwachungsinformationen für die Sitzung der virtuellen Maschine ab.</span><span class="sxs-lookup"><span data-stu-id="b3186-107">Retrieves the virtual machine session monitoring information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3186-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3186-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a><span data-ttu-id="b3186-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3186-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3186-110">*Exportfolderpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3186-110">*ExportFolderPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3186-111">Der Pfad zum Speicherort der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="b3186-111">Path to where the virtual machine will be exported.</span></span>

</dd> <dt>

<span data-ttu-id="b3186-112">*Exportjobobjectpath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b3186-112">*ExportJobObjectPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3186-113">Bei erfolgreicher Ausführung wird der HyperV-Objekt Pfad "concretejob" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3186-113">On a success returns the HyperV ConcreteJob object path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3186-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3186-114">Return value</span></span>

<span data-ttu-id="b3186-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3186-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b3186-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b3186-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3186-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3186-117">Requirements</span></span>



| <span data-ttu-id="b3186-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3186-118">Requirement</span></span> | <span data-ttu-id="b3186-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b3186-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3186-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3186-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3186-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b3186-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="b3186-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3186-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3186-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3186-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="b3186-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3186-124">Namespace</span></span><br/>                | <span data-ttu-id="b3186-125">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b3186-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="b3186-126">MOF</span><span class="sxs-lookup"><span data-stu-id="b3186-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3186-127"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b3186-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="b3186-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b3186-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3186-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3186-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3186-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3186-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3186-131">**Win32- \_ VM**</span><span class="sxs-lookup"><span data-stu-id="b3186-131">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





