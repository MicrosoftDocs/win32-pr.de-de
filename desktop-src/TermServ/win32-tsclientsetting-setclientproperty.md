---
title: Setclientproperty-Methode der Win32_TSClientSetting-Klasse
description: Die setclientproperty-Methode legt die lptportmapping-, COMPortMapping-, audiomapping-, ClipboardMapping-, DriveMapping-oder WindowsPrinterMapping-Eigenschaft für die-Klasse fest.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Setclientproperty-Methode Remotedesktopdienste
- Setclientproperty-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setclientproperty-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341794"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="7a745-106">Setclientproperty-Methode der Win32- \_ Klasse "tsclientsetting"</span><span class="sxs-lookup"><span data-stu-id="7a745-106">SetClientProperty method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="7a745-107">Die **setclientproperty** -Methode legt die **lptportmapping**-, **COMPortMapping**-, **audiomapping**-, **ClipboardMapping**-, **DriveMapping**-oder **WindowsPrinterMapping** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="7a745-107">The **SetClientProperty** method sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a745-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a745-108">Syntax</span></span>


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="7a745-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a745-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a745-110">*PropertyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a745-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a745-111">Gibt die Client Eigenschaft an, die von der-Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7a745-111">Specifies the client property that the method is setting.</span></span>

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span data-ttu-id="7a745-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**Audiomapping**</span><span class="sxs-lookup"><span data-stu-id="7a745-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-113">Die-Methode legt die **audiomapping** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7a745-113">The method is setting the **AudioMapping** property.</span></span>

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span data-ttu-id="7a745-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="7a745-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-115">Die-Methode legt die **ClipboardMapping** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7a745-115">The method is setting the **ClipboardMapping** property.</span></span>

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span data-ttu-id="7a745-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="7a745-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-117">Die-Methode legt die **COMPortMapping** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7a745-117">The method is setting the **COMPortMapping** property.</span></span>

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span data-ttu-id="7a745-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="7a745-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-119">Die-Methode legt die **DriveMapping** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7a745-119">The method is setting the **DriveMapping** property.</span></span>

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span data-ttu-id="7a745-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**Lptportmapping**</span><span class="sxs-lookup"><span data-stu-id="7a745-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-121">Die-Methode legt die **lptportmapping** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7a745-121">The method is setting the **LPTPortMapping** property.</span></span>

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span data-ttu-id="7a745-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**Pnpredirection**</span><span class="sxs-lookup"><span data-stu-id="7a745-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-123">Die-Methode legt die **pnpredirection** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7a745-123">The method is setting the **PNPRedirection** property.</span></span>

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span data-ttu-id="7a745-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="7a745-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-125">Die-Methode legt die **WindowsPrinterMapping** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7a745-125">The method is setting the **WindowsPrinterMapping** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7a745-126">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a745-126">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a745-127">Ein Wert, der angibt, ob die durch den *propertyName* -Parameter angegebene Eigenschaft aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a745-127">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="7a745-128"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="7a745-128"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-129">Deaktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7a745-129">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="7a745-130"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="7a745-130"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="7a745-131">Aktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7a745-131">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a745-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a745-132">Return value</span></span>

<span data-ttu-id="7a745-133">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a745-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7a745-134">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7a745-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="7a745-135">Die-Methode gibt einen Fehler zurück, wenn die angegebene Client Eigenschaft nicht unter der Gruppenrichtlinien Steuerung liegt oder wenn die-Eigenschafts Einstellung nicht vom Server außer Kraft gesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a745-135">The method returns an error if the specified client property is not under group policy control or if the property setting is not eligible for override by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a745-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a745-136">Remarks</span></span>

<span data-ttu-id="7a745-137">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7a745-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7a745-138">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="7a745-138">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7a745-139">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7a745-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7a745-140">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7a745-140">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a745-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a745-141">Requirements</span></span>



| <span data-ttu-id="7a745-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a745-142">Requirement</span></span> | <span data-ttu-id="7a745-143">Wert</span><span class="sxs-lookup"><span data-stu-id="7a745-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a745-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a745-144">Minimum supported client</span></span><br/> | <span data-ttu-id="7a745-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a745-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a745-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a745-146">Minimum supported server</span></span><br/> | <span data-ttu-id="7a745-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a745-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a745-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a745-148">Namespace</span></span><br/>                | <span data-ttu-id="7a745-149">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7a745-149">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7a745-150">MOF</span><span class="sxs-lookup"><span data-stu-id="7a745-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a745-151"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7a745-151"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a745-152">DLL</span><span class="sxs-lookup"><span data-stu-id="7a745-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a745-153"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a745-153"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a745-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a745-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a745-155">**Win32- \_ tsclientsetting**</span><span class="sxs-lookup"><span data-stu-id="7a745-155">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

