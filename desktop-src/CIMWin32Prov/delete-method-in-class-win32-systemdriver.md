---
description: 'Delete-Methode der Win32_SystemDriver-Klasse: Delete&\# 8194; Die WMI-Klassenmethode löscht einen vorhandenen Dienst.'
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Delete-Methode der Win32_SystemDriver Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097088"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="a856b-103">Delete-Methode der Win32 \_ SystemDriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="a856b-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="a856b-104">Die **Delete** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) löscht einen vorhandenen Dienst.</span><span class="sxs-lookup"><span data-stu-id="a856b-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="a856b-105">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a856b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a856b-106">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="a856b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a856b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a856b-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="a856b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a856b-108">Parameters</span></span>

<span data-ttu-id="a856b-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a856b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a856b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a856b-110">Return value</span></span>

<span data-ttu-id="a856b-111">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich gelöscht wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a856b-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a856b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a856b-112">Requirements</span></span>



| <span data-ttu-id="a856b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a856b-113">Requirement</span></span> | <span data-ttu-id="a856b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a856b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a856b-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a856b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a856b-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a856b-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a856b-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a856b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a856b-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a856b-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a856b-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="a856b-119">Namespace</span></span><br/>                | <span data-ttu-id="a856b-120">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="a856b-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a856b-121">MOF</span><span class="sxs-lookup"><span data-stu-id="a856b-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a856b-122"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a856b-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a856b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a856b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a856b-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a856b-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a856b-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a856b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a856b-126">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a856b-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a856b-127">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="a856b-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

