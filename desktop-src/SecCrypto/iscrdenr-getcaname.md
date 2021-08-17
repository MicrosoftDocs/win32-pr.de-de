---
description: Ruft den Namen der angegebenen Zertifizierungsstelle für eine bestimmte Zertifikatvorlage ab.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: ISCrdEnr::getCAName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 6de5d1108ab09c9658af307d6a67c5a94a5dc35514720a221540de263f516c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960280"
---
# <a name="iscrdenrgetcaname-method"></a>ISCrdEnr::getCAName-Methode

Die **getCAName-Methode** ruft den Namen der angegebenen Zertifizierungsstelle [*für*](../secgloss/c-gly.md) eine bestimmte Zertifikatvorlage ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein -Wert, der bestimmt, ob der Name auf den Namen der Zertifizierungsstelle oder den Computernamen der Zertifizierungsstelle verweist. Wenn dieser Wert SCARD ENROLL CA MACHINE NAME (definiert als 0x01) ist, bezieht sich der Name auf den Computernamen der Zertifizierungsstelle. Andernfalls bezieht sich der Name auf den Namen der \_ \_ \_ \_ Zertifizierungsstelle.

</dd> <dt>

*bstrCertTemplateName* \[ In\]
</dt> <dd>

Der Name der Zertifikatvorlage.

</dd> <dt>

*pbstrCAName* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen der Zertifizierungsstelle zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen der Zertifizierungsstelle darstellt.

## <a name="remarks"></a>Hinweise

Der Standardname der Zertifizierungsstelle ist der Vorname in der liste der verfügbaren Zertifizierungsstellen.

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

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
