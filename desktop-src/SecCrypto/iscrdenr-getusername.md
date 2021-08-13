---
description: Ruft den Namen des Benutzers ab, für den die Zertifikatregistrierung vorgesehen ist.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: ISCrdEnr::getUserName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b61dd43980049355621c2ee4085634303c55e0f9dac79db839602d07c7d61f94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409447"
---
# <a name="iscrdenrgetusername-method"></a>ISCrdEnr::getUserName-Methode

Die **getUserName-Methode** ruft den Namen des Benutzers ab, für den die Zertifikatregistrierung vorgesehen ist.

Vor dem Aufrufen dieser Methode müssen Sie den Benutzernamen in einem Aufruf von [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) oder [**ISCrdEnr::setUserName angeben.**](iscrdenr-setusername.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Wert muss entweder null (0), SCARD \_ ENROLL \_ UPN \_ NAME oder SCARD ENROLL SAM \_ COMPATIBLE NAME \_ \_ \_ sein.

Wenn dieser Wert SCARD \_ ENROLL \_ UPN \_ NAME ist, gibt **getUserName** den Universal Principal Name (UPN) des Benutzers zurück, z. B. " someone@example.com ".

Wenn dieser Wert SCARD ENROLL SAM COMPATIBLE NAME ist, gibt die Methode den Sam-Namen (Security Access Manager) des Benutzers im Format \_ \_ \_ \_ "DOMAIN \\ USER" zurück.

Wenn dieser Wert 0 (null) ist, gibt die Methode den UPN-Namen des Benutzers zurück, sofern vorhanden. Wenn der Benutzer keinen UPN-Namen hat, gibt die Methode den SAM-Namen des Benutzers zurück.

</dd> <dt>

*pbstrUserName* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Benutzers zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte.](common-hresult-values.md)

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen des Benutzers darstellt.

## <a name="remarks"></a>Hinweise

Sie können den Namen des Benutzers [](../secgloss/s-gly.md) angeben, für den die Smartcard ausgestellt wird, indem Sie [**entweder ISCrdEnr::setUserName**](iscrdenr-setusername.md) oder [**ISCrdEnr::selectUserName aufrufen.**](iscrdenr-selectusername.md) Nachdem ein Benutzername angegeben wurde, kann sein Wert durch Aufrufen von **getUserName abgerufen werden.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr ist als 753988a1-1357-436d-9cf5-f089bdd67d64 definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 
