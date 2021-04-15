---
title: Gettslanaids-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft die NetBIOS-(Lana) IDs und Beschreibungen von Remotedesktopdienste Netzwerkadaptern ab.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- Gettslanaids-Methode Remotedesktopdienste
- Gettslanaids-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, gettslanaids-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479308"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="73bce-106">Gettslanaids-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="73bce-106">GetTSLanaIds method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="73bce-107">Die **gettslanaids** -Methode ruft die NetBIOS-(Lana) IDs und Beschreibungen Remotedesktopdienste Netzwerkadapters ab.</span><span class="sxs-lookup"><span data-stu-id="73bce-107">The **GetTSLanaIds** method gets the NetBIOS Local Area Network Adapter (LANA) IDs and descriptions of Remote Desktop Services network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="73bce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="73bce-108">Syntax</span></span>


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="73bce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="73bce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73bce-110">*Lanaidlist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73bce-110">*LanaIdList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73bce-111">Array von Lana-Zahlen.</span><span class="sxs-lookup"><span data-stu-id="73bce-111">Array of LANA numbers.</span></span>

</dd> <dt>

<span data-ttu-id="73bce-112">*Lanaidbeschreibungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73bce-112">*LanaIdDescriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73bce-113">Ein Array von Lana-Beschreibungen, das dem *lanaidlist* -Array entspricht.</span><span class="sxs-lookup"><span data-stu-id="73bce-113">Array of LANA descriptions corresponding to the *LanaIdList* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73bce-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73bce-114">Return value</span></span>

<span data-ttu-id="73bce-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="73bce-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="73bce-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="73bce-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="73bce-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73bce-117">Remarks</span></span>

<span data-ttu-id="73bce-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="73bce-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73bce-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="73bce-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73bce-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="73bce-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73bce-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="73bce-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73bce-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73bce-122">Requirements</span></span>



| <span data-ttu-id="73bce-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73bce-123">Requirement</span></span> | <span data-ttu-id="73bce-124">Wert</span><span class="sxs-lookup"><span data-stu-id="73bce-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73bce-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73bce-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73bce-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73bce-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73bce-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73bce-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73bce-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73bce-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73bce-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="73bce-129">Namespace</span></span><br/>                | <span data-ttu-id="73bce-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="73bce-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="73bce-131">MOF</span><span class="sxs-lookup"><span data-stu-id="73bce-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73bce-132"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="73bce-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="73bce-133">DLL</span><span class="sxs-lookup"><span data-stu-id="73bce-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73bce-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73bce-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73bce-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73bce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73bce-136">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="73bce-136">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

