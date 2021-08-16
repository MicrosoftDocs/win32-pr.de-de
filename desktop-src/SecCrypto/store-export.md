---
description: Kopiert den Inhalt eines geöffneten Zertifikatspeichers in eine codierte Zeichenfolge.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Exportmethode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9adf0f42d64e0bc7ced76441ae0fe1da2d2b6609d9d717d5e3b26f8dd07db7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897804"
---
# <a name="storeexport-method"></a>Store. Exportmethode

\[Die **Exportmethode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Export-Methode** kopiert den Inhalt eines geöffneten [*Zertifikatspeichers*](../secgloss/c-gly.md) in eine codierte Zeichenfolge.

## <a name="syntax"></a>Syntax


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SaveAs* \[ in, optional\]
</dt> <dd>

Ein Wert der [CAPICOM \_ STORE SAVE AS \_ \_ \_ TYPE-Enumeration,](capicom-store-save-as-type.md) der das Format für den Exportvorgang angibt. Der Standardwert ist CAPICOM \_ STORE \_ SAVE AS \_ \_ SERIALIZED. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                     | Bedeutung                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <dt>**CAPICOM \_ STORE \_ SAVE \_ AS \_ SERIALIZED**</dt> </dl> | Der Speicher wird im serialisierten Format gespeichert.<br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <dt>**CAPICOM \_ STORE \_ SAVE \_ AS \_ PKCS7**</dt> </dl>                | Der Speicher wird im PKCS \# 7-Format gespeichert.<br/>   |



 

</dd> <dt>

*EncodingType* \[ in, optional\]
</dt> <dd>

Ein Wert der [CAPICOM \_ ENCODING \_ TYPE-Enumeration,](capicom-encoding-type.md) der den Codierungstyp des exportierten Speichers angibt. Der Standardwert ist CAPICOM \_ ENCODE \_ BASE64. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp haben. Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen CAPICOM \_ ENCODE \_ BASE64 verwendet. Eingeführt in CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_CAPICOM-CODIERUNG \_ BASE64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BINARY**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine Zeichenfolge zurück, die die Zertifikate im Speicher im angegebenen Codierungsformular enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Speicher**](store.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
