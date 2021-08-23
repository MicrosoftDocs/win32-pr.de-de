---
description: Bestimmt, ob die Signaturen für signierte Daten im SignedData-Objekt gültig sind.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData.Verify-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ccda81fc3640d4d09f9644bdf0d84a18a68b743397e1578a5ad434349893e893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898974"
---
# <a name="signeddataverify-method"></a>SignedData.Verify-Methode

\[Die **Verify-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Verify-Methode** bestimmt, ob die [*Signaturen*](../secgloss/d-gly.md) für signierte Daten im [**SignedData-Objekt**](signeddata.md) gültig sind. Um eine Signatur zu überprüfen, wird der verschlüsselte [*Hash*](../secgloss/h-gly.md) des Inhalts mithilfe des öffentlichen Schlüssels des Signaturgebers aus dem Zertifikat des Signaturgebers entschlüsselt. Der entschlüsselte Hash wird mit einem neuen Hash des Dateninhalts verglichen. Eine Signatur ist gültig, wenn die Hashes übereinstimmen. Darüber hinaus erstellt diese Methode auch eine Zertifikatkette, um die Gültigkeit des Zertifikats zu bestimmen, das den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) bereitstellt, der zum Entschlüsseln des Hashs verwendet wird.

## <a name="syntax"></a>Syntax


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SignedMessage* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die die zu überprüfende signierte Nachricht enthält.

</dd> <dt>

*bDetached* \[ in, optional\]
</dt> <dd>

**True** gibt an, dass die zu signierten Daten getrennt werden. Das heißt, der signierte Inhalt ist nicht als Teil des signierten Objekts enthalten. Um die Signatur für getrennten Inhalt zu überprüfen, muss eine Anwendung über eine Kopie des ursprünglichen Inhalts verfügen. Getrennte Inhalte werden häufig verwendet, um die Größe eines über das Web zu sendenden signierten Objekts zu verringern, wenn der Empfänger der signierten Nachricht über eine ursprüngliche Kopie der signierten Daten verfügt. Der Standardwert ist **False**.

</dd> <dt>

*VerifyFlag* \[ in, optional\]
</dt> <dd>

Ein Wert der [CAPICOM \_ SIGNED DATA VERIFY \_ \_ \_ FLAG-Enumeration,](capicom-signed-data-verify-flag.md) der die Überprüfungsrichtlinie angibt. Der Standardwert ist CAPICOM \_ VERIFY \_ SIGNATURE AND \_ \_ CERTIFICATE. Mit diesem Wert werden sowohl die Gültigkeit des Zertifikats als auch die Gültigkeit der Signatur überprüft. Dieser Parameter kann festgelegt werden, um die Signatur und nicht das Zertifikat zu überprüfen. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                             | Bedeutung                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**CAPICOM– NUR SIGNATUR \_ ÜBERPRÜFEN \_ \_**</dt> </dl>                                   | Nur die Signatur wird überprüft.<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**CAPICOM \_ VERIFY \_ SIGNATURE \_ AND \_ CERTIFICATE**</dt> </dl> | Sowohl die Signatur als auch die Gültigkeit des Zertifikats, das zum Erstellen der Signatur verwendet wird, werden überprüft.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine Zeichenfolge zurück, die die codierten, signierten Daten enthält.

Wenn diese Methode fehlschlägt, wird ein Fehler ausgelöst. Das **Err-Objekt** enthält zusätzliche Informationen zum Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
