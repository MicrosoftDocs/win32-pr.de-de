---
description: Aktiviert den Netzwerkadapter.
ms.assetid: ceb71e1b-5107-420f-a677-814307340469
ms.tgt_platform: multiple
title: Enable-Methode der Win32_NetworkAdapter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a7653d0bcda28ca333bc5c70bdcd69bce382787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214115"
---
# <a name="enable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="e7a92-103">Enable-Methode der Win32- \_ NetworkAdapter-Klasse</span><span class="sxs-lookup"><span data-stu-id="e7a92-103">Enable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="e7a92-104">Die **enable** -Methode aktiviert den Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="e7a92-104">The **Enable** method enables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7a92-105">Syntax</span></span>


```mof
uint32 Enable();
```



## <a name="parameters"></a><span data-ttu-id="e7a92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7a92-106">Parameters</span></span>

<span data-ttu-id="e7a92-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e7a92-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7a92-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7a92-108">Return value</span></span>

<span data-ttu-id="e7a92-109">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e7a92-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="e7a92-110">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="e7a92-110">Any other number indicates an error.</span></span> <span data-ttu-id="e7a92-111">Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e7a92-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7a92-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7a92-112">Remarks</span></span>

<span data-ttu-id="e7a92-113">Die Verwendung dieser Methode kann Schwierigkeiten bereiten, wenn Ihre Anwendung keinen Administrator Zugriff auf Berechtigungen hat.</span><span class="sxs-lookup"><span data-stu-id="e7a92-113">You may experience difficulty using this method if your application does not administrator access privilidges.</span></span>

## <a name="examples"></a><span data-ttu-id="e7a92-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7a92-114">Examples</span></span>

<span data-ttu-id="e7a92-115">Im folgenden Visual Basic Skript Beispiel wird der erste Netzwerkadapter aktiviert und der Status der Eigenschaft " **nettenabled** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7a92-115">The following Visual Basic Script example enables the first network adapter and shows the status of the **NetEnabled** property.</span></span> <span data-ttu-id="e7a92-116">Weitere Informationen finden Sie unter " [**errbemubjectset. ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex)".</span><span class="sxs-lookup"><span data-stu-id="e7a92-116">For more information, see [**SWbemObjectSet.ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colAdapters = _
    objWMIService.Execquery_
        ("Select * from Win32_NetworkAdapter Where NetEnabled=False")
For Each Adapter in colAdapters
    WScript.Echo Adapter.DeviceId & "    " & Adapter.Name
Next
errReturn = colAdapters.ItemIndex(0).Enable()
If errReturn <> 0 Then
    WScript.Echo "Enable Network adapter failed for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId
Else 
    WScript.Echo "Enable Network adapter succeeded for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId 
End If 
WScript.Echo "NetEnabled= " & colAdapters.ItemIndex(0).NetEnabled
```



## <a name="requirements"></a><span data-ttu-id="e7a92-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7a92-117">Requirements</span></span>



| <span data-ttu-id="e7a92-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7a92-118">Requirement</span></span> | <span data-ttu-id="e7a92-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e7a92-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a92-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7a92-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a92-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7a92-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7a92-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7a92-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a92-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7a92-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7a92-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7a92-124">Namespace</span></span><br/>                | <span data-ttu-id="e7a92-125">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e7a92-125">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7a92-126">MOF</span><span class="sxs-lookup"><span data-stu-id="e7a92-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7a92-127"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e7a92-127"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7a92-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e7a92-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7a92-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a92-129"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7a92-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7a92-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a92-131">**Win32- \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="e7a92-131">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="e7a92-132">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="e7a92-132">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="e7a92-133">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="e7a92-133">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

