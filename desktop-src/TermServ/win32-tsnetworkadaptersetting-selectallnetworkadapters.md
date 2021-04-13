---
title: Selectallnetworkadapters-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Mit der selectallnetworkadapters-Methode werden alle Netzwerkadapter ausgewählt.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- Selectallnetworkadapters-Methode Remotedesktopdienste
- Selectallnetworkadapters-Methode Remotedesktopdienste, Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste, selectallnetworkadapters-Methode
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f68245c30fbdbf0721d138d1fc0386c779efe111
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340867"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="b0f17-106">Selectallnetworkadapters-Methode der Win32- \_ Klasse "znetworkadaptersetting"</span><span class="sxs-lookup"><span data-stu-id="b0f17-106">SelectAllNetworkAdapters method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="b0f17-107">Mit der **selectallnetworkadapters** -Methode werden alle Netzwerkadapter ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b0f17-107">The **SelectAllNetworkAdapters** method selects all network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f17-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0f17-108">Syntax</span></span>


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a><span data-ttu-id="b0f17-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0f17-109">Parameters</span></span>

<span data-ttu-id="b0f17-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b0f17-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0f17-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0f17-111">Return value</span></span>

<span data-ttu-id="b0f17-112">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0f17-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b0f17-113">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b0f17-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f17-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0f17-114">Remarks</span></span>

<span data-ttu-id="b0f17-115">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b0f17-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b0f17-116">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b0f17-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b0f17-117">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0f17-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b0f17-118">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b0f17-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f17-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0f17-119">Requirements</span></span>



| <span data-ttu-id="b0f17-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0f17-120">Requirement</span></span> | <span data-ttu-id="b0f17-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b0f17-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f17-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0f17-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f17-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0f17-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0f17-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0f17-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f17-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0f17-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0f17-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0f17-126">Namespace</span></span><br/>                | <span data-ttu-id="b0f17-127">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b0f17-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b0f17-128">MOF</span><span class="sxs-lookup"><span data-stu-id="b0f17-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0f17-129"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b0f17-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0f17-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b0f17-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0f17-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0f17-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f17-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0f17-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f17-133">**Win32-Datei "t-Network \_ adaptersetting"**</span><span class="sxs-lookup"><span data-stu-id="b0f17-133">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

