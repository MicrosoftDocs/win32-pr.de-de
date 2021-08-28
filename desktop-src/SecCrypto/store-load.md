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
ms.openlocfilehash: 1b39c2be625ff88869d27e6210e49496352af868c73557d2657c509fd0e79f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897790"
---
# <a name="storeload-method"></a>Store. Load-Methode

\[Die **Load-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Load-Methode** importiert Zertifikate aus einer Datei in den Speicher.

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

*FileName* \[ In\]
</dt> <dd>

Die Zeichenfolge, die den Pfad zu einer CER-, SST-, SPC-, P7S- oder PFX-Datei oder zu einer signierten Authenticode-Datei enthält.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Die Zeichenfolge, die das Klartextkennwort für die Datei enthält. Für das Kennwort können bis zu 32 Unicode-Zeichen verwendet werden, einschließlich eines beendenden NULL-Zeichens. Informationen zum Schutz des Kennworts finden Sie unter [Behandeln von Kennwörtern.](../secbp/handling-passwords.md)

</dd> <dt>

*KeyStorageFlag* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ KEY STORAGE \_ \_ FLAG-Enumeration,**](capicom-key-storage-flag.md) die Schlüsselspeicherflags definiert. Der Standardwert ist CAPICOM \_ KEY \_ STORAGE \_ DEFAULT. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                           | Bedeutung                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**CAPICOM \_ KEY \_ STORAGE \_ DEFAULT**</dt> </dl>                       | Standardspeicher für Schlüssel.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**CAPICOM \_ KEY \_ STORAGE \_ EXPORTABLE**</dt> </dl>              | Der Schlüssel kann exportiert werden.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**CAPICOM \_ KEY \_ STORAGE \_ USER \_ PROTECTED**</dt> </dl> | Der Schlüssel ist benutzergeschützt.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die **Load-Methode** für einen Speicher aufgerufen wird, werden alle erstellten Schlüsselcontainer gelöscht, wenn der Speicher gelöscht wird. Wenn z. B. eine PFX-Datei in einen Speicher geladen und später einem Systemspeicher (z. B. my store) aus dem Speicher hinzugefügt wird, enthält das Zertifikat im Speicher My keinen Schlüssel. In diesem Fall sollte die PFX-Datei direkt in den Speicher My geladen werden.

Diese Methode löst CAPICOM E NOT ALLOWED aus, wenn ein Skript \_ aus einer \_ \_ webbasierten Anwendung erstellt wird.

Wenn das Kennwort die Datei mit dem privaten Schlüssel nicht entschlüsseln kann, sollte der Standardmäßige Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) abgefragt werden. Wenn der Standard-CSP der Microsoft Base Cryptographic Provider ist und der Entschlüsselungsvorgang fehlschlägt, sollte der Entschlüsselungsvorgang erneut mit dem Microsoft Strong Cryptographic Provider oder dem Microsoft Enhanced Cryptographic Provider versucht werden, sofern verfügbar.

Wenn das in den Speicher geladene Zertifikat mit dem bereits vorhandenen Zertifikat identisch ist, löscht die **Load-Methode** das vorhandene Zertifikat aus dem Speicher und fügt dann das neue Zertifikat hinzu. Das neue Zertifikat erbt Eigenschaften vom vorhandenen Zertifikat. Der vorhandene Private Key-Container wird durch den neuen Privaten Schlüsselcontainer ersetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Speicher**](store.md)
</dt> </dl>

 

 
