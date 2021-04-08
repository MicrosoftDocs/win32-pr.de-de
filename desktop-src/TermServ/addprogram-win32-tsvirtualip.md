---
title: Addprogram-Methode der Win32_TSVirtualIP-Klasse (bmolface. h)
description: Fügt der Liste der Programme, die die IP-Virtualisierung verwenden, ein Programm hinzu.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Addprogram-Methode Remotedesktopdienste
- Addprogram-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, addprogram-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de573e8d04500917ed44d5a0453005b3aa691bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740768"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="9ad88-106">Addprogram-Methode der Win32- \_ Klasse "tvirtualip"</span><span class="sxs-lookup"><span data-stu-id="9ad88-106">AddProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="9ad88-107">Fügt der Liste der Programme, die die IP-Virtualisierung verwenden, ein Programm hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ad88-107">Adds a program to the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad88-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ad88-108">Syntax</span></span>


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="9ad88-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ad88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ad88-110">*Programpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ad88-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ad88-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ad88-111">Type: **string**</span></span>

<span data-ttu-id="9ad88-112">Der Pfad und der Dateiname des Programms, das der Liste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ad88-112">The path and file name of the program to add to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ad88-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ad88-113">Return value</span></span>

<span data-ttu-id="9ad88-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ad88-114">Type: **uint32**</span></span>

<span data-ttu-id="9ad88-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ad88-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9ad88-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9ad88-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="9ad88-117">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="9ad88-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ad88-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ad88-118">Requirements</span></span>



| <span data-ttu-id="9ad88-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ad88-119">Requirement</span></span> | <span data-ttu-id="9ad88-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9ad88-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad88-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ad88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad88-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ad88-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9ad88-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ad88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad88-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ad88-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="9ad88-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ad88-125">Namespace</span></span><br/>                | <span data-ttu-id="9ad88-126">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9ad88-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9ad88-127">Header</span><span class="sxs-lookup"><span data-stu-id="9ad88-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ad88-128"><dt>Bmolface. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ad88-128"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ad88-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9ad88-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ad88-130"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9ad88-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ad88-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9ad88-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ad88-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ad88-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ad88-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ad88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad88-134">**Win32- \_ virtualialip**</span><span class="sxs-lookup"><span data-stu-id="9ad88-134">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





