---
description: Durch die Add-Methode des Objekts "Swap-Objekt" wird der "Swap-Auflistung"-Auflistung ein "taubemprivilege"-Objekt hinzugefügt. Wenn eine Berechtigung mit dem gleichen Namen bereits in der Sammlung vorhanden ist, wird Sie ersetzt.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Taubemprivilegeset. Add-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041999"
---
# <a name="swbemprivilegesetadd-method"></a><span data-ttu-id="29e7e-104">Taubemprivilegeset. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="29e7e-104">SWbemPrivilegeSet.Add method</span></span>

<span data-ttu-id="29e7e-105">Durch die **Add** -Methode des Objekts " [**Swap**](swbemprivilegeset.md) -Objekt" wird der " **Swap** -Auflistung"-Auflistung ein " [**taubemprivilege**](swbemprivilege.md) "-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="29e7e-105">The **Add** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection.</span></span> <span data-ttu-id="29e7e-106">Wenn eine Berechtigung mit dem gleichen Namen bereits in der Sammlung vorhanden ist, wird Sie ersetzt.</span><span class="sxs-lookup"><span data-stu-id="29e7e-106">If a privilege with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="29e7e-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="29e7e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="29e7e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="29e7e-108">Syntax</span></span>


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="29e7e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29e7e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29e7e-110">*iprivilege*</span><span class="sxs-lookup"><span data-stu-id="29e7e-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="29e7e-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29e7e-111">Required.</span></span> <span data-ttu-id="29e7e-112">Eine der WMI-Konstanten aus der [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) -Gruppe.</span><span class="sxs-lookup"><span data-stu-id="29e7e-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="29e7e-113">Diese Konstanten sind im wesentlichen ganze Zahlen, die bestimmte Berechtigungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="29e7e-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="29e7e-114">Wenn Sie z. b. die Berechtigung hinzufügen möchten, mit der Sie ein Computersystem Herunterfahren können, verwenden Sie die Konstante **wbemprivilegeshutdown** .</span><span class="sxs-lookup"><span data-stu-id="29e7e-114">For example, to add the privilege that allows you to shut down a computer system, use the **wbemPrivilegeShutdown** constant.</span></span> <span data-ttu-id="29e7e-115">In einem Skript müssen Sie die numerische Entsprechung von 23 (0x17) verwenden.</span><span class="sxs-lookup"><span data-stu-id="29e7e-115">In a script, you must use the numeric equivalent of 23 (0x17).</span></span> <span data-ttu-id="29e7e-116">Eine umfassende Liste dieser Konstanten und der zugehörigen Berechtigungs Zeichenfolgen finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="29e7e-116">For a complete list of these constants and the associated privilege strings, see [**Privilege Constants**](privilege-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="29e7e-117">*bisenabled* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="29e7e-117">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29e7e-118">Boolescher Wert, der dieses Privileg aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="29e7e-118">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="29e7e-119">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="29e7e-119">The default value is **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29e7e-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29e7e-120">Return value</span></span>

<span data-ttu-id="29e7e-121">Bei erfolgreicher Ausführung gibt die Methode ein-Objekt zurück, das die [**neue Berechtigung darstellt**](swbemprivilege.md) .</span><span class="sxs-lookup"><span data-stu-id="29e7e-121">If successful, the method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="29e7e-122">Andernfalls wird ein NULL-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29e7e-122">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="29e7e-123">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="29e7e-123">Error codes</span></span>

<span data-ttu-id="29e7e-124">Nach Abschluss der **Add** -Methode kann das **Err** -Objekt den Fehlercode in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="29e7e-124">Upon the completion of the **Add** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="29e7e-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="29e7e-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="29e7e-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="29e7e-126">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="29e7e-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29e7e-127">Examples</span></span>

<span data-ttu-id="29e7e-128">Ein Codebeispiel, in dem diese Methode verwendet wird, wird im Thema " [**chanbemprivilegeset**](swbemprivilegeset.md) " beschrieben.</span><span class="sxs-lookup"><span data-stu-id="29e7e-128">A code example using this method is described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="29e7e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29e7e-129">Requirements</span></span>



| <span data-ttu-id="29e7e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29e7e-130">Requirement</span></span> | <span data-ttu-id="29e7e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="29e7e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29e7e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29e7e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="29e7e-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29e7e-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29e7e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29e7e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="29e7e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29e7e-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29e7e-136">Header</span><span class="sxs-lookup"><span data-stu-id="29e7e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="29e7e-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="29e7e-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="29e7e-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="29e7e-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="29e7e-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="29e7e-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="29e7e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="29e7e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29e7e-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29e7e-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="29e7e-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="29e7e-142">CLSID</span></span><br/>                    | <span data-ttu-id="29e7e-143">CLSID- \_ Swap-taubemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="29e7e-143">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="29e7e-144">IID</span><span class="sxs-lookup"><span data-stu-id="29e7e-144">IID</span></span><br/>                      | <span data-ttu-id="29e7e-145">IID \_ iswbemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="29e7e-145">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="29e7e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29e7e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e7e-147">**Swap-Privileg**</span><span class="sxs-lookup"><span data-stu-id="29e7e-147">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="29e7e-148">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="29e7e-148">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="29e7e-149">Ausführen privilegierter Vorgänge mit VBScript</span><span class="sxs-lookup"><span data-stu-id="29e7e-149">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="29e7e-150">**"Taubemprivilegeset. addasstring"**</span><span class="sxs-lookup"><span data-stu-id="29e7e-150">**SWbemPrivilegeSet.AddAsString**</span></span>](swbemprivilegeset-addasstring.md)
</dt> <dt>

[<span data-ttu-id="29e7e-151">**"Swap-privilegeset. Remove"**</span><span class="sxs-lookup"><span data-stu-id="29e7e-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="29e7e-152">**Wbemprivilegeumum**</span><span class="sxs-lookup"><span data-stu-id="29e7e-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="29e7e-153">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="29e7e-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




