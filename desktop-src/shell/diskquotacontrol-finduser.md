---
description: Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingentdatei des Volumes.
title: DiskQuotaControl.FindUser-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: eab539a5ec5a360ae28fc87d5ffbb9dd4f9f1cc8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841521"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="1f17a-103">DiskQuotaControl.FindUser-Methode</span><span class="sxs-lookup"><span data-stu-id="1f17a-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="1f17a-104">Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingentdatei des Volumes.</span><span class="sxs-lookup"><span data-stu-id="1f17a-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f17a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f17a-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="1f17a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f17a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f17a-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="1f17a-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="1f17a-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f17a-108">Type: **String**</span></span>

<span data-ttu-id="1f17a-109">Ein Zeichenfolgenwert, der den Anmeldenamen des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="1f17a-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f17a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f17a-110">Return value</span></span>

<span data-ttu-id="1f17a-111">Gibt einen Objektausdruck zurück, der das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) des Benutzers ergibt.</span><span class="sxs-lookup"><span data-stu-id="1f17a-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f17a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f17a-112">Remarks</span></span>

<span data-ttu-id="1f17a-113">Diese Methode gibt ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) zurück, auch wenn kein Eintrag für den Benutzer in der Kontingentdatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1f17a-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="1f17a-114">Für das zurückgegebene Benutzerobjekt sind warnungsschwellenwert und harte Kontingentgrenzen auf die Standardwerte des Volumes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f17a-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="1f17a-115">Die von [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) zurückgegebene Zeichenfolge kann anstelle des *sLogonName-Parameters* übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1f17a-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="1f17a-116">Wenn **FindUser** eine SID-Zeichenfolge empfängt, verwendet er die entsprechende SID für die direkte Suche des Kontingentdatensatzes des Benutzers auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="1f17a-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="1f17a-117">Dadurch wird der SID-Name-Cache umgangen.</span><span class="sxs-lookup"><span data-stu-id="1f17a-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="1f17a-118">In Fällen, in denen **FindUser** aufgrund eines Konflikts im Format (z. B. SAM-kompatibel und UPN) des angegebenen Anmeldenamens und des zwischengespeicherten Anmeldenamens fehlschlägt, kann der Anmeldename mit **TranslateLogonNameToSID** in eine SID-Zeichenfolge übersetzt und dann erneut an **FindUser** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1f17a-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="1f17a-119">Dies wird im folgenden VBScript-Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1f17a-119">The following VBScript code illustrates this technique.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1f17a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f17a-120">Requirements</span></span>



| <span data-ttu-id="1f17a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f17a-121">Requirement</span></span> | <span data-ttu-id="1f17a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1f17a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f17a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f17a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1f17a-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f17a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f17a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f17a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1f17a-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f17a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1f17a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1f17a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f17a-128"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1f17a-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f17a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f17a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f17a-130">**DiskQuotaControl-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1f17a-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




