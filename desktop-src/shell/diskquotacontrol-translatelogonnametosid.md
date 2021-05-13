---
description: Übersetzt einen Anmeldenamen in die entsprechende Benutzersicherheits-ID im Zeichenfolgenformat.
title: DiskQuotaControl.TranslateLogonNameToSID-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: 5f0a2591b0f5df6bc0f50994fcbf101b7bfbb36d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841561"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="3e34f-103">DiskQuotaControl.TranslateLogonNameToSID-Methode</span><span class="sxs-lookup"><span data-stu-id="3e34f-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="3e34f-104">Übersetzt einen Anmeldenamen in die entsprechende Benutzersicherheits-ID im Zeichenfolgenformat.</span><span class="sxs-lookup"><span data-stu-id="3e34f-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e34f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e34f-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="3e34f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e34f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e34f-107">*Anmeldename*</span><span class="sxs-lookup"><span data-stu-id="3e34f-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="3e34f-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e34f-108">Type: **String**</span></span>

<span data-ttu-id="3e34f-109">Ein Zeichenfolgenwert, der den Anmeldenamen des Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="3e34f-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e34f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e34f-110">Return value</span></span>

<span data-ttu-id="3e34f-111">Gibt die Benutzersicherheits-ID (SID) im Zeichenfolgenformat zurück, das dem angegebenen Anmeldenamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3e34f-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="3e34f-112">Die zurückgegebene Zeichenfolge enthält die standardmäßigen umschließenden geschweiften Klammern.</span><span class="sxs-lookup"><span data-stu-id="3e34f-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="3e34f-113">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3e34f-113">For example:</span></span>

<span data-ttu-id="3e34f-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span><span class="sxs-lookup"><span data-stu-id="3e34f-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="3e34f-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e34f-115">Remarks</span></span>

<span data-ttu-id="3e34f-116">Die zurückgegebene SID-Zeichenfolge kann statt eines Anmeldenamens an die [**FindUser-Methode**](diskquotacontrol-finduser.md) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e34f-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="3e34f-117">Wenn bei einem Aufruf der [**FindUser-Methode**](diskquotacontrol-finduser.md) *(logonname)* ein Fehler auftritt, kann dies auf einen Konflikt zwischen dem Formular (z. B. SAM-kompatibel mit dem Sicherheitskonto-Manager und dem \[ \] \[ Benutzerprinzipalnamen-UPN) des bereitgestellten Anmeldenamens und dem im SID-Namenscache gespeicherten Formular \] liegen.</span><span class="sxs-lookup"><span data-stu-id="3e34f-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="3e34f-118">In solchen Fällen kann der Anmeldename in eine SID konvertiert und der Aufruf von **FindUser wiederholt** werden.</span><span class="sxs-lookup"><span data-stu-id="3e34f-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="3e34f-119">**FindUser** erkennt eine SID-Zeichenfolge und umgeht die Cachesuche nach SID-Namen.</span><span class="sxs-lookup"><span data-stu-id="3e34f-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="3e34f-120">Der folgende Code Visual Basic Scripting Edition (VBScript) von Microsoft veranschaulicht diese Technik.</span><span class="sxs-lookup"><span data-stu-id="3e34f-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



<span data-ttu-id="3e34f-121">Die Namens-zu-SID-Übersetzung kann im Vergleich zu Suchen im SID-Namenscache ein langsamer Prozess sein.</span><span class="sxs-lookup"><span data-stu-id="3e34f-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="3e34f-122">Daher empfiehlt es sich, [**FindUser**](diskquotacontrol-finduser.md) zuerst mit einem Anmeldenamen auf zu nennen.</span><span class="sxs-lookup"><span data-stu-id="3e34f-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="3e34f-123">Im obigen Beispiel wird diese Technik verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e34f-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e34f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e34f-124">Requirements</span></span>



| <span data-ttu-id="3e34f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e34f-125">Requirement</span></span> | <span data-ttu-id="3e34f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3e34f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e34f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e34f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3e34f-128">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e34f-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e34f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e34f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3e34f-130">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e34f-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3e34f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3e34f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e34f-132"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3e34f-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e34f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e34f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e34f-134">**DiskQuotaControl-Objekt**</span><span class="sxs-lookup"><span data-stu-id="3e34f-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




