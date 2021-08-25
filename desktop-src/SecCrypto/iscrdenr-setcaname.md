---
description: Gibt den Namen der Zertifizierungsstelle an.
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: ISCrdEnr::setCAName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 726b1d6d6a31831e5db192b5a71dea9efa32f624333ee7f6d6d2eea432dacae9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960270"
---
# <a name="iscrdenrsetcaname-method"></a>ISCrdEnr::setCAName-Methode

Die **setCAName-Methode** gibt den Namen der [*Zertifizierungsstelle*](../secgloss/c-gly.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Wert, der angibt, ob der Name auf den Namen der Zertifizierungsstelle oder den Computernamen der Zertifizierungsstelle verweist. Wenn dieser Wert SCARD \_ ENROLL CA MACHINE NAME ist \_ \_ \_ (definiert als 0x01), bezieht sich der Name auf den Computernamen der Zertifizierungsstelle. Andernfalls bezieht sich der Name auf den Namen der Zertifizierungsstelle.

</dd> <dt>

*bstrCertTemplateName* \[ In\]
</dt> <dd>

Name der Zertifikatvorlage.

</dd> <dt>

*bstrCAName* \[ In\]
</dt> <dd>

Der Name der Zertifizierungsstelle, der mit der durch *bstrCertTemplateName* angegebenen Zertifikatvorlage verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um eine Zertifizierungsstelle für eine Zertifikatvorlage anzugeben.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
