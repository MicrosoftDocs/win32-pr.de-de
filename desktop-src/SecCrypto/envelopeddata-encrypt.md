---
description: Generiert einen Sitzungsschlüssel und verschlüsselt und umschließt Daten.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData. Verschlüsseln-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373725"
---
# <a name="envelopeddataencrypt-method"></a>EnvelopedData. Verschlüsseln-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die Methode " **verschlüsseln** " generiert einen Sitzungsschlüssel, verwendet diesen Schlüssel zum Verschlüsseln des Inhalts, gibt den verschlüsselten Inhalt für jeden Empfänger ein, indem er den Sitzungsschlüssel mit dem öffentlichen Schlüssel jedes Empfängers verschlüsselt und dann das [*BLOB*](../secgloss/b-gly.md) zurückgibt, das den verschlüsselten Inhalt und die verschlüsselten Sitzungsschlüssel als codierte Zeichenfolge enthält.

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EncodingType* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, der den Codierungstyp angibt, der zum Codieren der eingeschlossenen Daten verwendet wird. Der Standard Codierungs Wert ist CAPICOM- \_ Codieren \_ Base64. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Codieren \_ Any**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen. Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet. Eingeführt in CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ Codieren \_ Base64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein BLOB zurück, das die eingeschlossenen Daten in einer codierten Zeichenfolge enthält.

## <a name="remarks"></a>Bemerkungen

Das zurückgegebene BLOB enthält den verschlüsselten Inhalt und einen verschlüsselten Sitzungsschlüssel für jeden vorgesehenen Empfänger. Diese Sitzungsschlüssel werden mit dem öffentlichen Schlüssel der einzelnen Empfänger verschlüsselt. Die verschlüsselten Sitzungsschlüssel können nur mit dem privaten Schlüssel eines Empfängers entschlüsselt werden.

Wenn die Eigenschaft " [**Empfänger**](envelopeddata-recipients.md) " keine Informationen enthält, durchsucht diese Methode den addressbook-Zertifikat Speicher des aktuellen Benutzers nach möglichen Empfängern. Wenn mehr als ein potenzieller Empfänger gefunden wird, wird der Benutzer aufgefordert, im Dialogfeld Auswahl einen Empfänger auszuwählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
