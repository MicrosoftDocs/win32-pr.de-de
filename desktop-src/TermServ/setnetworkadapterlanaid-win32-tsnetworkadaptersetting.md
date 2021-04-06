---
title: Setnetworkadapterlanaid-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Gibt die Nummer des lokalen Netzwerkadapters (Lana) des festzulegenden Netzwerkadapters an.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Setnetworkadapterlanaid-Methode Remotedesktopdienste
- Setnetworkadapterlanaid-Methode Remotedesktopdienste, Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste, setnetworkadapterlanaid-Methode
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743496"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="683f6-106">Setnetworkadapterlanaid-Methode der Win32- \_ Klasse "znetworkadaptersetting"</span><span class="sxs-lookup"><span data-stu-id="683f6-106">SetNetworkAdapterLanaID method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="683f6-107">Die **setnetworkadapterlanaid** -Methode gibt die Nummer des lokalen Netzwerkadapters (Lana) des festzulegenden Netzwerkadapters an.</span><span class="sxs-lookup"><span data-stu-id="683f6-107">The **SetNetworkAdapterLanaID** method specifies the Local Area Network Adapter (LANA) number of the network adapter to set.</span></span> <span data-ttu-id="683f6-108">Wenn die angegebene Lana-ID ungültig ist oder nicht vorhanden ist, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="683f6-108">If the LANA ID specified is not valid or does not exist, an error is returned.</span></span> <span data-ttu-id="683f6-109">Die Liste der verfügbaren Lana-IDs wird durch Aufzählen der **deviceidlist** -Eigenschaft in der Win32-Klasse " [**\_ tnetworkadaptersetting**](win32-tsnetworkadaptersetting.md) " abgerufen.</span><span class="sxs-lookup"><span data-stu-id="683f6-109">The available list of LANA IDs is obtained by enumerating the property **DeviceIDList** in the [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="683f6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="683f6-110">Syntax</span></span>


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a><span data-ttu-id="683f6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="683f6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="683f6-112">*Networkadapterlanaid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="683f6-112">*NetworkAdapterLanaID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="683f6-113">Lana-Nummer des festzulegenden Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="683f6-113">LANA number of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="683f6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="683f6-114">Return value</span></span>

<span data-ttu-id="683f6-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="683f6-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="683f6-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="683f6-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="683f6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="683f6-117">Remarks</span></span>

<span data-ttu-id="683f6-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="683f6-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="683f6-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="683f6-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="683f6-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="683f6-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="683f6-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="683f6-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="683f6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="683f6-122">Requirements</span></span>



| <span data-ttu-id="683f6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="683f6-123">Requirement</span></span> | <span data-ttu-id="683f6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="683f6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="683f6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="683f6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="683f6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="683f6-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="683f6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="683f6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="683f6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="683f6-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="683f6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="683f6-129">Namespace</span></span><br/>                | <span data-ttu-id="683f6-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="683f6-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="683f6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="683f6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="683f6-132"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="683f6-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="683f6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="683f6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="683f6-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683f6-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683f6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="683f6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683f6-136">**Win32-Datei "t-Network \_ adaptersetting"**</span><span class="sxs-lookup"><span data-stu-id="683f6-136">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

