---
title: Create-Methode der Win32_Terminal-Klasse
description: Erstellt ein Terminal mit Standardeinstellungen, die mithilfe der Eigenschaften und Methoden der Win32 \_ TerminalSetting-Klassen angepasst werden können.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Create-Methode Remotedesktopdienste
- Create Method Remotedesktopdienste, Win32_Terminal-Klasse
- Win32_Terminal Klasse Remotedesktopdienste, Methode erstellen
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475642"
---
# <a name="create-method-of-the-win32_terminal-class"></a><span data-ttu-id="aced1-106">Create-Methode der Win32- \_ Terminal Klasse</span><span class="sxs-lookup"><span data-stu-id="aced1-106">Create method of the Win32\_Terminal class</span></span>

<span data-ttu-id="aced1-107">Die **Create** -Methode erstellt ein Terminal mit Standardeinstellungen, das mithilfe der Eigenschaften und Methoden der [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) -Klassen angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="aced1-107">The **Create** method creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span> <span data-ttu-id="aced1-108">Die Funktion gibt bei Erfolg 0 (null) und einen Fehler Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="aced1-108">The function returns zero on success and an error on failure.</span></span>

## <a name="syntax"></a><span data-ttu-id="aced1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aced1-109">Syntax</span></span>


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="aced1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aced1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aced1-111">*Newterminalname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aced1-111">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aced1-112">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="aced1-112">Name of the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="aced1-113">*Transport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aced1-113">*Transport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aced1-114">Transport für das Terminal.</span><span class="sxs-lookup"><span data-stu-id="aced1-114">Transport for the terminal.</span></span> <span data-ttu-id="aced1-115">Dies ist eine Eigenschaft der Win32-Klasse " [**\_ tgeneralsetting**](win32-tsgeneralsetting.md) ".</span><span class="sxs-lookup"><span data-stu-id="aced1-115">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="aced1-116">*TerminalProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aced1-116">*TerminalProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aced1-117">Protokoll für das Terminal.</span><span class="sxs-lookup"><span data-stu-id="aced1-117">Protocol for the terminal.</span></span> <span data-ttu-id="aced1-118">Dies ist eine Eigenschaft der Win32-Klasse " [**\_ tgeneralsetting**](win32-tsgeneralsetting.md) ".</span><span class="sxs-lookup"><span data-stu-id="aced1-118">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aced1-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aced1-119">Return value</span></span>

<span data-ttu-id="aced1-120">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aced1-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="aced1-121">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="aced1-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="aced1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aced1-122">Remarks</span></span>

<span data-ttu-id="aced1-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="aced1-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aced1-124">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="aced1-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aced1-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aced1-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aced1-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="aced1-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="aced1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aced1-127">Requirements</span></span>



| <span data-ttu-id="aced1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aced1-128">Requirement</span></span> | <span data-ttu-id="aced1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="aced1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aced1-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aced1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aced1-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aced1-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aced1-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aced1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aced1-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aced1-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aced1-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="aced1-134">Namespace</span></span><br/>                | <span data-ttu-id="aced1-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="aced1-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="aced1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="aced1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aced1-137"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aced1-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="aced1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="aced1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aced1-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aced1-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aced1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aced1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aced1-141">**Win32- \_ Terminal**</span><span class="sxs-lookup"><span data-stu-id="aced1-141">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

