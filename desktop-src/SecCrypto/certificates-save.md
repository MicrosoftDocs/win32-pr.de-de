---
description: Speichert die Zertifikat Objekte in der Auflistung.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Zertifikats. Save-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367833"
---
# <a name="certificatessave-method"></a>Zertifikats. Save-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Mit der **Save** -Methode werden die [**Zertifikat**](certificate.md) Objekte in der Auflistung gespeichert.

## <a name="syntax"></a>Syntax


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Ausgabedatei enthält, in der die Zertifikate gespeichert werden.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die das [*Klartext*](../secgloss/p-gly.md) -Kennwort für eine Datei mit einem [*privaten Schlüssel*](../secgloss/p-gly.md) enthält. Der Standardwert ist eine leere Zeichenfolge (""). Bis zu 32 Unicode-Zeichen, einschließlich eines abschließenden NULL-Zeichens, können für das Kennwort verwendet werden. Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).

</dd> <dt>

*SaveAs* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ Zertifikate \_ Save \_ As \_ Type**](capicom-certificates-save-as-type.md) -Enumeration, die das Format der Ausgabedatei angibt. Der Standardwert sind CAPICOM-Zertifikate, die \_ \_ \_ als \_ PFX gespeichert werden. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**CAPICOM \_ - \_ Zertifikate \_ als \_ PFX speichern**</dt> </dl>                      | Die Zertifikate werden als PFX gespeichert.<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**CAPICOM- \_ Zertifikate \_ speichern \_ als \_ PKCS7**</dt> </dl>                | Die Zertifikate werden als PKCS 7 gespeichert \# .<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**CAPICOM- \_ Zertifikate werden \_ \_ als \_ serialisiert gespeichert.**</dt> </dl> | Die Zertifikate werden als serialisiert gespeichert.<br/> |



 

</dd> <dt>

*Exportflag* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ \_ exportflag**](capicom-export-flag.md) -Enumeration, der angibt, ob Export Fehler des privaten Schlüssels ignoriert werden. Der Standardwert ist "CAPICOM \_ Export \_ default". In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                                                          | Bedeutung                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**Standardwert für CAPICOM- \_ Export \_**</dt> </dl>                                                                                                      | Export Fehler des privaten Schlüssels werden nicht ignoriert.<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**CAPICOM \_ - \_ Export \_ \_ Fehler beim \_ nicht \_ exportierbaren privaten Schlüssel \_ ignorieren**</dt> </dl> | Export Fehler des privaten Schlüssels werden ignoriert.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.

Die [**Zertifikat**](certificate.md) Objekte können mithilfe der [**Store. Load**](store-load.md) -Methode abgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zertifikate**](certificates.md)
</dt> </dl>

 

 
