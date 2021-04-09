---
description: Wird verwendet, um zu bestimmen, ob eine Zertifikat Vorlage die \_ \_ \_ Verwendung der e-Mail- \_ Schutz Schlüssel für den szoid-PKIX
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'Iscrdenr:: getcerttemplatesmime-Methode'
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
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867399"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>Iscrdenr:: getcerttemplatesmime-Methode

Die **getcerttemplatesmime** -Methode wird verwendet, um zu bestimmen, ob eine Zertifikat Vorlage die \_ \_ \_ Verwendung des e-Mail-Schutzes für den szoomid PKIX KP- \_ Schlüssel enthält

Wenn diese Schlüssel Verwendung Teil der Zertifikat Vorlage ist, werden von der Zertifikat Vorlage [*sichere/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) Vorgänge (S/MIME) unterstützt.

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

*bstraucerttemplatename* \[ in\]
</dt> <dd>

Der Name des Zertifikats, das für die Verwendung von S/MIME-Schlüsseln abgefragt wird.

</dd> <dt>

*pdwcerttemplatesmime* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein **DWORD** , das den Wert 1 zurückgibt, wenn *bstrincerttemplatename* S/MIME unterstützt. Andernfalls wird NULL zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Der **lange** Wert 1, wenn *bstrincerttemplatename* S/MIME unterstützt. andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Die Konstante für szoid \_ PKIX \_ KP \_ -e-Mail- \_ Schutz ist in Wincrypt. h definiert.

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

[**Iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
