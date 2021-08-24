---
title: IADsDomain-Eigenschaftenmethoden (Iads.h)
description: Die Schnittstellenmethoden IADsDomain lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- IADsDomain-Eigenschaftenmethoden ADSI
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
ms.openlocfilehash: 90769faec8bc5e05f1aa590dd3211125665a4b07228b920e622fc5b33754e322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082494"
---
# <a name="iadsdomain-property-methods"></a>IADsDomain-Eigenschaftenmethoden

Die [**Schnittstellenmethoden IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**AutoUnlockInterval**
</dt> <dd> <dl>

Gibt die Mindestzeit an, die verstreichen muss, bevor das Konto automatisch erneut gestartet wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

**IsWorkgroup**
</dt> <dd> <dl>

Diese Eigenschaft wird nicht mehr implementiert.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **VARIANT \_ BOOL**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

**LockoutObservationInterval**
</dt> <dd> <dl>

Gibt das Zeitfenster an, in dem die Anzahl fehlerhafter Kennwörter überwacht und akkumuliert wird, bevor bestimmt wird, ob das Konto gesperrt werden muss. Wenn beispielsweise die Anzahl fehlerhafter Kennwortversuche für ein Konto den Schwellenwert (Maximal zulässige fehlerhafte Kennwörter) während des angegebenen Zeitraums (Sperrungs-Beobachtungsintervall) überschreitet, wird das Konto gesperrt, indem die entsprechende Eigenschaft in der Login Parameter-Eigenschaft festgelegt wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

**MaxBadPasswordsAllowed**
</dt> <dd> <dl>

Gibt die maximale Anzahl von fehlerhaften Kennwortanmeldungen an, die vor einer Kontosperrung zulässig sind.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

**MaxPasswordAge**
</dt> <dd> <dl>

Gibt das maximale Zeitintervall in Sekunden an, nach dem das Kennwort vom Benutzer geändert werden muss.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

**MinPasswordAge**
</dt> <dd> <dl>

Gibt das minimale Zeitintervall in Sekunden an, bevor das Kennwort geändert werden kann.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

**MinPasswordLength**
</dt> <dd> <dl>

Gibt die Mindestanzahl von Zeichen an, die für ein Kennwort verwendet werden müssen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

**PasswordAttributes**
</dt> <dd> <dl>

Gibt Einschränkungen für Kennwörter an, wie in der folgenden Liste von Attributen und Werten definiert.

> [!Note]  
> Für PASSWORD ATTR COMPLEX muss das Kennwort mindestens ein Interpunktionszeichen \_ \_ oder ein nicht druckbares Zeichen enthalten.

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

**KENNWORT \_ ATTR \_ NONE** (0x00000000)


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

**KENNWORT \_ ATTR \_ MIXED \_ CASE** (0x00000001)


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

**KENNWORT \_ ATTR \_ COMPLEX** (0x00000002)


</dt> <dd></dd> </dl> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

Gibt die Anzahl der vorherigen Kennwörter an, die in der Verlaufsliste gespeichert wurden. Der Benutzer kann ein Kennwort nicht in der Verlaufsliste wiederverwenden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

Im folgenden Codebeispiel wird der Wert der **PasswordHistoryLength-Eigenschaft** angezeigt.


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



Im folgenden Codebeispiel wird der Wert der **PasswordHistoryLength-Eigenschaft** angezeigt.


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
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsDomain ist als 00E4C220-FD16-11CE-ABC4-02608C9E7553 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[Schnittstelleneigenschaftsmethoden](interface-property-methods.md)
</dt> </dl>

 

 





