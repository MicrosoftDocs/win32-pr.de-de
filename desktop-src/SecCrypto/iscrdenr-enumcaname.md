---
description: Enumeriert den Namen der Zertifizierungsstellen (CAs) für einen angegebenen Zertifikatvorlagennamen.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: ISCrdEnr::enumCAName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 11742525d616aecc8d83871ae2a59025d1034513ae99d8a7253d16d9e0f64dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005218"
---
# <a name="iscrdenrenumcaname-method"></a>ISCrdEnr::enumCAName-Methode

Die **enumCAName-Methode** aufzählt den Namen der Zertifizierungsstellen (CAs) für einen angegebenen Zertifikatvorlagennamen. [](../secgloss/c-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ In\]
</dt> <dd>

Der nullbasierte Index für die Enumerationssequenz.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein -Wert, der bestimmt, ob der Name auf den Namen der Zertifizierungsstelle oder den Computernamen der Zertifizierungsstelle verweist. Wenn dieser Wert SCARD ENROLL CA MACHINE NAME (definiert als 0x01) ist, bezieht sich der Name auf den \_ \_ \_ \_ Computernamen der Zertifizierungsstelle. Andernfalls verweist der Name auf den Namen der Zertifizierungsstelle.

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr ist als 753988a1-1357-436d-9cf5-f089bdd67d64 definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
