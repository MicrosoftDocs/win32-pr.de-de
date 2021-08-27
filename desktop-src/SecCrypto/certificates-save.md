---
description: Speichert die Zertifikatobjekte in der Auflistung.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Certificates.Save-Methode
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
ms.openlocfilehash: c3d724a6859a1fbc7765822227290facfb2c2f021fce2f5815f32c5e91fe6453
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126760"
---
# <a name="certificatessave-method"></a>Certificates.Save-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Save-Methode** speichert [**die Certificate-Objekte**](certificate.md) in der Auflistung.

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

*FileName* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Ausgabedatei enthält, in der die Zertifikate gespeichert werden.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die das [*Klartextkennwort*](../secgloss/p-gly.md) für eine [*Datei mit privatem Schlüssel*](../secgloss/p-gly.md) enthält. Der Standardwert ist eine leere Zeichenfolge (""). Für das Kennwort können bis zu 32 Unicode-Zeichen verwendet werden, einschließlich eines beendenden NULL-Zeichens. Informationen zum Schutz des Kennworts finden Sie unter [Behandeln von Kennwörtern.](../secbp/handling-passwords.md)

</dd> <dt>

*SaveAs* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ CERTIFICATES \_ SAVE AS \_ \_ TYPE-Enumeration,**](capicom-certificates-save-as-type.md) der das Format der Ausgabedatei angibt. Der Standardwert ist CAPICOM \_ CERTIFICATES \_ SAVE AS \_ \_ PFX. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**\_CAPICOM-ZERTIFIKATE \_ SPEICHERN ALS \_ \_ PFX**</dt> </dl>                      | Die Zertifikate werden als PFX gespeichert.<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**\_CAPICOM-ZERTIFIKATE \_ SPEICHERN ALS \_ \_ PKCS7**</dt> </dl>                | Die Zertifikate werden als PKCS \# 7 gespeichert.<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**\_CAPICOM-ZERTIFIKATE \_ WERDEN ALS \_ \_ SERIALISIERT SPEICHERN**</dt> </dl> | Die Zertifikate werden als serialisiert gespeichert.<br/> |



 

</dd> <dt>

*ExportFlag* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ EXPORT \_ FLAG-Enumeration,**](capicom-export-flag.md) der angibt, ob Exportfehler für private Schlüssel ignoriert werden. Der Standardwert ist CAPICOM \_ EXPORT \_ DEFAULT. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                                                          | Bedeutung                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**CAPICOM \_ EXPORT \_ DEFAULT**</dt> </dl>                                                                                                      | Fehler beim Exportieren privater Schlüssel werden nicht ignoriert.<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**CAPICOM \_ EXPORT \_ IGNORE \_ PRIVATE \_ KEY \_ NOT \_ EXPORTABLE \_ ERROR**</dt> </dl> | Fehler beim Exportieren privater Schlüssel werden ignoriert.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode löst CAPICOM E NOT ALLOWED aus, wenn ein Skript \_ aus einer \_ \_ webbasierten Anwendung erstellt wird.

Die [**Zertifikatobjekte**](certificate.md) können mithilfe der [**-Store. Load-Methode.**](store-load.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zertifikate**](certificates.md)
</dt> </dl>

 

 
