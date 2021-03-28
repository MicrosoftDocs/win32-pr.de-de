---
description: Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingent Datei des Volumes.
title: Diskquotacontrol. FINDUSER-Methode
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
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977185"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="7786d-103">Diskquotacontrol. FINDUSER-Methode</span><span class="sxs-lookup"><span data-stu-id="7786d-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="7786d-104">Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingent Datei des Volumes.</span><span class="sxs-lookup"><span data-stu-id="7786d-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7786d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7786d-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="7786d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7786d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7786d-107">*slogonname*</span><span class="sxs-lookup"><span data-stu-id="7786d-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="7786d-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7786d-108">Type: **String**</span></span>

<span data-ttu-id="7786d-109">Ein Zeichen folgen Wert, der den Anmelde Namen des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="7786d-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7786d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7786d-110">Return value</span></span>

<span data-ttu-id="7786d-111">Gibt einen Objekt Ausdruck zurück, der das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers ergibt.</span><span class="sxs-lookup"><span data-stu-id="7786d-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7786d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7786d-112">Remarks</span></span>

<span data-ttu-id="7786d-113">Diese Methode gibt ein [**didiskquotauser**](didiskquotauser-object.md) -Objekt zurück, auch wenn in der Kontingent Datei kein Eintrag für den Benutzer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7786d-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="7786d-114">Für das zurückgegebene Benutzerobjekt sind Warnungs Schwellenwert und feste Kontingent Limits auf die Standardwerte des Volumes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7786d-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="7786d-115">Die von [**translatelogonnametosid**](diskquotacontrol-translatelogonnametosid.md) zurückgegebene Zeichenfolge kann anstelle des *slogonname* -Parameters übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7786d-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="7786d-116">Wenn **FINDUSER** eine SID-Zeichenfolge empfängt, wird die entsprechende sid für die direkte Suche des Kontingent Datensatzes des Benutzers auf dem Volume verwendet.</span><span class="sxs-lookup"><span data-stu-id="7786d-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="7786d-117">Dadurch wird der SID-Name-Cache umgangen.</span><span class="sxs-lookup"><span data-stu-id="7786d-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="7786d-118">In Fällen, in denen **FINDUSER** aufgrund eines Konflikts im Format (z. b. Sam-kompatibel und UPN) des bereitgestellten Anmelde namens und des zwischengespeicherten Anmelde namens ausfällt, kann der Anmelde Name mithilfe von **translatelogonnametosid** in eine SID-Zeichenfolge übersetzt werden und dann erneut an **FINDUSER** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7786d-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="7786d-119">Dieses Verfahren wird im folgenden VBScript-Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7786d-119">The following VBScript code illustrates this technique.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7786d-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7786d-120">Requirements</span></span>



| <span data-ttu-id="7786d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7786d-121">Requirement</span></span> | <span data-ttu-id="7786d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7786d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7786d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7786d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7786d-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7786d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7786d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7786d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7786d-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7786d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7786d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7786d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7786d-128"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7786d-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7786d-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7786d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7786d-130">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7786d-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




