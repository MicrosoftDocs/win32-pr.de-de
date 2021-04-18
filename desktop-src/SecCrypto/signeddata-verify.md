---
description: Bestimmt, ob die Signaturen für signierte Daten im SignedData-Objekt gültig sind.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData. Verify-Methode
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
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364817"
---
# <a name="signeddataverify-method"></a>SignedData. Verify-Methode

\[Die **Verifizierungs** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Verify** -Methode bestimmt, ob die [*Signaturen*](../secgloss/d-gly.md) für signierte Daten im [**SignedData**](signeddata.md) -Objekt gültig sind. Um eine Signatur zu überprüfen, wird der verschlüsselte [*Hash*](../secgloss/h-gly.md) der Inhalte mithilfe des öffentlichen Schlüssels des Signatur Gebers aus dem Zertifikat des Signatur Gebers entschlüsselt. Der entschlüsselte Hash wird mit einem neuen Hash des Daten Inhalts verglichen. Eine Signatur ist gültig, wenn die Hashwerte entsprechen. Außerdem wird mit dieser Methode auch eine Zertifikat Kette erstellt, um die Gültigkeit des Zertifikats zu bestimmen, das den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) zum Entschlüsseln des Hashs bereitstellt.

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

*Signedmessage* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die signierte Meldung enthält, die überprüft werden soll.

</dd> <dt>

*bgetrennte* \[ in, optional\]
</dt> <dd>

**True** gibt an, dass die zu Signier enden Daten getrennt sind. Das heißt, der signierte Inhalt ist nicht als Teil des signierten Objekts enthalten. Zum Überprüfen der Signatur bei getrennter Inhalte muss eine Anwendung über eine Kopie des ursprünglichen Inhalts verfügen. Getrennter Inhalt wird häufig verwendet, um die Größe eines signierten Objekts zu verringern, das über das Internet gesendet werden soll, wenn der Empfänger der signierten Nachricht über eine ursprüngliche Kopie der signierten Daten verfügt. Der Standardwert ist **False**.

</dd> <dt>

*Verifyflag* \[ in, optional\]
</dt> <dd>

Ein Wert der [CAPICOM- \_ \_ \_ \_ Flag für signierte Daten](capicom-signed-data-verify-flag.md) Überprüfung, der die Überprüfungs Richtlinie angibt. Der Standardwert ist CAPICOM \_ Verify \_ Signature \_ und \_ Certificate. Wenn Sie diesen Wert verwenden, werden sowohl die Gültigkeit des Zertifikats als auch die Gültigkeit der Signatur überprüft. Dieser Parameter kann festgelegt werden, um die Signatur und nicht das Zertifikat zu überprüfen. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                             | Bedeutung                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**nur CAPICOM- \_ Signatur überprüfen \_ \_**</dt> </dl>                                   | Nur die Signatur wird geprüft.<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**CAPICOM \_ \_ -Signatur \_ und \_ Zertifikat überprüfen**</dt> </dl> | Sowohl die Signatur als auch die Gültigkeit des Zertifikats, das zum Erstellen der Signatur verwendet wird, werden überprüft.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine Zeichenfolge zurück, die die codierten, signierten Daten enthält.

Wenn diese Methode fehlschlägt, wird ein Fehler ausgelöst. Das **Err** -Objekt enthält zusätzliche Informationen über den Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
