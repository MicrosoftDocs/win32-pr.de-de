---
description: Importiert ein Zertifikat aus einer Datei.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: ICertificate2::Load-Methode
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
ms.openlocfilehash: fceb6ba9a9868711aefae64865c08e49551e20e8a05686e1691f390f05b76071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771534"
---
# <a name="icertificate2load-method"></a>ICertificate2::Load-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Load-Methode** importiert ein Zertifikat aus einer Datei. Diese Methode wurde in CAPICOM 2.0 eingeführt.

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

*FileName* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die den Pfad zu einer CER- oder PFX-Datei enthält, die die Zertifikatdaten enthält.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die das [*Klartextkennwort*](../secgloss/p-gly.md) für die Datei mit dem [*privaten Schlüssel*](../secgloss/p-gly.md) enthält. Das Kennwort kann bis zu 32 Unicode-Zeichen enthalten, einschließlich eines abschließenden NULL-Zeichens. Informationen zum Schutz des Kennworts finden Sie unter [Behandeln von Kennwörtern.](../secbp/handling-passwords.md)

</dd> <dt>

*KeyStorageFlag* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ KEY STORAGE \_ \_ FLAG-Enumeration,**](capicom-key-storage-flag.md) der Schlüsselspeicherflags definiert. Der Standardwert ist CAPICOM \_ KEY \_ STORAGE \_ DEFAULT. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                           | Bedeutung                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**\_ \_ \_ CAPICOM-SCHLÜSSELSPEICHERSTANDARD**</dt> </dl>                       | Standardschlüsselspeicher.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**CAPICOM \_ KEY \_ STORAGE \_ EXPORTABLE**</dt> </dl>              | Der Schlüssel kann exportiert werden.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**CAPICOM \_ KEY \_ STORAGE \_ USER \_ PROTECTED**</dt> </dl> | Der Schlüssel ist vom Benutzer geschützt.<br/> |



 

</dd> <dt>

*KeyLocation* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ KEY \_ LOCATION-Enumeration,**](capicom-key-location.md) der Schlüsselspeicherorttypen definiert. Der Standardwert ist CAPICOM \_ CURRENT \_ USER \_ KEY. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                               | Bedeutung                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**CAPICOM \_ – AKTUELLER \_ \_ BENUTZERSCHLÜSSEL**</dt> </dl>    | Der Schlüssel ist ein Benutzerschlüssel.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**CAPICOM \_ LOCAL \_ MACHINE \_ KEY**</dt> </dl> | Der Schlüssel ist ein Computerschlüssel.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode löst CAPICOM \_ E \_ NOT ALLOWED \_ aus, wenn ein Skript aus einer webbasierten Anwendung erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
