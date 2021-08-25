---
description: Gibt den Namen der Zertifikatvorlage an.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: ISCrdEnr::setCertTemplateName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 5f757ead06e5d1769e109bcbfc8e3510f4298f32145d60c4c0bc992a01f3ab36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993040"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>ISCrdEnr::setCertTemplateName-Methode

Die **setCertTemplateName-Methode** gibt den Namen der Zertifikatvorlage an.

## <a name="syntax"></a>Syntax


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein Wert, der bestimmt, ob der tatsächliche Name oder Anzeigename der Zertifikatvorlage festgelegt wird. Wenn *dwFlags über* den Wert SCARD ENROLL CERT TEMPLATE DISPLAY NAME verfügt, wird der Anzeigename der \_ \_ \_ \_ \_ Zertifikatvorlage festgelegt. Andernfalls wird der tatsächliche Name der Zertifikatvorlage festgelegt.

</dd> <dt>

*bstrCertTemplateName* \[ In\]
</dt> <dd>

Name der Zertifikatvorlage, die in der Zertifikatanforderung verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Hinweise

Wenn Sie den Namen der Zertifikatvorlage nicht durch Aufrufen von **ISCrdEnr::setCertTemplateName** festlegen, wird der Name standardmäßig auf den Vornamen in der Liste der verfügbaren Zertifikatvorlagen festgelegt.

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

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




