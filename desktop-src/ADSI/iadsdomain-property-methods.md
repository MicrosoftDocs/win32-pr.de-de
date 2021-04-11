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
# <a name="iadsdomain-property-methods"></a>Iadsdomain-Eigenschaften Methoden

Die [**iadsdomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) -Schnittstellen Methoden lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Autounlockinterval**
</dt> <dd> <dl>

Gibt die minimale Zeitspanne an, die ververgehen muss, bevor das Konto automatisch erneut aktiviert wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Isworkgroup**
</dt> <dd> <dl>

Diese Eigenschaft ist nicht mehr implementiert.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

**Lockoutobservationinterval**
</dt> <dd> <dl>

Gibt das Zeitfenster an, in dem die Anzahl fehlerhafter Kenn Wörter überwacht und akkumuliert wird, bevor festgestellt wird, ob das Konto gesperrt werden muss. Wenn beispielsweise die Anzahl fehlerhafter Kenn Wort Versuche eines Kontos den Schwellenwert (maximale Anzahl ungültiger Kenn Wörter) während des angegebenen Zeitraums (Sperr beobachtungsintervall) überschreitet, wird das Konto gesperrt, indem die entsprechende Eigenschaft im Eigenschaften Satz des Anmelde Parameters festgelegt wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Maxbadpasswordsallowed**
</dt> <dd> <dl>

Gibt die maximale Anzahl von Anmeldungen für ungültige Kenn Wörter an, die vor einer Kontosperrung zulässig sind.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Maxpasswordage**
</dt> <dd> <dl>

Gibt das maximale Zeitintervall in Sekunden an, nach dem das Kennwort vom Benutzer geändert werden muss.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Minpasswordage**
</dt> <dd> <dl>

Gibt das minimale Zeitintervall in Sekunden an, bevor das Kennwort geändert werden kann.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Minpasswordlength**
</dt> <dd> <dl>

Gibt die Mindestanzahl von Zeichen an, die für ein Kennwort verwendet werden muss.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Passwordattributes**
</dt> <dd> <dl>

Gibt Einschränkungen für Kenn Wörter an, wie in der folgenden Liste von Attributen und Werten definiert.

> [!Note]  
> Bei einem \_ komplexen Kennwort \_ muss das Kennwort mindestens ein Satzzeichen oder ein nicht druckbares Zeichen enthalten.

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

**Kennwort \_ Attr \_ None** (0x00000000)


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

**Kennwort \_ "Attr \_ mixed \_ Case** " (0x00000001)


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

**Kennwort \_ Attr \_ Komplex** (0x00000002)


</dt> <dd></dd> </dl> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**PasswordHistoryLength**
</dt> <dd> <dl>

Gibt die Anzahl der vorherigen Kenn Wörter an, die in der Liste Verlauf gespeichert wurden. Der Benutzer kann ein Kennwort in der Verlaufs Liste nicht wieder verwenden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird der Wert der **PasswordHistoryLength** -Eigenschaft angezeigt.


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



Im folgenden Codebeispiel wird der Wert der **PasswordHistoryLength** -Eigenschaft angezeigt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsdomain ist als 00e4c220-SD16-11CE-abc4-02608c9e7553 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsdomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

 





