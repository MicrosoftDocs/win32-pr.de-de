---
title: Die Methode "kreatewinstation" der Win32_TerminalServiceSetting-Klasse
description: Erstellt einen neuen listenerstapel auf der Grundlage der eindeutigen Kombination aus Listenername und NIC.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreatewinstation"
- Methode Remotedesktopdienste der Methode, Win32_TerminalServiceSetting Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, Methode "kreatewinstation"
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339541"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="0cc7a-106">Die Methode "up-WinStation" der Win32- \_ Klasse "terminalservicesetts"</span><span class="sxs-lookup"><span data-stu-id="0cc7a-106">CreateWinstation method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="0cc7a-107">Die **Methode "** Methode" erstellt einen neuen listenerstapel auf der Grundlage der eindeutigen Kombination aus Listenername und NIC.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-107">The **CreateWinstation** method creates a new listener stack based on the unique combination of listener name and NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc7a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cc7a-108">Syntax</span></span>


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a><span data-ttu-id="0cc7a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cc7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cc7a-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cc7a-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cc7a-111">Der Listenername.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-111">Listener name.</span></span>

</dd> <dt>

<span data-ttu-id="0cc7a-112">*Winstadrivername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cc7a-112">*WinstaDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cc7a-113">Der Name des WinStation-Treibers.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-113">The winstation driver name.</span></span>

</dd> <dt>

<span data-ttu-id="0cc7a-114">*LanaID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cc7a-114">*LanaId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cc7a-115">NetBIOS-Nummer des lokalen Netzwerkadapters (Lana) für die NIC.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-115">NetBIOS Local Area Network Adapter (LANA) number for the NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cc7a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cc7a-116">Return value</span></span>

<span data-ttu-id="0cc7a-117">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0cc7a-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc7a-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cc7a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cc7a-119">Remarks</span></span>

<span data-ttu-id="0cc7a-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0cc7a-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0cc7a-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0cc7a-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0cc7a-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc7a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cc7a-124">Requirements</span></span>



| <span data-ttu-id="0cc7a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cc7a-125">Requirement</span></span> | <span data-ttu-id="0cc7a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0cc7a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc7a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cc7a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc7a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cc7a-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cc7a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cc7a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc7a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cc7a-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cc7a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cc7a-131">Namespace</span></span><br/>                | <span data-ttu-id="0cc7a-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0cc7a-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0cc7a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0cc7a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cc7a-134"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0cc7a-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cc7a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0cc7a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cc7a-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cc7a-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc7a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cc7a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc7a-138">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="0cc7a-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

