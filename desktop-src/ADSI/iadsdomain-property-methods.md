---
title: Iadsdomain-Eigenschaften Methoden (IADs. h)
description: Die iadsdomain-Schnittstellen Methoden lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- Iadsdomain-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a10c6377c7e97f83046f60d46312a03db68cadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956912"
---
# <a name="iadsdomain-property-methods"></a><span data-ttu-id="34982-105">Iadsdomain-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="34982-105">IADsDomain Property Methods</span></span>

<span data-ttu-id="34982-106">Die [**iadsdomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) -Schnittstellen Methoden lesen und schreiben die in diesem Thema beschriebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34982-106">The [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="34982-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="34982-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="34982-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34982-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="34982-109">**Autounlockinterval**</span><span class="sxs-lookup"><span data-stu-id="34982-109">**AutoUnlockInterval**</span></span>
<span data-ttu-id="34982-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-111">Gibt die minimale Zeitspanne an, die ververgehen muss, bevor das Konto automatisch erneut aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="34982-111">Indicates the minimum time that must elapse before the account is automatically reenabled.</span></span>

<dt>

<span data-ttu-id="34982-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34982-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34982-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="34982-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="34982-114">**Isworkgroup**</span><span class="sxs-lookup"><span data-stu-id="34982-114">**IsWorkgroup**</span></span>
<span data-ttu-id="34982-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-116">Diese Eigenschaft ist nicht mehr implementiert.</span><span class="sxs-lookup"><span data-stu-id="34982-116">This property is no longer implemented.</span></span>

<dt>

<span data-ttu-id="34982-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34982-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34982-118">Skript Datentyp: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="34982-118">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="34982-119">**Lockoutobservationinterval**</span><span class="sxs-lookup"><span data-stu-id="34982-119">**LockoutObservationInterval**</span></span>
<span data-ttu-id="34982-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-121">Gibt das Zeitfenster an, in dem die Anzahl fehlerhafter Kenn Wörter überwacht und akkumuliert wird, bevor festgestellt wird, ob das Konto gesperrt werden muss. Wenn beispielsweise die Anzahl fehlerhafter Kenn Wort Versuche eines Kontos den Schwellenwert (maximale Anzahl ungültiger Kenn Wörter) während des angegebenen Zeitraums (Sperr beobachtungsintervall) überschreitet, wird das Konto gesperrt, indem die entsprechende Eigenschaft im Eigenschaften Satz des Anmelde Parameters festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="34982-121">Indicates the time window during which the bad password count is monitored and accumulated before determining whether the account needs to be locked out. For example, if the number of bad password attempts on an account exceed the threshold (Maximum Bad Passwords Allowed) during the specified time period (Lockout Observation Interval) the account will be locked out by setting the appropriate property in the Login Parameter property set.</span></span>

<dt>

<span data-ttu-id="34982-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34982-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34982-123">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="34982-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="34982-124">**Maxbadpasswordsallowed**</span><span class="sxs-lookup"><span data-stu-id="34982-124">**MaxBadPasswordsAllowed**</span></span>
<span data-ttu-id="34982-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-126">Gibt die maximale Anzahl von Anmeldungen für ungültige Kenn Wörter an, die vor einer Kontosperrung zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="34982-126">Indicates the maximum number of bad password logins allowed before an account lockout.</span></span>

<dt>

<span data-ttu-id="34982-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34982-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34982-128">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="34982-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="34982-129">**Maxpasswordage**</span><span class="sxs-lookup"><span data-stu-id="34982-129">**MaxPasswordAge**</span></span>
<span data-ttu-id="34982-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-131">Gibt das maximale Zeitintervall in Sekunden an, nach dem das Kennwort vom Benutzer geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="34982-131">Indicates the maximum time interval, in seconds, after which the password must be changed by the user.</span></span>

<dt>

<span data-ttu-id="34982-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34982-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34982-133">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="34982-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="34982-134">**Minpasswordage**</span><span class="sxs-lookup"><span data-stu-id="34982-134">**MinPasswordAge**</span></span>
<span data-ttu-id="34982-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-136">Gibt das minimale Zeitintervall in Sekunden an, bevor das Kennwort geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="34982-136">Indicates the minimum time interval, in seconds, before the password can be changed.</span></span>

<dt>

<span data-ttu-id="34982-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34982-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34982-138">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="34982-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="34982-139">**Minpasswordlength**</span><span class="sxs-lookup"><span data-stu-id="34982-139">**MinPasswordLength**</span></span>
<span data-ttu-id="34982-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-141">Gibt die Mindestanzahl von Zeichen an, die für ein Kennwort verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="34982-141">Indicates the minimum number of characters that must be used for a password.</span></span>

<dt>

<span data-ttu-id="34982-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34982-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34982-143">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="34982-143">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="34982-144">**Passwordattributes**</span><span class="sxs-lookup"><span data-stu-id="34982-144">**PasswordAttributes**</span></span>
<span data-ttu-id="34982-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-146">Gibt Einschränkungen für Kenn Wörter an, wie in der folgenden Liste von Attributen und Werten definiert.</span><span class="sxs-lookup"><span data-stu-id="34982-146">Indicates restrictions on passwords, as defined by the following list of attributes and values.</span></span>

> [!Note]  
> <span data-ttu-id="34982-147">Bei einem \_ komplexen Kennwort \_ muss das Kennwort mindestens ein Satzzeichen oder ein nicht druckbares Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="34982-147">For PASSWORD\_ATTR\_COMPLEX, the password must include at least one punctuation mark or non-printable character.</span></span>

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

<span data-ttu-id="34982-148">**Kennwort \_ Attr \_ None** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="34982-148">**PASSWORD\_ATTR\_NONE** (0x00000000)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

<span data-ttu-id="34982-149">**Kennwort \_ "Attr \_ mixed \_ Case** " (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="34982-149">**PASSWORD\_ATTR\_MIXED\_CASE** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

<span data-ttu-id="34982-150">**Kennwort \_ Attr \_ Komplex** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="34982-150">**PASSWORD\_ATTR\_COMPLEX** (0x00000002)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="34982-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34982-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34982-152">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="34982-152">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="34982-153">**PasswordHistoryLength**</span><span class="sxs-lookup"><span data-stu-id="34982-153">**PasswordHistoryLength**</span></span>
<span data-ttu-id="34982-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="34982-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="34982-155">Gibt die Anzahl der vorherigen Kenn Wörter an, die in der Liste Verlauf gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="34982-155">Indicates the number of previous passwords saved in the history list.</span></span> <span data-ttu-id="34982-156">Der Benutzer kann ein Kennwort in der Verlaufs Liste nicht wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="34982-156">The user cannot reuse a password in the history list.</span></span>

<dt>

<span data-ttu-id="34982-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34982-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34982-158">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="34982-158">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="34982-159">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34982-159">Examples</span></span>

<span data-ttu-id="34982-160">Im folgenden Codebeispiel wird der Wert der **PasswordHistoryLength** -Eigenschaft angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34982-160">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



<span data-ttu-id="34982-161">Im folgenden Codebeispiel wird der Wert der **PasswordHistoryLength** -Eigenschaft angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34982-161">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a><span data-ttu-id="34982-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34982-162">Requirements</span></span>



| <span data-ttu-id="34982-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34982-163">Requirement</span></span> | <span data-ttu-id="34982-164">Wert</span><span class="sxs-lookup"><span data-stu-id="34982-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34982-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34982-165">Minimum supported client</span></span><br/> | <span data-ttu-id="34982-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34982-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34982-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34982-167">Minimum supported server</span></span><br/> | <span data-ttu-id="34982-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34982-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34982-169">Header</span><span class="sxs-lookup"><span data-stu-id="34982-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="34982-170"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="34982-170"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="34982-171">DLL</span><span class="sxs-lookup"><span data-stu-id="34982-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34982-172"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34982-172"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="34982-173">IID</span><span class="sxs-lookup"><span data-stu-id="34982-173">IID</span></span><br/>                      | <span data-ttu-id="34982-174">IID \_ iadsdomain ist als 00e4c220-SD16-11CE-abc4-02608c9e7553 definiert.</span><span class="sxs-lookup"><span data-stu-id="34982-174">IID\_IADsDomain is defined as 00E4C220-FD16-11CE-ABC4-02608C9E7553</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="34982-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34982-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34982-176">**Iadsdomain**</span><span class="sxs-lookup"><span data-stu-id="34982-176">**IADsDomain**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[<span data-ttu-id="34982-177">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="34982-177">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





