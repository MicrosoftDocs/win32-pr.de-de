---
description: Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Shell. IsRestricted-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2224a3ea4ea26cf39f2e15486de4f96afe5448d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216603"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="041a4-103">Shell. IsRestricted-Methode</span><span class="sxs-lookup"><span data-stu-id="041a4-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="041a4-104">Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="041a4-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="041a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="041a4-105">Syntax</span></span>


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="041a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="041a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="041a4-107">*sgroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="041a4-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="041a4-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="041a4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="041a4-109">Eine **Zeichenfolge** , die den Gruppennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="041a4-109">A **String** that contains the group name.</span></span> <span data-ttu-id="041a4-110">Dieser Wert ist der Name eines Registrierungs unter Schlüssels, unter dem die Einschränkung überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="041a4-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="041a4-111">*seinschränkung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="041a4-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="041a4-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="041a4-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="041a4-113">Eine **Zeichenfolge** , die die Einschränkung enthält, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="041a4-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="041a4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="041a4-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="041a4-115">JScript</span><span class="sxs-lookup"><span data-stu-id="041a4-115">JScript</span></span>

<span data-ttu-id="041a4-116">Typ: \**Integer \** _</span><span class="sxs-lookup"><span data-stu-id="041a4-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="041a4-117">Der Wert der Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="041a4-117">The value of the restriction.</span></span> <span data-ttu-id="041a4-118">Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="041a4-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="041a4-119">VB</span><span class="sxs-lookup"><span data-stu-id="041a4-119">VB</span></span>

<span data-ttu-id="041a4-120">Type: _*Integer \**_</span><span class="sxs-lookup"><span data-stu-id="041a4-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="041a4-121">Der Wert der Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="041a4-121">The value of the restriction.</span></span> <span data-ttu-id="041a4-122">Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="041a4-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="041a4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="041a4-123">Remarks</span></span>

<span data-ttu-id="041a4-124">_ *IsRestricted*\* sucht zuerst nach einem Unterschlüssel Namen, der mit *sgroup* unter dem folgenden Schlüssel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="041a4-124">_ *IsRestricted*\* first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="041a4-125">Einschränkungen werden als Werte der einzelnen Richtlinien Unterschlüssel deklariert.</span><span class="sxs-lookup"><span data-stu-id="041a4-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="041a4-126">Wenn die in *seinschränkung* benannte Einschränkung in dem Unterschlüssel mit dem Namen in *sgroup* gefunden wird, gibt **IsRestricted** den aktuellen Wert der Einschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="041a4-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="041a4-127">Wenn die Einschränkung unter **HKEY \_ local \_ Machine** nicht gefunden wird, wird unter **HKEY \_ Current \_ User** der gleiche Unterschlüssel geprüft.</span><span class="sxs-lookup"><span data-stu-id="041a4-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="041a4-128">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="041a4-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="041a4-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="041a4-129">Examples</span></span>

<span data-ttu-id="041a4-130">In den folgenden Beispielen wird die Verwendung von **IsRestricted** zum Abrufen des Daten Werts der **undockwithoutlogon** -Einschränkung aus dem **System** Unterschlüssel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="041a4-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="041a4-131">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="041a4-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="041a4-132">JScript</span><span class="sxs-lookup"><span data-stu-id="041a4-132">JScript:</span></span>


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



<span data-ttu-id="041a4-133">VBScript</span><span class="sxs-lookup"><span data-stu-id="041a4-133">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="041a4-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="041a4-134">Requirements</span></span>



| <span data-ttu-id="041a4-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="041a4-135">Requirement</span></span> | <span data-ttu-id="041a4-136">Wert</span><span class="sxs-lookup"><span data-stu-id="041a4-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041a4-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="041a4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="041a4-138">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="041a4-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="041a4-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="041a4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="041a4-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="041a4-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="041a4-141">Header</span><span class="sxs-lookup"><span data-stu-id="041a4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="041a4-142"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="041a4-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="041a4-143">IDL</span><span class="sxs-lookup"><span data-stu-id="041a4-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="041a4-144"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="041a4-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="041a4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="041a4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="041a4-146"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="041a4-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
