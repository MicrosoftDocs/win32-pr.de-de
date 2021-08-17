---
description: Kopiert ein Zertifikat in eine codierte Zeichenfolge.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: ICertificate2::Export-Methode
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
ms.openlocfilehash: f002be332097baa0ad0947367259d15f0657d276770682b709402e2f0a333290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771767"
---
# <a name="icertificate2export-method"></a>ICertificate2::Export-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Export-Methode** kopiert ein Zertifikat in eine codierte Zeichenfolge. Die codierte Zeichenfolge kann in eine Datei geschrieben oder in ein neues [**Certificate-Objekt**](certificate.md) importiert werden.

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

Ein Wert der [**CAPICOM \_ ENCODING \_ TYPE-Enumeration,**](capicom-encoding-type.md) der den Codierungstyp für den Exportvorgang angibt. Der Standardwert ist **CAPICOM \_ ENCODE \_ BASE64**. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen. Wenn dieser Wert zum Angeben des Codierungstyps der Ausgabe verwendet wird, wird stattdessen CAPICOM \_ ENCODE \_ BASE64 verwendet. Eingeführt in CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_CAPICOM-CODIERUNG \_ BASE64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_ \_ CAPICOM-CODIERUNGSBINÄRDATEI**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Zeichenfolge, die das exportierte Zertifikat im angegebenen Codierungsformular enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Zertifikat**](certificate.md)
</dt> </dl>

 

 
