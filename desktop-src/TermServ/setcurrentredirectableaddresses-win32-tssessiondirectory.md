---
title: Setcurrentredirectableadressen-Methode der Win32_TSSessionDirectory-Klasse
description: Legt die konfigurierte Liste der für die Umleitung zu verwendenden DNS-Adressen fest.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Setcurrentredirectableadressen-Methode Remotedesktopdienste
- Setcurrentredirectableadressen-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, setcurrentredirectableadressen-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e70f8d108e908155b5db3e6800f4be26811c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392067"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="f8bef-106">Setcurrentredirectableadressen-Methode der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="f8bef-106">SetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="f8bef-107">Mit der **setcurrentredirectableadressen** -Methode wird die konfigurierte Liste der für die Umleitung zu verwendenden DNS-Adressen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8bef-107">The **SetCurrentRedirectableAddresses** method sets the configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8bef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8bef-108">Syntax</span></span>


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="f8bef-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8bef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8bef-110">Kennzeichen *Umleitung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8bef-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8bef-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8bef-111">Type: **uint32**</span></span>

<span data-ttu-id="f8bef-112">Ein Flag, das angibt, ob die Tokenumleitung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8bef-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f8bef-113">*IP-Adressen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8bef-113">*IPAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8bef-114">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="f8bef-114">Type: **string\[\]**</span></span>

<span data-ttu-id="f8bef-115">Ein Array von Zeichen folgen, das die Liste der für die Umleitung geeigneten IP-Adressen darstellt, die für die Umleitung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f8bef-115">An array of strings that represents the list of DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8bef-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8bef-116">Return value</span></span>

<span data-ttu-id="f8bef-117">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8bef-117">Type: **uint32**</span></span>

<span data-ttu-id="f8bef-118">Gibt bei Erfolg 0 zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8bef-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="f8bef-119">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f8bef-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8bef-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8bef-120">Remarks</span></span>

<span data-ttu-id="f8bef-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f8bef-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f8bef-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f8bef-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f8bef-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f8bef-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f8bef-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f8bef-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8bef-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8bef-125">Requirements</span></span>



| <span data-ttu-id="f8bef-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8bef-126">Requirement</span></span> | <span data-ttu-id="f8bef-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f8bef-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8bef-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8bef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f8bef-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f8bef-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f8bef-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8bef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f8bef-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8bef-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8bef-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8bef-132">Namespace</span></span><br/>                | <span data-ttu-id="f8bef-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f8bef-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f8bef-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f8bef-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8bef-135"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f8bef-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8bef-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f8bef-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8bef-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8bef-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8bef-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8bef-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8bef-139">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="f8bef-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

