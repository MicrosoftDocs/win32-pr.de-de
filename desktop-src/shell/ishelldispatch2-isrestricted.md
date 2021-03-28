---
description: Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: IShellDispatch2. IsRestricted-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978065"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="01f1f-103">IShellDispatch2. IsRestricted-Methode</span><span class="sxs-lookup"><span data-stu-id="01f1f-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="01f1f-104">Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="01f1f-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f1f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01f1f-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="01f1f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01f1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f1f-107">*sgroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01f1f-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f1f-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="01f1f-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="01f1f-109">Eine **Zeichenfolge** , die den Gruppennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="01f1f-109">A **String** that contains the group name.</span></span> <span data-ttu-id="01f1f-110">Dieser Wert ist der Name eines Registrierungs unter Schlüssels, unter dem die Einschränkung überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="01f1f-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="01f1f-111">*seinschränkung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01f1f-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f1f-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="01f1f-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="01f1f-113">Eine **Zeichenfolge** , die die Einschränkung enthält, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="01f1f-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f1f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01f1f-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="01f1f-115">JScript</span><span class="sxs-lookup"><span data-stu-id="01f1f-115">JScript</span></span>

<span data-ttu-id="01f1f-116">Typ: \**Integer \** _</span><span class="sxs-lookup"><span data-stu-id="01f1f-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="01f1f-117">Der Wert der Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="01f1f-117">The value of the restriction.</span></span> <span data-ttu-id="01f1f-118">Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="01f1f-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="01f1f-119">VB</span><span class="sxs-lookup"><span data-stu-id="01f1f-119">VB</span></span>

<span data-ttu-id="01f1f-120">Type: _*Integer \**_</span><span class="sxs-lookup"><span data-stu-id="01f1f-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="01f1f-121">Der Wert der Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="01f1f-121">The value of the restriction.</span></span> <span data-ttu-id="01f1f-122">Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="01f1f-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="01f1f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01f1f-123">Remarks</span></span>

<span data-ttu-id="01f1f-124">Diese Methode wird implementiert und über die [_ *Shell. IsRestricted* \*](./shell-isrestricted.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="01f1f-124">This method is implemented and accessed through the [_ *Shell.IsRestricted*\*](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="01f1f-125">**IsRestricted** sucht zuerst nach einem Unterschlüssel Namen, der mit *sgroup* unter dem folgenden Schlüssel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="01f1f-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="01f1f-126">Einschränkungen werden als Werte der einzelnen Richtlinien Unterschlüssel deklariert.</span><span class="sxs-lookup"><span data-stu-id="01f1f-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="01f1f-127">Wenn die in *seinschränkung* benannte Einschränkung in dem Unterschlüssel mit dem Namen in *sgroup* gefunden wird, gibt **IsRestricted** den aktuellen Wert der Einschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="01f1f-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="01f1f-128">Wenn die Einschränkung unter **HKEY \_ local \_ Machine** nicht gefunden wird, wird unter **HKEY \_ Current \_ User** der gleiche Unterschlüssel geprüft.</span><span class="sxs-lookup"><span data-stu-id="01f1f-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="01f1f-129">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="01f1f-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="01f1f-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01f1f-130">Examples</span></span>

<span data-ttu-id="01f1f-131">In den folgenden Beispielen wird die Verwendung von **IsRestricted** zum Abrufen des Daten Werts der **undockwithoutlogon** -Einschränkung aus dem **System** Unterschlüssel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="01f1f-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="01f1f-132">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="01f1f-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="01f1f-133">JScript</span><span class="sxs-lookup"><span data-stu-id="01f1f-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



<span data-ttu-id="01f1f-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="01f1f-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="01f1f-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="01f1f-135">Requirements</span></span>



| <span data-ttu-id="01f1f-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01f1f-136">Requirement</span></span> | <span data-ttu-id="01f1f-137">Wert</span><span class="sxs-lookup"><span data-stu-id="01f1f-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f1f-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01f1f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="01f1f-139">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01f1f-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01f1f-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01f1f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="01f1f-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01f1f-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="01f1f-142">Header</span><span class="sxs-lookup"><span data-stu-id="01f1f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="01f1f-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01f1f-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="01f1f-144">IDL</span><span class="sxs-lookup"><span data-stu-id="01f1f-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01f1f-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01f1f-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="01f1f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="01f1f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f1f-147"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="01f1f-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
