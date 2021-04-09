---
description: Versucht, einen benutzerdefinierten Steuerelement Code an einen von einem System Treiber verwalteten Dienst zu senden.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: UserControlService-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958549"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="b2e3e-103">UserControlService-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="b2e3e-103">UserControlService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="b2e3e-104">Die **UserControlService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, einen benutzerdefinierten Steuerelement Code an einen von einem System Treiber verwalteten Dienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="b2e3e-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service managed by a system driver.</span></span>

<span data-ttu-id="b2e3e-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2e3e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b2e3e-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b2e3e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e3e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2e3e-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="b2e3e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e3e-109">*ControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2e3e-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e3e-110">Gibt definierte Werte an (von 128 bis 255), die für einen benutzerspezifische Steuerungsbefehle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b2e3e-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e3e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2e3e-111">Return value</span></span>

<span data-ttu-id="b2e3e-112">Gibt den Wert 0 (null) zurück, wenn die **UserControlService** -Anforderung akzeptiert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="b2e3e-112">Returns a value of 0 (zero) if the **UserControlService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e3e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2e3e-113">Requirements</span></span>



| <span data-ttu-id="b2e3e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2e3e-114">Requirement</span></span> | <span data-ttu-id="b2e3e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b2e3e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e3e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2e3e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e3e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2e3e-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2e3e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2e3e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e3e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2e3e-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2e3e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2e3e-120">Namespace</span></span><br/>                | <span data-ttu-id="b2e3e-121">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b2e3e-121">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b2e3e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="b2e3e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2e3e-123"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b2e3e-123"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2e3e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b2e3e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2e3e-125"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2e3e-125"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e3e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2e3e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2e3e-127">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2e3e-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b2e3e-128">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="b2e3e-128">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

