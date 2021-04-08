---
title: Selectnetworkadapter-Methode der Win32_TSVirtualIP-Klasse
description: Legt die Mac-Adresse des Netzwerkadapters fest, der für die IP-Virtualisierung verwendet werden soll.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Selectnetworkadapter-Methode Remotedesktopdienste
- Selectnetworkadapter-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, selectnetworkadapter-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949796"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="60d88-106">Selectnetworkadapter-Methode der Win32- \_ Klasse "tvirtualip"</span><span class="sxs-lookup"><span data-stu-id="60d88-106">SelectNetworkAdapter method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="60d88-107">Legt die Mac-Adresse des Netzwerkadapters fest, der für die IP-Virtualisierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60d88-107">Sets the MAC address of the network adapter to use for IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d88-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="60d88-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="60d88-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="60d88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d88-110">*Networkadaptermacaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60d88-110">*NetworkAdapterMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d88-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60d88-111">Type: **string**</span></span>

<span data-ttu-id="60d88-112">Gibt die Mac-Adresse des Netzwerkadapters an.</span><span class="sxs-lookup"><span data-stu-id="60d88-112">Specifies the MAC address of the network adapter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60d88-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60d88-113">Return value</span></span>

<span data-ttu-id="60d88-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60d88-114">Type: **uint32**</span></span>

<span data-ttu-id="60d88-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60d88-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="60d88-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="60d88-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

<span data-ttu-id="60d88-117">Wenn die Mac-Adresse ungültig ist oder nicht vorhanden ist oder der IP-Virtualisierungsmodus pro Sitzung erfolgt, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60d88-117">If the MAC address is invalid or does not exist, or if the IP virtualization mode is per-session, an error is returned.</span></span>

<span data-ttu-id="60d88-118">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="60d88-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="60d88-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60d88-119">Requirements</span></span>



| <span data-ttu-id="60d88-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60d88-120">Requirement</span></span> | <span data-ttu-id="60d88-121">Wert</span><span class="sxs-lookup"><span data-stu-id="60d88-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60d88-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60d88-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60d88-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="60d88-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="60d88-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60d88-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60d88-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60d88-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="60d88-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="60d88-126">Namespace</span></span><br/>                | <span data-ttu-id="60d88-127">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="60d88-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="60d88-128">MOF</span><span class="sxs-lookup"><span data-stu-id="60d88-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60d88-129"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60d88-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="60d88-130">DLL</span><span class="sxs-lookup"><span data-stu-id="60d88-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60d88-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60d88-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d88-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60d88-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d88-133">**Win32- \_ virtualialip**</span><span class="sxs-lookup"><span data-stu-id="60d88-133">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





