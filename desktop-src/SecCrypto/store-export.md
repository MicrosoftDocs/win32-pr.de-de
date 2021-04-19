---
description: Kopiert den Inhalt eines geöffneten Zertifikat Speicher in eine codierte Zeichenfolge.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Export-Methode
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
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367743"
---
# <a name="storeexport-method"></a>Store. Export-Methode

\[Die **Export** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Export** Methode kopiert den Inhalt eines geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md) in eine codierte Zeichenfolge.

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

Ein Wert der " [CAPICOM \_ Store"- \_ \_ \_ Dateityp](capicom-store-save-as-type.md) -Enumeration, die das Format für den Export Vorgang angibt. Der Standardwert ist "CAPICOM \_ Store \_ Save \_ As \_ serialized". Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                     | Bedeutung                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <dt>**CAPICOM- \_ Speicher, \_ gespeichert \_ als \_ serialisiert**</dt> </dl> | Der Speicher wird im serialisierten Format gespeichert.<br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <dt>**CAPICOM \_ Store \_ \_ PKCS7 speichern \_ unter**</dt> </dl>                | Der Speicher wird im PKCS \# 7-Format gespeichert.<br/>   |



 

</dd> <dt>

*EncodingType* \[ in, optional\]
</dt> <dd>

Ein Wert der [CAPICOM- \_ \_ Codierungstyp](capicom-encoding-type.md) -Enumeration, die den Codierungstyp des exportierten Speicher Werts angibt. Der Standardwert ist CAPICOM- \_ Codieren \_ Base64. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Codieren \_ Any**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen. Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet. Eingeführt in CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ Codieren \_ Base64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine Zeichenfolge zurück, die die Zertifikate im Speicher im angegebenen Codierungs Formular enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
