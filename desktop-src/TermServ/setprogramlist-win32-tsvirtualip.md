---
title: Setprogramlist-Methode der Win32_TSVirtualIP-Klasse
description: Überschreibt die Liste der Programme, die die IP-Virtualisierung verwenden.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Setprogramlist-Methode Remotedesktopdienste
- Setprogramlist-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, setprogramlist-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518023"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="7dca2-106">Setprogramlist-Methode der Win32- \_ Klasse "tvirtualip"</span><span class="sxs-lookup"><span data-stu-id="7dca2-106">SetProgramList method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="7dca2-107">Überschreibt die Liste der Programme, die die IP-Virtualisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7dca2-107">Overwrites the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dca2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dca2-108">Syntax</span></span>


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a><span data-ttu-id="7dca2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7dca2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dca2-110">*Programmliste* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7dca2-110">*ProgramList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dca2-111">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="7dca2-111">Type: **string\[\]**</span></span>

<span data-ttu-id="7dca2-112">Ein Array von Zeichen folgen, das die Pfad-und Dateinamen der Programme enthält, die die IP-Virtualisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7dca2-112">An array of strings that contain the path and file names of the programs that use IP virtualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dca2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7dca2-113">Return value</span></span>

<span data-ttu-id="7dca2-114">Typ: **unint32**</span><span class="sxs-lookup"><span data-stu-id="7dca2-114">Type: **unint32**</span></span>

<span data-ttu-id="7dca2-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7dca2-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7dca2-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7dca2-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="7dca2-117">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="7dca2-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dca2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dca2-118">Requirements</span></span>



| <span data-ttu-id="7dca2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7dca2-119">Requirement</span></span> | <span data-ttu-id="7dca2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7dca2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dca2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7dca2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7dca2-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7dca2-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7dca2-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7dca2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7dca2-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7dca2-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="7dca2-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="7dca2-125">Namespace</span></span><br/>                | <span data-ttu-id="7dca2-126">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7dca2-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7dca2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="7dca2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7dca2-128"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7dca2-128"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7dca2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7dca2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dca2-130"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dca2-130"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dca2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dca2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dca2-132">**Win32- \_ virtualialip**</span><span class="sxs-lookup"><span data-stu-id="7dca2-132">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





