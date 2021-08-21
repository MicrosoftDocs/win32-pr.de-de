---
description: Erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der SignedCode.FileName-Eigenschaft angegeben ist.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: SignedCode.Sign-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3baf2b324177cf7a05c660d23d9e94cf19e044d47c5d02138047b51a96c3f272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974177"
---
# <a name="signedcodesign-method"></a>SignedCode.Sign-Methode

\[Die **Sign-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktionen [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) aufzurufen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) Die [Unterabschnitte .NET und CryptoAPI über P/Invoke: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.NET und CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Erweiterung der [.NET-Kryptografie mit CAPICOM und P/Invoke](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Sign-Methode** erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der [**SignedCode.FileName-Eigenschaft**](signedcode-filename.md) angegeben ist.

## <a name="syntax"></a>Syntax


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Signierer* \[ in, optional\]
</dt> <dd>

Ein [**Signer-Objekt,**](signer.md) das Zugriff auf den privaten Schlüssel des Zertifikats hat, das zum Signieren des Codes verwendet wird. Der Standardwert ist **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Bevor die **Sign-Methode** aufgerufen wird, muss die Datei, die den Code enthält, in der [**FileName-Eigenschaft**](signedcode-filename.md) angegeben werden.

Wenn die ausführbare Datei bereits signiert ist, überschreibt diese Methode die vorhandene Signatur.

Die folgenden Ergebnisse gelten für den *Signer-Parameterwert:*

-   Wenn der *Signer-Parameter* nicht **NULL** ist, verwendet diese Methode den privaten Schlüssel, auf den das zugeordnete Zertifikat zeigt, um die Signatur zu verschlüsseln. Wenn der private Schlüssel, auf den das Zertifikat verweist, nicht verfügbar ist, schlägt die -Methode fehl.
-   Wenn der *Signer-Parameter* **NULL** ist und genau ein Zertifikat im SPEICHER CURRENT USER MY vorhanden \_ ist, das Zugriff auf einen privaten Schlüssel mit Codesignaturfunktion hat, wird dieses Zertifikat zum Erstellen der Signatur verwendet.
-   Wenn der *Signer-Parameter* **NULL** ist, [**Einstellungen. Der EnablePromptForCertificateUI-Eigenschaftswert**](settings-enablepromptforcertificateui.md) ist true, und es gibt mehrere Zertifikate im Speicher CURRENT \_ USER MY mit einem verfügbaren privaten Schlüssel mit Codesignaturfunktion. Es wird ein Dialogfeld angezeigt, in dem der Benutzer auswählen kann, welches Zertifikat verwendet wird.
-   Wenn der *Signer-Parameter* **NULL** ist und der [**Einstellungen. Die EnablePromptForCertificateUI-Eigenschaft**](settings-enablepromptforcertificateui.md) ist false, die Methode schlägt fehl.
-   Wenn der *Signer-Parameter* **NULL** ist und im CURRENT USER MY-Speicher keine Zertifikate \_ mit einem verfügbaren privaten Schlüssel mit Codesignaturfunktion vorhanden sind, schlägt die -Methode fehl.

Diese Methode verwendet den SHA-1-Hashalgorithmus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
