---
title: Setpolicypropertyname-Methode der Win32_TerminalServiceSetting-Klasse
description: Die setpolicypropertyname-Methode legt die deletetempfolders-, usetempfolders-oder Help-Eigenschaft für die-Klasse fest.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Setpolicypropertyname-Methode Remotedesktopdienste
- Setpolicypropertyname-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, setpolicypropertyname-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478831"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="4fcd8-106">Setpolicypropertyname-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="4fcd8-106">SetPolicyPropertyName method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="4fcd8-107">Die **setpolicypropertyname** -Methode legt die **deletetempfolders**-, **usetempfolders** -oder **Help** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-107">The **SetPolicyPropertyName** method sets the **DeleteTempFolders**, **UseTempFolders** or **Help** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fcd8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fcd8-108">Syntax</span></span>


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="4fcd8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fcd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fcd8-110">*PropertyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fcd8-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcd8-111">Gibt die Richtlinien Eigenschaft an, die von der-Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-111">Specifies the policy property that the method is setting.</span></span>

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span data-ttu-id="4fcd8-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**Deletetempfolders**</span><span class="sxs-lookup"><span data-stu-id="4fcd8-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="4fcd8-113">Die-Methode legt die **deletetempfolders** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-113">The method is setting the **DeleteTempFolders** property.</span></span>

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span data-ttu-id="4fcd8-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**Usetempfolders**</span><span class="sxs-lookup"><span data-stu-id="4fcd8-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="4fcd8-115">Die-Methode legt die **usetempfolders** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-115">The method is setting the **UseTempFolders** property.</span></span>

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span data-ttu-id="4fcd8-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Hilfe**</span><span class="sxs-lookup"><span data-stu-id="4fcd8-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Help**</span></span>


</dt> <dd>

<span data-ttu-id="4fcd8-117">Die-Methode legt die- **Hilfe** Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-117">The method is setting the **Help** property.</span></span>

<span data-ttu-id="4fcd8-118">**Hinweis**  **Hilfe** wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-118">**Note**  **Help** is not supported</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4fcd8-119">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fcd8-119">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcd8-120">Ein Wert, der angibt, ob die durch den *propertyName* -Parameter angegebene Eigenschaft aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-120">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="4fcd8-121"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="4fcd8-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="4fcd8-122">Deaktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-122">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="4fcd8-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="4fcd8-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="4fcd8-124">Aktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-124">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fcd8-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fcd8-125">Return value</span></span>

<span data-ttu-id="4fcd8-126">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4fcd8-127">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4fcd8-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="4fcd8-128">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fcd8-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fcd8-129">Remarks</span></span>

<span data-ttu-id="4fcd8-130">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4fcd8-131">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4fcd8-132">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4fcd8-133">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4fcd8-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fcd8-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fcd8-134">Requirements</span></span>



| <span data-ttu-id="4fcd8-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fcd8-135">Requirement</span></span> | <span data-ttu-id="4fcd8-136">Wert</span><span class="sxs-lookup"><span data-stu-id="4fcd8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcd8-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fcd8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4fcd8-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fcd8-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4fcd8-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fcd8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4fcd8-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fcd8-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4fcd8-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fcd8-141">Namespace</span></span><br/>                | <span data-ttu-id="4fcd8-142">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4fcd8-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4fcd8-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4fcd8-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fcd8-144"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4fcd8-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fcd8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4fcd8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fcd8-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fcd8-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fcd8-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fcd8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fcd8-148">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="4fcd8-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

