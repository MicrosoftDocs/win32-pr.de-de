---
title: Removeprogram-Methode der Win32_TSVirtualIP-Klasse (bmolface. h)
description: Entfernt ein Programm aus der Liste der Programme, die die IP-Virtualisierung verwenden.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Removeprogram-Methode Remotedesktopdienste
- Removeprogram-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, removeprogram-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743625"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="aafc1-106">Removeprogram-Methode der Win32- \_ Klasse "tvirtualip"</span><span class="sxs-lookup"><span data-stu-id="aafc1-106">RemoveProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="aafc1-107">Entfernt ein Programm aus der Liste der Programme, die die IP-Virtualisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="aafc1-107">Removes a program from the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="aafc1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aafc1-108">Syntax</span></span>


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="aafc1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aafc1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aafc1-110">*Programpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aafc1-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aafc1-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aafc1-111">Type: **string**</span></span>

<span data-ttu-id="aafc1-112">Der Pfad und der Dateiname des Programms, das aus der Liste entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aafc1-112">The path and file name of the program to remove from the list.</span></span> <span data-ttu-id="aafc1-113">Wenn das Programm nicht gefunden wird, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aafc1-113">If the program is not found, an error is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aafc1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aafc1-114">Return value</span></span>

<span data-ttu-id="aafc1-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aafc1-115">Type: **uint32**</span></span>

<span data-ttu-id="aafc1-116">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aafc1-116">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="aafc1-117">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="aafc1-117">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="aafc1-118">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="aafc1-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="aafc1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aafc1-119">Requirements</span></span>



| <span data-ttu-id="aafc1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aafc1-120">Requirement</span></span> | <span data-ttu-id="aafc1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="aafc1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aafc1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aafc1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aafc1-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aafc1-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="aafc1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aafc1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aafc1-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aafc1-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="aafc1-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="aafc1-126">Namespace</span></span><br/>                | <span data-ttu-id="aafc1-127">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="aafc1-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="aafc1-128">Header</span><span class="sxs-lookup"><span data-stu-id="aafc1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="aafc1-129"><dt>Bmolface. h</dt></span><span class="sxs-lookup"><span data-stu-id="aafc1-129"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="aafc1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="aafc1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aafc1-131"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aafc1-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="aafc1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="aafc1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aafc1-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aafc1-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aafc1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aafc1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aafc1-135">**Win32- \_ virtualialip**</span><span class="sxs-lookup"><span data-stu-id="aafc1-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





