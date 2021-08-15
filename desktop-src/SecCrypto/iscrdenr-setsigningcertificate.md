---
description: Gibt ein Signaturzertifikat (auch als Registrierungs-Agent-Zertifikat bezeichnet) an.
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: ISCrdEnr::setSigningCertificate-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8b93e2b76e46ed75abcd6460f351dfc2780826c2ff5e7dc8d07e8d48ae617e4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425730"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>ISCrdEnr::setSigningCertificate-Methode

Die **setSigningCertificate-Methode** gibt ein Signaturzertifikat (auch als *Registrierungs-Agent-Zertifikat* bezeichnet) an.

Vor der Registrierung im Namen von Benutzern müssen Sie ein Signaturzertifikat auswählen oder festlegen. Der diesem Signaturzertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) wird zum Signieren einer PKCS \# 7-Anforderung verwendet. PKCS \# 7 wiederum enthält die PKCS \# 10-Anforderung des Benutzers (die mit dem privaten Schlüssel des Benutzers signiert ist).

## <a name="syntax"></a>Syntax


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Für die zukünftige Verwendung reserviert. Legen Sie diesen Wert auf 0 (null) fest.

</dd> <dt>

*bstrCertTemplateName* \[ In\]
</dt> <dd>

Name der Zertifikatvorlage für das Signaturzertifikat. Sie können den Wert "EnrollmentAgent" verwenden, wenn Sie ein EnrollmentAgent-Zertifikat erhalten haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte.](common-hresult-values.md)

## <a name="remarks"></a>Hinweise

Bevor Sie sich im Namen eines Benutzers registrieren, müssen Sie zunächst ein Signaturzertifikat abrufen. Sie können ein Signaturzertifikat mithilfe des MMC-Snap-Ins des Zertifikat-Managers abrufen. Die **setSigningCertificate-Methode** ruft nicht das Signaturzertifikat ab, sondern informiert die Smartcard-Registrierungssteuerung, die zuvor das Signaturzertifikat zur Verwendung erhalten hat. Die **setSigningCertificate-Methode** durchsucht den Speicher "My" des Aufrufers nach dem letzten Signaturzertifikat, das der durch *bstrCertTemplateName* angegebenen Zertifikatvorlage entspricht.

Eine Alternative zu **setSigningCertificate** ist **ISCrdEnr::setSigningCertificate.**

Nachdem ein Signaturzertifikat festgelegt wurde, kann sein Name durch Aufrufen von [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)abgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr ist als 753988a1-1357-436d-9cf5-f089bdd67d64 definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
