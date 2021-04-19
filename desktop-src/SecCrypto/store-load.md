---
description: Importiert Zertifikate aus einer Datei in den Speicher.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store. Load-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355053"
---
# <a name="storeload-method"></a>Store. Load-Methode

\[Die **Load** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Load** -Methode importiert Zertifikate aus einer Datei in den Speicher.

## <a name="syntax"></a>Syntax


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Die Zeichenfolge, die den Pfad zu einer CER-, SST-,. SPC-,. p7s-oder PFX-Datei oder einer beliebigen mit Authenticode signierten Datei enthält.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Die Zeichenfolge, die das Klartext-Kennwort für die Datei enthält. Bis zu 32 Unicode-Zeichen, einschließlich eines abschließenden NULL-Zeichens, können für das Kennwort verwendet werden. Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).

</dd> <dt>

*Keystorageflag* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ \_ Schlüsselspeicherflag \_**](capicom-key-storage-flag.md) -Enumeration, die Schlüsselspeicherflags definiert. Der Standardwert ist der Standardwert von CAPICOM \_ Key \_ Storage \_ . Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                           | Bedeutung                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**Standardwert für CAPICOM- \_ Schlüssel \_ Speicher \_**</dt> </dl>                       | Standardschlüssel Speicher.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**zu \_ \_ \_ exportier barer CAPICOM-Schlüsselspeicher**</dt> </dl>              | Der Schlüssel ist exportierbar.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**Benutzer geschützter CAPICOM- \_ Schlüssel \_ Speicher \_ \_**</dt> </dl> | Der Schlüssel ist Benutzer geschützt.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die **Load** -Methode für einen Speicher Speicher aufgerufen wird, werden alle erstellten Schlüssel Container gelöscht, wenn der Speicher Speicher gelöscht wird. Wenn z. b. eine PFX-Datei in einen Speicher Speicher geladen und später einem Systemspeicher (z. b. dem eigenen Speicher) aus dem Speicher Speicher hinzugefügt wird, enthält das Zertifikat im My Store keinen Schlüssel. In diesem Fall muss die PFX-Datei direkt in den My-Speicher geladen werden.

Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.

Wenn das Kennwort die Datei mit dem privaten Schlüssel nicht entschlüsseln kann, sollte der Standard- [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) abgefragt werden. Wenn der Standard-CSP der Kryptografieanbieter von Microsoft ist und der Entschlüsselungsvorgang fehlschlägt, sollte der Entschlüsselungsvorgang erneut mit dem Microsoft-starken Kryptografieanbieter oder Microsoft Enhanced Cryptographic Provider ausgeführt werden, je nachdem, welcher Wert verfügbar ist.

Wenn das Zertifikat, das in den Speicher geladen wird, dasselbe ist, das bereits vorhanden ist, löscht die **Load** -Methode das vorhandene Zertifikat aus dem Speicher und fügt dann das neue Zertifikat hinzu. Das neue Zertifikat erbt die Eigenschaften des vorhandenen Zertifikats. Der vorhandene Container für den privaten Schlüssel wird durch den neuen Container für private Schlüssel ersetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> </dl>

 

 
