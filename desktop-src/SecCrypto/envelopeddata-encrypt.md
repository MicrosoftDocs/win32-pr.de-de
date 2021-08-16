---
description: Generiert einen Sitzungsschlüssel und verschlüsselt und umschlagt Daten.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData.Encrypt-Methode
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
ms.openlocfilehash: df4741538ae11dbe1b158fd9b8e8a6c8632c427f9a0e8376e8cd10c9056461fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766086"
---
# <a name="envelopeddataencrypt-method"></a>EnvelopedData.Encrypt-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Encrypt-Methode** generiert einen Sitzungsschlüssel, verwendet diesen Schlüssel, um den Inhalt zu verschlüsseln, um den verschlüsselten Inhalt für jeden Empfänger einzukapseln, indem der Sitzungsschlüssel mit dem öffentlichen Schlüssel jedes Empfängers verschlüsselt wird, und gibt dann das [*BLOB*](../secgloss/b-gly.md) zurück, das den verschlüsselten Inhalt und die verschlüsselten Sitzungsschlüssel als codierte Zeichenfolge enthält.

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

Ein Wert der [**CAPICOM \_ ENCODING \_ TYPE-Enumeration,**](capicom-encoding-type.md) der den Codierungstyp angibt, der zum Codieren der umschlagten Daten verwendet wird. Der Standardcodierungswert ist CAPICOM \_ ENCODE \_ BASE64. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen. Wenn dieser Wert zum Angeben des Codierungstyps der Ausgabe verwendet wird, wird stattdessen CAPICOM \_ ENCODE \_ BASE64 verwendet. Eingeführt in CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_CAPICOM-CODIERUNG \_ BASE64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_ \_ CAPICOM-CODIERUNGSBINÄRDATEI**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein BLOB zurück, das die umschlagten Daten in einer codierten Zeichenfolge enthält.

## <a name="remarks"></a>Hinweise

Das zurückgegebene BLOB enthält den verschlüsselten Inhalt und einen verschlüsselten Sitzungsschlüssel für jeden vorgesehenen Empfänger. Diese Sitzungsschlüssel werden mit dem öffentlichen Schlüssel jedes Empfängers verschlüsselt. Die verschlüsselten Sitzungsschlüssel können nur mit dem privaten Schlüssel eines Empfängers entschlüsselt werden.

Wenn die [**Recipients-Eigenschaft**](envelopeddata-recipients.md) keine Informationen enthält, durchsucht diese Methode den AddressBook-Zertifikatspeicher des aktuellen Benutzers nach potenziellen Empfängern. Wenn mehrere potenzielle Empfänger gefunden werden, wird der Benutzer in einem Auswahldialogfeld aufgefordert, einen Empfänger auszuwählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
