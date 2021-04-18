---
title: Selectnetworkadapterip-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Wählt einen Netzwerkadapter auf der Grundlage der IP-Adresse des Adapters aus.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Selectnetworkadapterip-Methode Remotedesktopdienste
- Selectnetworkadapterip-Methode Remotedesktopdienste, Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste, selectnetworkadapterip-Methode
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339144"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="929d8-106">Selectnetworkadapterip-Methode der Win32- \_ Klasse "tnetworkadaptersetting"</span><span class="sxs-lookup"><span data-stu-id="929d8-106">SelectNetworkAdapterIP method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="929d8-107">Wählt einen Netzwerkadapter auf der Grundlage der IP-Adresse des Adapters aus.</span><span class="sxs-lookup"><span data-stu-id="929d8-107">Selects a network adapter based on the adapter's IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="929d8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="929d8-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a><span data-ttu-id="929d8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="929d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="929d8-110">*Network adapterip* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="929d8-110">*NetworkAdapterIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="929d8-111">Die IP-Adresse des festzulegenden Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="929d8-111">The IP address of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="929d8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="929d8-112">Return value</span></span>

<span data-ttu-id="929d8-113">Gibt 0 (null) zurück, wenn die angegebene IP-Adresse gültig ist, und gibt einen WMI-Fehlercode zurück, wenn die IP-Adresse ungültig oder nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="929d8-113">Returns zero if the specified IP address is valid, and returns a WMI error code if the IP address is invalid or does not exist.</span></span> <span data-ttu-id="929d8-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="929d8-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="929d8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="929d8-115">Remarks</span></span>

<span data-ttu-id="929d8-116">Sie können die IP-Adresse eines Netzwerkadapters abrufen, indem Sie die Eigenschaften der Win32-Klasse "t Network [**\_ adapterlistsetting**](win32-tsnetworkadapterlistsetting.md) " auflisten.</span><span class="sxs-lookup"><span data-stu-id="929d8-116">You can retrieve the IP address of a network adapter by enumerating the properties of the [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) class.</span></span>

<span data-ttu-id="929d8-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="929d8-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="929d8-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="929d8-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="929d8-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="929d8-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="929d8-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="929d8-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="929d8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="929d8-121">Requirements</span></span>



| <span data-ttu-id="929d8-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="929d8-122">Requirement</span></span> | <span data-ttu-id="929d8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="929d8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="929d8-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="929d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="929d8-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="929d8-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="929d8-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="929d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="929d8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="929d8-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="929d8-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="929d8-128">Namespace</span></span><br/>                | <span data-ttu-id="929d8-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="929d8-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="929d8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="929d8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="929d8-131"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="929d8-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="929d8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="929d8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="929d8-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="929d8-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="929d8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="929d8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="929d8-135">**Win32-Datei "t-Network \_ adaptersetting"**</span><span class="sxs-lookup"><span data-stu-id="929d8-135">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

