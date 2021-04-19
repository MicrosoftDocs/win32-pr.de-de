---
description: Deaktiviert den Netzwerkadapter.
ms.assetid: 6b328d7c-a9ef-4c9b-bc32-13fa2e0f65eb
ms.tgt_platform: multiple
title: Deaktivieren der Methode der Win32_NetworkAdapter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a9c6b1a506310460d9131709092b739f68986e02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346221"
---
# <a name="disable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="071e9-103">Deaktivieren der Methode der Win32- \_ NetworkAdapter-Klasse</span><span class="sxs-lookup"><span data-stu-id="071e9-103">Disable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="071e9-104">Die Methode " **Deaktivieren** " deaktiviert den Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="071e9-104">The **Disable** method disables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="071e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="071e9-105">Syntax</span></span>


```mof
uint32 Disable();
```



## <a name="parameters"></a><span data-ttu-id="071e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="071e9-106">Parameters</span></span>

<span data-ttu-id="071e9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="071e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="071e9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="071e9-108">Return value</span></span>

<span data-ttu-id="071e9-109">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="071e9-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="071e9-110">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="071e9-110">Any other number indicates an error.</span></span> <span data-ttu-id="071e9-111">Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="071e9-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="071e9-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="071e9-112">Requirements</span></span>



| <span data-ttu-id="071e9-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="071e9-113">Requirement</span></span> | <span data-ttu-id="071e9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="071e9-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="071e9-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="071e9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="071e9-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="071e9-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="071e9-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="071e9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="071e9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="071e9-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="071e9-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="071e9-119">Namespace</span></span><br/>                | <span data-ttu-id="071e9-120">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="071e9-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="071e9-121">MOF</span><span class="sxs-lookup"><span data-stu-id="071e9-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="071e9-122"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="071e9-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="071e9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="071e9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="071e9-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="071e9-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="071e9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="071e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071e9-126">**Win32- \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="071e9-126">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="071e9-127">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="071e9-127">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="071e9-128">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="071e9-128">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

