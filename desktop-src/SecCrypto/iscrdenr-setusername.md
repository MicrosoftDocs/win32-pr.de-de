---
description: Gibt den Namen des Benutzers an, für den die Zertifikat Registrierung vorgesehen ist.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'Iscrdenr:: setUserName-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373366"
---
# <a name="iscrdenrsetusername-method"></a>Iscrdenr:: setUserName-Methode

Die **setUserName** -Methode gibt den Namen des Benutzers an, für den die Zertifikat Registrierung vorgesehen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Bei diesem Wert muss es sich um den Namen der "SCard \_ ENROLL \_ UPN" \_ (definiert als 1) oder "SCard \_ Enroll" \_ Sam- \_ kompatiblen \_ namens (definiert als 2) handeln.

Legen Sie diesen Wert auf \_ "SCard ENROLL \_ UPN Name" fest \_ , wenn der in *bstrUsername* angegebene Name der universelle Prinzipal Name des Benutzers (z. b. "") ist someone@example.com . Der UPN-Name des Benutzers muss einem vorhandenen Sam-Namen (Security Access Manager) entsprechen.

Legen Sie diesen Wert auf \_ "SCard ENROLL \_ Sam \_ Compatible Name" fest \_ , wenn der in *bstrUsername* angegebene Name dem Sam-Namen des Benutzers im Format "Domänen \\ Benutzer" entspricht.

</dd> <dt>

*bstrUsername* \[ in\]
</dt> <dd>

Name des Benutzers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode können Sie den Benutzernamen angeben, der als [*Smartcard*](../secgloss/s-gly.md)ausgegeben werden soll. Eine Alternative zu " **setUserName** " ist " [**iscrdenr:: selectusername**](iscrdenr-selectusername.md)".

Nachdem ein Benutzername angegeben wurde, kann der zugehörige Wert durch Aufrufen von [**GetUsername**](iscrdenr-getusername.md)abgerufen werden.

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

[**Iscrdenr:: GetUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**Iscrdenr:: resetuser**](iscrdenr-resetuser.md)
</dt> <dt>

[**Iscrdenr:: selectusername**](iscrdenr-selectusername.md)
</dt> </dl>

 

 
