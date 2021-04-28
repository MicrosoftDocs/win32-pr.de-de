---
description: 'Shell.IsRestricted-Methode: Ruft die Einschränkungseinstellung einer Gruppe aus der Registrierung ab.'
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Shell.IsRestricted-Methode (Shldisp.h)
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
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104258"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="9fdc5-103">Shell.IsRestricted-Methode</span><span class="sxs-lookup"><span data-stu-id="9fdc5-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="9fdc5-104">Ruft die Einschränkungseinstellung einer Gruppe aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fdc5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fdc5-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="9fdc5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fdc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fdc5-107">*sGroup* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9fdc5-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fdc5-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9fdc5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9fdc5-109">Eine **Zeichenfolge,** die den Gruppennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-109">A **String** that contains the group name.</span></span> <span data-ttu-id="9fdc5-110">Dieser Wert ist der Name eines Registrierungsunterschlüssels, unter dem die Einschränkung überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="9fdc5-111">*sRestriction* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9fdc5-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fdc5-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9fdc5-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9fdc5-113">Eine **Zeichenfolge,** die die Einschränkung enthält, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fdc5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fdc5-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9fdc5-115">JScript</span><span class="sxs-lookup"><span data-stu-id="9fdc5-115">JScript</span></span>

<span data-ttu-id="9fdc5-116">Typ: **\* Integer**</span><span class="sxs-lookup"><span data-stu-id="9fdc5-116">Type: **Integer\***</span></span>

<span data-ttu-id="9fdc5-117">Der Wert der Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-117">The value of the restriction.</span></span> <span data-ttu-id="9fdc5-118">Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="9fdc5-119">VB</span><span class="sxs-lookup"><span data-stu-id="9fdc5-119">VB</span></span>

<span data-ttu-id="9fdc5-120">Typ: **\* Integer**</span><span class="sxs-lookup"><span data-stu-id="9fdc5-120">Type: **Integer\***</span></span>

<span data-ttu-id="9fdc5-121">Der Wert der Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-121">The value of the restriction.</span></span> <span data-ttu-id="9fdc5-122">Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fdc5-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fdc5-123">Remarks</span></span>

<span data-ttu-id="9fdc5-124">**IsRestricted** sucht zunächst unter dem folgenden Schlüssel nach einem Unterschlüsselnamen, der *sGroup* entspricht.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-124">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="9fdc5-125">Einschränkungen werden als Werte der einzelnen Richtlinienunterschlüssel deklariert.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="9fdc5-126">Wenn die in *sRestriction* benannte Einschränkung im Unterschlüssel mit dem Namen in *sGroup* gefunden wird, gibt **IsRestricted** den aktuellen Wert der Einschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="9fdc5-127">Wenn die Einschränkung unter **HKEY \_ LOCAL \_ MACHINE** nicht gefunden wird, wird derselbe Unterschlüssel unter **HKEY CURRENT USER \_ \_ überprüft.**</span><span class="sxs-lookup"><span data-stu-id="9fdc5-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="9fdc5-128">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="9fdc5-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fdc5-129">Examples</span></span>

<span data-ttu-id="9fdc5-130">Die folgenden Beispiele zeigen die Verwendung von **IsRestricted,** um den Datenwert der Einschränkung **"undockwithoutlogon"** aus dem **Unterschlüssel System** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="9fdc5-131">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="9fdc5-132">Jscript:</span><span class="sxs-lookup"><span data-stu-id="9fdc5-132">JScript:</span></span>


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



<span data-ttu-id="9fdc5-133">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="9fdc5-133">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9fdc5-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fdc5-134">Requirements</span></span>



| <span data-ttu-id="9fdc5-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fdc5-135">Requirement</span></span> | <span data-ttu-id="9fdc5-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9fdc5-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdc5-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fdc5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9fdc5-138">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fdc5-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fdc5-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fdc5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9fdc5-140">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fdc5-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9fdc5-141">Header</span><span class="sxs-lookup"><span data-stu-id="9fdc5-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fdc5-142"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="9fdc5-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9fdc5-143">Idl</span><span class="sxs-lookup"><span data-stu-id="9fdc5-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9fdc5-144"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="9fdc5-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9fdc5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9fdc5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fdc5-146"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="9fdc5-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
