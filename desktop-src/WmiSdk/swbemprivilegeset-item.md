---
description: Die Item-Methode des-Objekts von "taubemprivilegeset" gibt ein-Objekt aus der-Auflistung zurück. Die Item-Methode ist die Standardmethode eines "taubemprivilegeset"-Objekts.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Taubemprivilegeset. Item-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863767"
---
# <a name="swbemprivilegesetitem-method"></a><span data-ttu-id="bc328-104">Taubemprivilegeset. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="bc328-104">SWbemPrivilegeSet.Item method</span></span>

<span data-ttu-id="bc328-105">Die **Item** -Methode des-Objekts von " [**taubemprivilegeset**](swbemprivilegeset.md) " [**gibt ein-**](swbemprivilege.md) Objekt aus der-Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="bc328-105">The **Item** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object returns an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="bc328-106">Die **Item** -Methode ist die Standardmethode eines " **taubemprivilegeset** "-Objekts.</span><span class="sxs-lookup"><span data-stu-id="bc328-106">The **Item** method is the default method of an **SWbemPrivilegeSet** object.</span></span>

<span data-ttu-id="bc328-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bc328-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc328-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc328-108">Syntax</span></span>


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="bc328-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc328-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc328-110">*iprivilege*</span><span class="sxs-lookup"><span data-stu-id="bc328-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="bc328-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc328-111">Required.</span></span> <span data-ttu-id="bc328-112">Eine der WMI-Konstanten aus der [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) -Gruppe.</span><span class="sxs-lookup"><span data-stu-id="bc328-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="bc328-113">Diese Konstanten sind im wesentlichen ganze Zahlen, die bestimmte Berechtigungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="bc328-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="bc328-114">Um z. b. die Berechtigung zu erhalten, mit der Sie ein Windows-System Herunterfahren können, verwenden Sie die Konstante **wbemprivilegeshutdown** oder die numerische Entsprechung 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="bc328-114">For example, to get the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 23 (0x17).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc328-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc328-115">Return value</span></span>

<span data-ttu-id="bc328-116">Bei erfolgreicher Ausführung wird das angeforderte " [**taubemprivilege**](swbemprivilege.md) "-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc328-116">If successful, the requested [**SWbemPrivilege**](swbemprivilege.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc328-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bc328-117">Error codes</span></span>

<span data-ttu-id="bc328-118">Nach dem Abschluss der **Item** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="bc328-118">Upon the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bc328-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bc328-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bc328-120">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bc328-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bc328-121">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="bc328-121">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="bc328-122">Die angegebene Berechtigung ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bc328-122">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bc328-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc328-123">Examples</span></span>

<span data-ttu-id="bc328-124">Im folgenden VBScript-Codebeispiel wird die **Item** -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc328-124">The following VBScript code example uses the **Item** method</span></span>


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a><span data-ttu-id="bc328-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc328-125">Requirements</span></span>



| <span data-ttu-id="bc328-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc328-126">Requirement</span></span> | <span data-ttu-id="bc328-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bc328-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc328-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc328-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bc328-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc328-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc328-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc328-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bc328-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc328-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc328-132">Header</span><span class="sxs-lookup"><span data-stu-id="bc328-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc328-133"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc328-133"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc328-134">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="bc328-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc328-135"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc328-135"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc328-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bc328-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc328-137"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc328-137"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc328-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="bc328-138">CLSID</span></span><br/>                    | <span data-ttu-id="bc328-139">CLSID- \_ Swap-taubemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="bc328-139">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="bc328-140">IID</span><span class="sxs-lookup"><span data-stu-id="bc328-140">IID</span></span><br/>                      | <span data-ttu-id="bc328-141">IID \_ iswbemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="bc328-141">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="bc328-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc328-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc328-143">**Swap-Privileg**</span><span class="sxs-lookup"><span data-stu-id="bc328-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="bc328-144">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="bc328-144">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="bc328-145">**Austausch Berechtigung**</span><span class="sxs-lookup"><span data-stu-id="bc328-145">**SWbemPrivilege**</span></span>](swbemprivilege.md)
</dt> </dl>

 

 




