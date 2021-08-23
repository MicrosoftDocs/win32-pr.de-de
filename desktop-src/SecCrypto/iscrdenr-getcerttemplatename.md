---
description: Ruft den Namen der Zertifikatvorlage ab.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: ISCrdEnr::getCertTemplateName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: aaf37f3907bc2b26ca1adbbded7be5ed7897a74ea9664d4353354d5ad9657d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409620"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>ISCrdEnr::getCertTemplateName-Methode

Die **getCertTemplateName-Methode** ruft den Namen der Zertifikatvorlage ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein -Wert, der bestimmt, ob der echte Name oder Anzeigename der Zertifikatvorlage zurückgegeben wird. Wenn *dwFlags* über den Wert SCARD \_ ENROLL CERT TEMPLATE DISPLAY NAME verfügt, wird der Anzeigename der Zertifikatvorlage abgerufen. Andernfalls wird der tatsächliche Name der Zertifikatvorlage \_ \_ \_ \_ angezeigt.

</dd> <dt>

*pbstrCertTemplateName* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen der Zertifikatvorlage zurückgibt, die in der Zertifikatanforderung [*verwendet wird.*](../secgloss/c-gly.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen der Zertifikatvorlage darstellt, die in der Zertifikatanforderung [*verwendet wird.*](../secgloss/c-gly.md)

## <a name="remarks"></a>Hinweise

Wenn Sie den Namen der Zertifikatvorlage nicht durch Aufrufen von [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)festlegen, wird der Name standardmäßig auf den Vornamen in der Liste der verfügbaren Zertifikatvorlagen festgelegt.

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

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
