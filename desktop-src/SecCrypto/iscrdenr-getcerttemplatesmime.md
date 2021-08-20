---
description: Wird verwendet, um zu bestimmen, ob eine Zertifikatvorlage die SzOID \_ PKIX \_ KP EMAIL \_ \_ PROTECTION-Schlüsselverwendung enthält.
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: ISCrdEnr::getCertTemplateSMIME-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8da8c9c3202c0955a001a63e77f85858fc6237d7476c0fc5222ae8f85e94a7c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515960"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>ISCrdEnr::getCertTemplateSMIME-Methode

Die **getCertTemplateSMIME-Methode** wird verwendet, um zu bestimmen, ob eine Zertifikatvorlage die SzOID \_ PKIX \_ KP EMAIL \_ \_ PROTECTION-Schlüsselverwendung enthält.

Wenn diese Schlüsselverwendung Teil der Zertifikatvorlage ist, unterstützt die Zertifikatvorlage [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME)-Vorgänge.

## <a name="syntax"></a>Syntax


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrCertTemplateName* \[ In\]
</dt> <dd>

Der Name des Zertifikats, das für die Verwendung des S/MIME-Schlüssels abgefragt wird.

</dd> <dt>

*pdwCertTemplateSMIME* \[ out\]
</dt> <dd>

Ein Zeiger auf ein **DWORD,** das den Wert 1 zurückgibt, wenn *bstrCertTemplateName* S/MIME unterstützt. Andernfalls wird 0 (null) zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

**Long-Wert** von 1, wenn *bstrCertTemplateName* S/MIME unterstützt; andernfalls 0 (null).

## <a name="remarks"></a>Hinweise

Die Konstante für szOID \_ PKIX \_ KP EMAIL PROTECTION ist in \_ \_ Wincrypt.h definiert.

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

[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
