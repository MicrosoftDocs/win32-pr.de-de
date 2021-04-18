---
description: Speichert das Zertifikat in einer Datei.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'ICertificate2:: Save-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364911"
---
# <a name="icertificate2save-method"></a>ICertificate2:: Save-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Mit der **Save** -Methode wird das Zertifikat in einer Datei gespeichert. Diese Methode wurde in CAPICOM 2,0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Ausgabedatei enthält, in der das Zertifikat gespeichert wird.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die das [*Klartext*](../secgloss/p-gly.md) -Kennwort für eine Datei mit einem [*privaten Schlüssel*](../secgloss/p-gly.md) enthält. Das Kennwort kann bis zu 32 Unicode-Zeichen enthalten, einschließlich eines abschließenden NULL-Zeichens. Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).

</dd> <dt>

*SaveAs* \[ in, optional\]
</dt> <dd>

Ein Wert des [**CAPICOM- \_ Zertifikats " \_ Save \_ As \_ Type**](capicom-certificate-save-as-type.md) Enumeration", das das Format der Ausgabedatei angibt. Der Standardwert ist **CAPICOM \_ Certificate \_ Save \_ As \_ CER**. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                  | Bedeutung                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ speichern \_ als \_ CER**</dt> </dl> | Die Ausgabedatei wird als CER-Datei formatiert, ohne dass private Schlüssel gespeichert werden.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <dt>**CAPICOM \_ - \_ Zertifikat \_ als \_ PFX speichern**</dt> </dl> | Die Ausgabedatei wird als PFX-Datei (PKCS \# 12) formatiert, und alle zugehörigen privaten Schlüssel, die exportierbar sind, werden ebenfalls gespeichert.<br/> |



 

</dd> <dt>

*IncludeOption* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ Certificate \_ include- \_ Option**](capicom-certificate-include-option.md) -Enumeration, die angibt, wie viele Zertifikate in der Kette in der Ausgabedatei gespeichert werden. Der Standardwert ist "CAPICOM \_ Certificate \_ include \_ End \_ Entity \_ only". In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                             | Bedeutung                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM- \_ Zertifikats \_ include- \_ Kette \_ mit Ausnahme von \_ root**</dt> </dl> | Speichert alle Zertifikate in der Kette mit Ausnahme der Stamm Entität.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ einschließlich \_ ganzer \_ Kette**</dt> </dl>                    | Speichert die komplette Zertifikatskette.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ schließt \_ nur End- \_ Entität \_ ein.**</dt> </dl>       | Speichert nur das Endentitäts Zertifikat.<br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
