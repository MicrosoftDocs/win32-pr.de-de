---
title: Rename-Methode der Win32_Terminal-Klasse
description: Die Rename-Methode benennt das Terminal um.
ms.assetid: 85b5c83b-8ca3-4ed0-852b-b11ba98c18a6
ms.tgt_platform: multiple
keywords:
- Methode umbenennen Remotedesktopdienste
- Umbenennen der Methode Remotedesktopdienste, Win32_Terminal Klasse
- Win32_Terminal Klasse Remotedesktopdienste, Methode umbenennen
topic_type:
- apiref
api_name:
- Win32_Terminal.Rename
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0258277bd509f7f72d5e314bc20d9852fa03315a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341784"
---
# <a name="rename-method-of-the-win32_terminal-class"></a><span data-ttu-id="704a6-106">Rename-Methode der Win32- \_ Terminal Klasse</span><span class="sxs-lookup"><span data-stu-id="704a6-106">Rename method of the Win32\_Terminal class</span></span>

<span data-ttu-id="704a6-107">Die **Rename** -Methode benennt das Terminal um.</span><span class="sxs-lookup"><span data-stu-id="704a6-107">The **Rename** method renames the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="704a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="704a6-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="704a6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="704a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="704a6-110">*Newterminalname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="704a6-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="704a6-111">Der neue Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="704a6-111">The new name of the terminal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="704a6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="704a6-112">Return value</span></span>

<span data-ttu-id="704a6-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="704a6-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="704a6-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="704a6-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="704a6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="704a6-115">Remarks</span></span>

<span data-ttu-id="704a6-116">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="704a6-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="704a6-117">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="704a6-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="704a6-118">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="704a6-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="704a6-119">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="704a6-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="704a6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="704a6-120">Requirements</span></span>



| <span data-ttu-id="704a6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="704a6-121">Requirement</span></span> | <span data-ttu-id="704a6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="704a6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="704a6-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="704a6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="704a6-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="704a6-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="704a6-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="704a6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="704a6-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="704a6-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="704a6-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="704a6-127">Namespace</span></span><br/>                | <span data-ttu-id="704a6-128">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="704a6-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="704a6-129">MOF</span><span class="sxs-lookup"><span data-stu-id="704a6-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="704a6-130"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="704a6-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="704a6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="704a6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="704a6-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="704a6-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="704a6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="704a6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="704a6-134">**Win32- \_ Terminal**</span><span class="sxs-lookup"><span data-stu-id="704a6-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

