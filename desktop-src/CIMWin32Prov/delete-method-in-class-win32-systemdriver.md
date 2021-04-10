---
description: Der Lösch&\# 8194; WMI-Klassenmethode löscht einen vorhandenen Dienst.
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Delete-Methode der Win32_SystemDriver-Klasse
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
ms.openlocfilehash: 807fa6090fe2e088fb3900feb7f2068751ad2df6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861224"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="e5ea0-103">Delete-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="e5ea0-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="e5ea0-104">Mit der **Delete** [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode wird ein vorhandener Dienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e5ea0-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="e5ea0-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5ea0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e5ea0-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e5ea0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ea0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5ea0-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="e5ea0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5ea0-108">Parameters</span></span>

<span data-ttu-id="e5ea0-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e5ea0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5ea0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5ea0-110">Return value</span></span>

<span data-ttu-id="e5ea0-111">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich gelöscht wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="e5ea0-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ea0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5ea0-112">Requirements</span></span>



| <span data-ttu-id="e5ea0-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5ea0-113">Requirement</span></span> | <span data-ttu-id="e5ea0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e5ea0-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ea0-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5ea0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ea0-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5ea0-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5ea0-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5ea0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ea0-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5ea0-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5ea0-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5ea0-119">Namespace</span></span><br/>                | <span data-ttu-id="e5ea0-120">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e5ea0-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e5ea0-121">MOF</span><span class="sxs-lookup"><span data-stu-id="e5ea0-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5ea0-122"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e5ea0-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5ea0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e5ea0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5ea0-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5ea0-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ea0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5ea0-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5ea0-126">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e5ea0-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e5ea0-127">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="e5ea0-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

