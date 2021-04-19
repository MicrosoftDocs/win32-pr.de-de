---
description: Kopiert ein Zertifikat in eine codierte Zeichenfolge.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'ICertificate2:: Export-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371506"
---
# <a name="icertificate2export-method"></a>ICertificate2:: Export-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Export** Methode kopiert ein Zertifikat in eine codierte Zeichenfolge. Die codierte Zeichenfolge kann in eine Datei geschrieben oder in ein neues [**Zertifikat**](certificate.md) Objekt importiert werden.

## <a name="syntax"></a>Syntax


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EncodingType* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, die den Codierungstyp für den Export Vorgang angibt. Der Standardwert ist **CAPICOM- \_ Codieren \_ Base64**. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Codieren \_ Any**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen. Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet. Eingeführt in CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ Codieren \_ Base64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Zeichenfolge, die das exportierte Zertifikat im angegebenen Codierungs Formular enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Stellt**](certificate.md)
</dt> </dl>

 

 
