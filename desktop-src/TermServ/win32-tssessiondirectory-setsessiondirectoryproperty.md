---
title: Die Methode "Methode" der Klasse "Win32_TSSessionDirectory"
description: Legt die SessionDirectoryLocation-Eigenschaft oder die SessionDirectoryClusterName-Eigenschaft für die-Klasse fest.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "Win32_TSSessionDirectory Klasse"
- Win32_TSSessionDirectory Klasse Remotedesktopdienste, Methode "Methode"
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476191"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="1e30d-106">Die Methode "stenessiondirectoryproperty" der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="1e30d-106">SetSessionDirectoryProperty method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="1e30d-107">Legt die **SessionDirectoryLocation** -Eigenschaft oder die **SessionDirectoryClusterName** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="1e30d-107">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e30d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e30d-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="1e30d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e30d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e30d-110">*PropertyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e30d-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e30d-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e30d-111">Type: **string**</span></span>

<span data-ttu-id="1e30d-112">Gibt die Eigenschaft an, die von der Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1e30d-112">Specifies the property that the method is setting.</span></span>

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span data-ttu-id="1e30d-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**Sessiondirectoriylocation**</span><span class="sxs-lookup"><span data-stu-id="1e30d-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span></span>


</dt> <dd>

<span data-ttu-id="1e30d-114">Die-Methode legt die **SessionDirectoryLocation** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="1e30d-114">The method is setting the **SessionDirectoryLocation** property.</span></span>

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span data-ttu-id="1e30d-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**Sessiondirectoriyclustername**</span><span class="sxs-lookup"><span data-stu-id="1e30d-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span></span>


</dt> <dd>

<span data-ttu-id="1e30d-116">Die-Methode legt die **SessionDirectoryClusterName** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="1e30d-116">The method is setting the **SessionDirectoryClusterName** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1e30d-117">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e30d-117">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e30d-118">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e30d-118">Type: **string**</span></span>

<span data-ttu-id="1e30d-119">Der neue Wert für die Eigenschaft, die durch den *propertyName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1e30d-119">The new value for the property specified by the *PropertyName* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e30d-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e30d-120">Return value</span></span>

<span data-ttu-id="1e30d-121">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e30d-121">Type: **uint32**</span></span>

<span data-ttu-id="1e30d-122">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e30d-122">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1e30d-123">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1e30d-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1e30d-124">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="1e30d-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e30d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e30d-125">Remarks</span></span>

<span data-ttu-id="1e30d-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1e30d-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1e30d-127">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="1e30d-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1e30d-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1e30d-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1e30d-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1e30d-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e30d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e30d-130">Requirements</span></span>



| <span data-ttu-id="1e30d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e30d-131">Requirement</span></span> | <span data-ttu-id="1e30d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1e30d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e30d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e30d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1e30d-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1e30d-134">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1e30d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e30d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1e30d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e30d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e30d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e30d-137">Namespace</span></span><br/>                | <span data-ttu-id="1e30d-138">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1e30d-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1e30d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1e30d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e30d-140"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1e30d-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e30d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1e30d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e30d-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e30d-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e30d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e30d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e30d-144">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="1e30d-144">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

