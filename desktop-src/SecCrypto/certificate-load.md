---
description: Importiert ein Zertifikat aus einer Datei.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'ICertificate2:: Load-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367436"
---
# <a name="icertificate2load-method"></a>ICertificate2:: Load-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Load** -Methode importiert ein Zertifikat aus einer Datei. Diese Methode wurde in CAPICOM 2,0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die den Pfad zu einer CER-oder PFX-Datei enthält, die die Zertifikatsdaten enthält.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die das [*Klartext*](../secgloss/p-gly.md) -Kennwort für die Datei mit dem [*privaten Schlüssel*](../secgloss/p-gly.md) enthält. Das Kennwort kann bis zu 32 Unicode-Zeichen enthalten, einschließlich eines abschließenden NULL-Zeichens. Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).

</dd> <dt>

*Keystorageflag* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ \_ Schlüsselspeicherflag \_**](capicom-key-storage-flag.md) -Enumeration, die Schlüsselspeicherflags definiert. Der Standardwert ist der Standardwert von CAPICOM \_ Key \_ Storage \_ . In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                           | Bedeutung                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**Standardwert für CAPICOM- \_ Schlüssel \_ Speicher \_**</dt> </dl>                       | Standardschlüssel Speicher.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**zu \_ \_ \_ exportier barer CAPICOM-Schlüsselspeicher**</dt> </dl>              | Der Schlüssel ist exportierbar.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**Benutzer geschützter CAPICOM- \_ Schlüssel \_ Speicher \_ \_**</dt> </dl> | Der Schlüssel ist Benutzer geschützt.<br/> |



 

</dd> <dt>

*Keylocation* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ \_ schlüssellocation**](capicom-key-location.md) -Enumeration, die Schlüssel Speicherort Typen definiert. Der Standardwert ist der aktuelle CAPICOM- \_ \_ Benutzer \_ Schlüssel. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                               | Bedeutung                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**Schlüssel für aktuellen CAPICOM- \_ \_ Benutzer \_**</dt> </dl>    | Der Schlüssel ist ein Benutzerschlüssel.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**lokaler CAPICOM- \_ \_ Computer \_ Schlüssel**</dt> </dl> | Der Schlüssel ist ein Computer Schlüssel.<br/> |



 

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



 

 
