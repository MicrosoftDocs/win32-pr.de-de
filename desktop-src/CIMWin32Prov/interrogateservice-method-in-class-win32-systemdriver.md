---
description: Fordert an, dass der System Treiber Dienst seinen Status auf Service Manager aktualisiert.
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: InterrogateService-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 666a261dfe3fac7dd62e6253c5eb4804b3a55677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126481"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="97cb8-103">InterrogateService-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="97cb8-103">InterrogateService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="97cb8-104">Die Methode " **InterrogateService** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " fordert an, dass der System Treiber Dienst seinen Status auf den Dienst-Manager aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="97cb8-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the system driver service update its state to the service manager.</span></span>

<span data-ttu-id="97cb8-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="97cb8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="97cb8-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="97cb8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="97cb8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97cb8-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="97cb8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97cb8-108">Parameters</span></span>

<span data-ttu-id="97cb8-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="97cb8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97cb8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97cb8-110">Return value</span></span>

<span data-ttu-id="97cb8-111">Gibt einen Wert von 0 (null) zurück, wenn die Anfrage **gateservice** -Anforderung akzeptiert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="97cb8-111">Returns a value of 0 (zero) if the **InterrogateService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="97cb8-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97cb8-112">Requirements</span></span>



| <span data-ttu-id="97cb8-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97cb8-113">Requirement</span></span> | <span data-ttu-id="97cb8-114">Wert</span><span class="sxs-lookup"><span data-stu-id="97cb8-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97cb8-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97cb8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="97cb8-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97cb8-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97cb8-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97cb8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="97cb8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97cb8-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97cb8-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="97cb8-119">Namespace</span></span><br/>                | <span data-ttu-id="97cb8-120">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="97cb8-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97cb8-121">MOF</span><span class="sxs-lookup"><span data-stu-id="97cb8-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97cb8-122"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="97cb8-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97cb8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="97cb8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97cb8-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97cb8-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97cb8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97cb8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97cb8-126">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="97cb8-126">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> <dt>

<span data-ttu-id="97cb8-127">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97cb8-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="97cb8-128">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="97cb8-128">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

