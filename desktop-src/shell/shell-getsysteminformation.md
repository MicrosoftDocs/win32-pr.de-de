---
description: 'Shell.GetSystemInformation-Methode: Ruft Systeminformationen ab.'
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Shell.GetSystemInformation-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9e021e767309007cfee2cfc78268fb7d7cea042
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104278"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="a7d09-103">Shell.GetSystemInformation-Methode</span><span class="sxs-lookup"><span data-stu-id="a7d09-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="a7d09-104">Ruft Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="a7d09-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7d09-105">Syntax</span></span>


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="a7d09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7d09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d09-107">*sName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a7d09-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d09-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a7d09-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a7d09-109">Eine **Zeichenfolge,** die die angeforderten Systeminformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="a7d09-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d09-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7d09-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a7d09-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a7d09-111">JScript</span></span>

<span data-ttu-id="a7d09-112">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="a7d09-112">Type: **Variant**</span></span>

<span data-ttu-id="a7d09-113">Gibt den Wert der angeforderten Systeminformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="a7d09-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="a7d09-114">Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a7d09-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="a7d09-115">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="a7d09-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="a7d09-116">VB</span><span class="sxs-lookup"><span data-stu-id="a7d09-116">VB</span></span>

<span data-ttu-id="a7d09-117">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="a7d09-117">Type: **Variant**</span></span>

<span data-ttu-id="a7d09-118">Gibt den Wert der angeforderten Systeminformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="a7d09-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="a7d09-119">Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a7d09-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="a7d09-120">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="a7d09-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7d09-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7d09-121">Remarks</span></span>

<span data-ttu-id="a7d09-122">Diese Methode kann verwendet werden, um viele Systeminformationswerte an fordern.</span><span class="sxs-lookup"><span data-stu-id="a7d09-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="a7d09-123">Die folgende Tabelle enthält den *sName-Wert,* der zum Anfordern der Informationen verwendet wird, und den zugeordneten Typ des zurückgegebenen Werts.</span><span class="sxs-lookup"><span data-stu-id="a7d09-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="a7d09-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="a7d09-124">*sName*</span></span>

<span data-ttu-id="a7d09-125">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="a7d09-125">Return type</span></span>

<span data-ttu-id="a7d09-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7d09-126">Description</span></span>

<span data-ttu-id="a7d09-127">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="a7d09-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="a7d09-128">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="a7d09-128">**Boolean**</span></span>

<span data-ttu-id="a7d09-129">Legen Sie auf **TRUE fest,** wenn der Verzeichnisdienst verfügbar ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a7d09-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="a7d09-130">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="a7d09-130">DoubleClickTime</span></span>

<span data-ttu-id="a7d09-131">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a7d09-131">**Integer**</span></span>

<span data-ttu-id="a7d09-132">Die Doppelklickzeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="a7d09-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="a7d09-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="a7d09-133">ProcessorLevel</span></span>

<span data-ttu-id="a7d09-134">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a7d09-134">**Integer**</span></span>

<span data-ttu-id="a7d09-135">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="a7d09-135">**Windows Vista and later**.</span></span> <span data-ttu-id="a7d09-136">Die Prozessorebene.</span><span class="sxs-lookup"><span data-stu-id="a7d09-136">The processor level.</span></span> <span data-ttu-id="a7d09-137">Gibt für Prozessoren auf x386-, x486- und Pentium-Ebene 3, 4 oder 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="a7d09-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="a7d09-138">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="a7d09-138">ProcessorSpeed</span></span>

<span data-ttu-id="a7d09-139">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a7d09-139">**Integer**</span></span>

<span data-ttu-id="a7d09-140">Die Prozessorgeschwindigkeit in Megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="a7d09-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="a7d09-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="a7d09-141">ProcessorArchitecture</span></span>

<span data-ttu-id="a7d09-142">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a7d09-142">**Integer**</span></span>

<span data-ttu-id="a7d09-143">Die Prozessorarchitektur.</span><span class="sxs-lookup"><span data-stu-id="a7d09-143">The processor architecture.</span></span> <span data-ttu-id="a7d09-144">Weitere Informationen finden Sie in der Erläuterung des **wProcessorArchitecture-Elements** der [**SYSTEM \_ INFO-Struktur.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)</span><span class="sxs-lookup"><span data-stu-id="a7d09-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="a7d09-145">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="a7d09-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="a7d09-146">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a7d09-146">**Integer**</span></span>

<span data-ttu-id="a7d09-147">Die Menge des installierten physischen Arbeitsspeichers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a7d09-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="a7d09-148">Die folgenden Sind nur unter Windows XP gültig.</span><span class="sxs-lookup"><span data-stu-id="a7d09-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="a7d09-149">IsOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="a7d09-149">IsOS\_Professional</span></span>

<span data-ttu-id="a7d09-150">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="a7d09-150">**Boolean**</span></span>

<span data-ttu-id="a7d09-151">Legen Sie diese Einstellung auf **TRUE** fest, wenn das Betriebssystem Windows XP Professional Edition ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a7d09-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="a7d09-152">IsOS \_ Personal</span><span class="sxs-lookup"><span data-stu-id="a7d09-152">IsOS\_Personal</span></span>

<span data-ttu-id="a7d09-153">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="a7d09-153">**Boolean**</span></span>

<span data-ttu-id="a7d09-154">Legen Sie diese Einstellung auf **TRUE** fest, wenn das Betriebssystem Windows XP Home Edition ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a7d09-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="a7d09-155">Folgendes ist nur unter Windows XP und höher gültig.</span><span class="sxs-lookup"><span data-stu-id="a7d09-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="a7d09-156">IsOS \_ DomainMember</span><span class="sxs-lookup"><span data-stu-id="a7d09-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="a7d09-157">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="a7d09-157">**Boolean**</span></span>

<span data-ttu-id="a7d09-158">Wird auf **TRUE** festgelegt, wenn der Computer Mitglied einer Domäne ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a7d09-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="a7d09-159">Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7d09-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="a7d09-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7d09-160">Examples</span></span>

<span data-ttu-id="a7d09-161">Die folgenden Beispiele zeigen die Verwendung von **GetSystemInformation** für JScript und VBScript.</span><span class="sxs-lookup"><span data-stu-id="a7d09-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="a7d09-162">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a7d09-162">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



<span data-ttu-id="a7d09-163">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="a7d09-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="a7d09-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7d09-164">Requirements</span></span>



| <span data-ttu-id="a7d09-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7d09-165">Requirement</span></span> | <span data-ttu-id="a7d09-166">Wert</span><span class="sxs-lookup"><span data-stu-id="a7d09-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d09-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7d09-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d09-168">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7d09-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7d09-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7d09-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d09-170">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7d09-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a7d09-171">Header</span><span class="sxs-lookup"><span data-stu-id="a7d09-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7d09-172"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a7d09-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a7d09-173">Idl</span><span class="sxs-lookup"><span data-stu-id="a7d09-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7d09-174"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7d09-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a7d09-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a7d09-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7d09-176"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d09-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
