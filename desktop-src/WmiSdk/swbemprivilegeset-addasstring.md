---
description: Mithilfe der addasstring-Methode des Objekts "taubemprivilegeset" können Sie einer "taubemprivilegeset"-Sammlung mithilfe einer Berechtigungs Zeichenfolge eine Berechtigung hinzufügen.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Methode ' Swap. addasstring ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369852"
---
# <a name="swbemprivilegesetaddasstring-method"></a><span data-ttu-id="c81e8-103">Taubemprivilegeset. addasstring-Methode</span><span class="sxs-lookup"><span data-stu-id="c81e8-103">SWbemPrivilegeSet.AddAsString method</span></span>

<span data-ttu-id="c81e8-104">Mithilfe der **addasstring** -Methode des Objekts " [**taubemprivilegeset**](swbemprivilegeset.md) " können Sie einer " **taubemprivilegeset** "-Sammlung mithilfe einer Berechtigungs Zeichenfolge eine Berechtigung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c81e8-104">You can use the **AddAsString** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object to add a privilege to an **SWbemPrivilegeSet** collection using a privilege string.</span></span> <span data-ttu-id="c81e8-105">Verwenden Sie diese Methode, um eine Berechtigung hinzuzufügen oder um eine Berechtigung für " [**Swap Security**](swbemsecurity.md) "-Objekte zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c81e8-105">Use this method to add a privilege or to enable a privilege for [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="c81e8-106">Weitere Informationen finden [Sie unter Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="c81e8-106">See [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="c81e8-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c81e8-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c81e8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c81e8-108">Syntax</span></span>


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c81e8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c81e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c81e8-110">*"Strauch Berechtigung"*</span><span class="sxs-lookup"><span data-stu-id="c81e8-110">*strPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="c81e8-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c81e8-111">Required.</span></span> <span data-ttu-id="c81e8-112">Eine der Berechtigungs Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="c81e8-112">One of the privilege strings.</span></span> <span data-ttu-id="c81e8-113">Eine umfassende Liste dieser Zeichen folgen und der zugehörigen WMI-Konstanten finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c81e8-113">For a complete list of these strings and the associated WMI constants, see [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="c81e8-114">Jede Berechtigungs Zeichenfolge stellt eine bestimmte Berechtigung dar.</span><span class="sxs-lookup"><span data-stu-id="c81e8-114">Every privilege string represents a specific privilege.</span></span> <span data-ttu-id="c81e8-115">Wenn Sie z. b. die Berechtigung hinzufügen möchten, mit der ein Computersystem heruntergefahren wird, verwenden Sie die Zeichenfolge **SeShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="c81e8-115">For example, to add the privilege that use to shut down a computer system, use the **SeShutdownPrivilege** string.</span></span>

</dd> <dt>

<span data-ttu-id="c81e8-116">*bisenabled* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="c81e8-116">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c81e8-117">Boolescher Wert, der dieses Privileg aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c81e8-117">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="c81e8-118">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="c81e8-118">The default value is **True**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c81e8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c81e8-119">Return value</span></span>

<span data-ttu-id="c81e8-120">Wenn der Vorgang erfolgreich ist, gibt diese Methode ein-Objekt zurück, das die [**neue Berechtigung darstellt**](swbemprivilege.md) .</span><span class="sxs-lookup"><span data-stu-id="c81e8-120">If successful, this method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="c81e8-121">Andernfalls wird ein NULL-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c81e8-121">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c81e8-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c81e8-122">Error codes</span></span>

<span data-ttu-id="c81e8-123">Nach Abschluss der **addasstring** -Methode kann das **Err** -Objekt den Fehlercode in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="c81e8-123">Upon the completion of the **AddAsString** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c81e8-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c81e8-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c81e8-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c81e8-125">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c81e8-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c81e8-126">Examples</span></span>

<span data-ttu-id="c81e8-127">Im folgenden VBScript-Codebeispiel wird ein neuer Port für einen Druckserver mit [**Win32 \_ tcpipprinterport**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport)erstellt.</span><span class="sxs-lookup"><span data-stu-id="c81e8-127">The following VBScript code example creates a new port for a print server using [**Win32\_TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span></span> <span data-ttu-id="c81e8-128">Für diesen Vorgang ist die **SeLoadDriverPrivilege-Berechtigung** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c81e8-128">The **SeLoadDriverPrivilege** is required for this operation.</span></span> <span data-ttu-id="c81e8-129">Siehe [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c81e8-129">See [Executing Privileged Operations](executing-privileged-operations.md).</span></span>


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



<span data-ttu-id="c81e8-130">Ein Codebeispiel, in dem diese Methode verwendet wird, wird auch im Thema " [**chanbemprivilegeset**](swbemprivilegeset.md) " beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c81e8-130">A code example using this method is also described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81e8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c81e8-131">Requirements</span></span>



| <span data-ttu-id="c81e8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c81e8-132">Requirement</span></span> | <span data-ttu-id="c81e8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="c81e8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c81e8-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c81e8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c81e8-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c81e8-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c81e8-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c81e8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c81e8-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c81e8-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c81e8-138">Header</span><span class="sxs-lookup"><span data-stu-id="c81e8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c81e8-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c81e8-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c81e8-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c81e8-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="c81e8-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c81e8-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c81e8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c81e8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c81e8-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c81e8-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c81e8-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="c81e8-144">CLSID</span></span><br/>                    | <span data-ttu-id="c81e8-145">CLSID- \_ Swap-taubemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="c81e8-145">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="c81e8-146">IID</span><span class="sxs-lookup"><span data-stu-id="c81e8-146">IID</span></span><br/>                      | <span data-ttu-id="c81e8-147">IID \_ iswbemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="c81e8-147">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="c81e8-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c81e8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81e8-149">**Swap-Privileg**</span><span class="sxs-lookup"><span data-stu-id="c81e8-149">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="c81e8-150">**Austauschen von "taubemprivilegeset. Add"**</span><span class="sxs-lookup"><span data-stu-id="c81e8-150">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> <dt>

[<span data-ttu-id="c81e8-151">**"Swap-privilegeset. Remove"**</span><span class="sxs-lookup"><span data-stu-id="c81e8-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="c81e8-152">**Wbemprivilegeumum**</span><span class="sxs-lookup"><span data-stu-id="c81e8-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="c81e8-153">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="c81e8-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="c81e8-154">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="c81e8-154">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="c81e8-155">Ausführen privilegierter Vorgänge mit VBScript</span><span class="sxs-lookup"><span data-stu-id="c81e8-155">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

