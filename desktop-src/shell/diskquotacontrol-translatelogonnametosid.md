---
description: Übersetzt einen Anmelde Namen in die entsprechende Benutzersicherheits-ID im Zeichen folgen Format.
title: Diskquotacontrol. translatelogonnametosid-Methode
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
ms.openlocfilehash: ec5e6c0bbd013c8fbd3f6616671ee006109566d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042571"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="1b68f-103">Diskquotacontrol. translatelogonnametosid-Methode</span><span class="sxs-lookup"><span data-stu-id="1b68f-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="1b68f-104">Übersetzt einen Anmelde Namen in die entsprechende Benutzersicherheits-ID im Zeichen folgen Format.</span><span class="sxs-lookup"><span data-stu-id="1b68f-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b68f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b68f-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="1b68f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b68f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b68f-107">*Anmelde Name*</span><span class="sxs-lookup"><span data-stu-id="1b68f-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="1b68f-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1b68f-108">Type: **String**</span></span>

<span data-ttu-id="1b68f-109">Ein Zeichen folgen Wert, der den Anmelde Namen des Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="1b68f-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b68f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b68f-110">Return value</span></span>

<span data-ttu-id="1b68f-111">Gibt die Benutzer Sicherheits-ID (SID) im Zeichen folgen Format zurück, das dem angegebenen Anmelde Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="1b68f-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="1b68f-112">Die zurückgegebene Zeichenfolge enthält die standardmäßigen schließenden geschweiften Klammern.</span><span class="sxs-lookup"><span data-stu-id="1b68f-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="1b68f-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1b68f-113">For example:</span></span>

<span data-ttu-id="1b68f-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span><span class="sxs-lookup"><span data-stu-id="1b68f-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="1b68f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b68f-115">Remarks</span></span>

<span data-ttu-id="1b68f-116">Die zurückgegebene SID-Zeichenfolge kann anstelle eines Anmelde namens an die [**FINDUSER**](diskquotacontrol-finduser.md) -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1b68f-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="1b68f-117">Wenn beim Aufrufen der Methode [**FINDUSER**](diskquotacontrol-finduser.md)( *Logonname*) ein Fehler auftritt, kann dies auf einen Konflikt zwischen dem Formular (z. b. dem Sicherheits Konto \[ -Manager SAM \] -kompatibel und dem Benutzer Prinzipal Namen- \[ UPN \] ) des angegebenen Anmelde namens und der im sid-Name-Cache gespeicherten Form zurückzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="1b68f-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="1b68f-118">In solchen Fällen kann der Anmelde Name in eine SID konvertiert werden, und der **FINDUSER** -Befehl wird wiederholt.</span><span class="sxs-lookup"><span data-stu-id="1b68f-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="1b68f-119">**FINDUSER** erkennt eine SID-Zeichenfolge und umgeht die Cache Suche mit dem SID-Namen.</span><span class="sxs-lookup"><span data-stu-id="1b68f-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="1b68f-120">Der folgende Microsoft Visual Basic Scripting Edition-Code (VBScript) veranschaulicht diese Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="1b68f-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


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



<span data-ttu-id="1b68f-121">Die Namens-zu-sid-Übersetzung kann im Vergleich zu Such Vorgängen im Cache für sid-Namen ein langsamer Prozess sein.</span><span class="sxs-lookup"><span data-stu-id="1b68f-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="1b68f-122">Daher wird empfohlen, dass [**FINDUSER**](diskquotacontrol-finduser.md) zuerst mit einem Anmelde Namen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1b68f-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="1b68f-123">Im obigen Beispiel wird diese Technik verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b68f-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b68f-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1b68f-124">Requirements</span></span>



| <span data-ttu-id="1b68f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b68f-125">Requirement</span></span> | <span data-ttu-id="1b68f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1b68f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b68f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b68f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1b68f-128">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b68f-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b68f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b68f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1b68f-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b68f-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1b68f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1b68f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b68f-132"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1b68f-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b68f-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1b68f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b68f-134">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1b68f-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




