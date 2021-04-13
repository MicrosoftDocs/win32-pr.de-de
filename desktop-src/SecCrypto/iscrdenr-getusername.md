---
description: Ruft den Namen des Benutzers ab, für den die Zertifikat Registrierung vorgesehen ist.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'Iscrdenr:: getUserName-Methode'
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
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348508"
---
# <a name="iscrdenrgetusername-method"></a>Iscrdenr:: getUserName-Methode

Die **GetUsername** -Methode ruft den Namen des Benutzers ab, für den die Zertifikat Registrierung vorgesehen ist.

Vor dem Aufrufen dieser Methode müssen Sie den Benutzernamen in einem Aufruf von [**iscrdenr:: selectusername**](iscrdenr-selectusername.md) oder [**iscrdenr:: setUserName**](iscrdenr-setusername.md)angeben.

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

*dwFlags* \[ in\]
</dt> <dd>

Dieser Wert muss entweder NULL (0), der UPN-Name von "SCard \_ Enroll" \_ oder " \_ SCard \_ ENROLL \_ Sam \_ Compatible \_ Name" lauten.

Wenn dieser Wert "SCard \_ ENROLL \_ UPN \_ Name" ist, gibt **GetUsername** den universellen Prinzipal Namen (UPN) des Benutzers zurück, z someone@example.com . b. "".

Wenn dieser Wert "SCard \_ ENROLL \_ Sam \_ Compatible \_ Name" ist, gibt die Methode den SAM-Namen (Security Access Manager) des Benutzers im Format "Domänen \\ Benutzer" zurück.

Wenn dieser Wert 0 (null) ist, gibt die Methode den UPN-Namen des Benutzers zurück, sofern vorhanden. Wenn der Benutzer keinen UPN-Namen hat, gibt die Methode den SAM-Namen des Benutzers zurück.

</dd> <dt>

*pbstrusername* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Benutzers zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen des Benutzers darstellt.

## <a name="remarks"></a>Bemerkungen

Sie können den Namen des Benutzers angeben, für den die [*Smartcard*](../secgloss/s-gly.md) ausgestellt wird, indem Sie entweder [**iscrdenr:: setUserName**](iscrdenr-setusername.md) oder [**iscrdenr:: selectusername**](iscrdenr-selectusername.md)aufrufen. Nachdem ein Benutzername angegeben wurde, kann der zugehörige Wert durch Aufrufen von **GetUsername** abgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscrdenr**](iscrdenr.md)
</dt> <dt>

[**Iscrdenr:: resetuser**](iscrdenr-resetuser.md)
</dt> <dt>

[**Iscrdenr:: selectusername**](iscrdenr-selectusername.md)
</dt> <dt>

[**Iscrdenr:: setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 
