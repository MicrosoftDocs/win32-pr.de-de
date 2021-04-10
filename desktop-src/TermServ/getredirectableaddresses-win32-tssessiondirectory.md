---
title: Getredirectableadressen-Methode der Win32_TSSessionDirectory-Klasse
description: Ruft die gesamte Liste der für den DNS berechtigten Adressen ab.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Getredirectableadressen-Methode Remotedesktopdienste
- Getredirectableadressen-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, getredirectableadressen-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040126"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="2e11a-106">Getredirectableadressen-Methode der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="2e11a-106">GetRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="2e11a-107">Ruft die gesamte Liste der für den DNS berechtigten Adressen ab.</span><span class="sxs-lookup"><span data-stu-id="2e11a-107">Obtains the entire list of DNS eligible addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e11a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e11a-108">Syntax</span></span>


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a><span data-ttu-id="2e11a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e11a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e11a-110">Kennzeichen *Umleitung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e11a-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e11a-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e11a-111">Type: **uint32**</span></span>

<span data-ttu-id="2e11a-112">Ein Flag, das angibt, ob die Tokenumleitung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e11a-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="2e11a-113">*IP-Adressen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e11a-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e11a-114">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="2e11a-114">Type: **string\[\]**</span></span>

<span data-ttu-id="2e11a-115">Die gesamte Liste der IP-Adressen, die für die Umleitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2e11a-115">The entire list of IP addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="2e11a-116">*Adapternames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e11a-116">*AdapterNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e11a-117">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="2e11a-117">Type: **string\[\]**</span></span>

<span data-ttu-id="2e11a-118">Die Liste der Netzwerkadapter Namen, die den für die Umleitung verfügbaren Adressen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2e11a-118">The list of network adapter names that are associated with the addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="2e11a-119">*Netkonname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e11a-119">*NetConName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e11a-120">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="2e11a-120">Type: **string\[\]**</span></span>

<span data-ttu-id="2e11a-121">Die Liste der Netzwerk Verbindungs Namen, die den für die Umleitung verfügbaren Adressen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2e11a-121">The list of network connection names that are associated with the addresses that are available for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e11a-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e11a-122">Return value</span></span>

<span data-ttu-id="2e11a-123">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e11a-123">Type: **uint32**</span></span>

<span data-ttu-id="2e11a-124">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e11a-124">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2e11a-125">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2e11a-125">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e11a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e11a-126">Remarks</span></span>

<span data-ttu-id="2e11a-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="2e11a-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e11a-128">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="2e11a-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2e11a-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2e11a-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e11a-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2e11a-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e11a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e11a-131">Requirements</span></span>



| <span data-ttu-id="2e11a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e11a-132">Requirement</span></span> | <span data-ttu-id="2e11a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2e11a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e11a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e11a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2e11a-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2e11a-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2e11a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e11a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2e11a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e11a-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e11a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e11a-138">Namespace</span></span><br/>                | <span data-ttu-id="2e11a-139">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2e11a-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2e11a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2e11a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e11a-141"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e11a-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e11a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2e11a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e11a-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e11a-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e11a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e11a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e11a-145">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="2e11a-145">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

