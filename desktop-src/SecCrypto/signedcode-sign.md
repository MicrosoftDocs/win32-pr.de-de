---
description: Erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der signedcode. FileName-Eigenschaft angegeben ist.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: Signedcode. Sign-Methode
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
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362050"
---
# <a name="signedcodesign-method"></a>Signedcode. Sign-Methode

\[Die **Sign** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Sign** -Methode erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der [**signedcode. filename**](signedcode-filename.md) -Eigenschaft angegeben ist.

## <a name="syntax"></a>Syntax


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Signatur Geber* \[ in, optional\]
</dt> <dd>

Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den privaten Schlüssel des Zertifikats hat, das zum Signieren des Codes verwendet wird. Der Standardwert ist **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bevor die **Sign** -Methode aufgerufen wird, muss die Datei, die den Code enthält, in der [**filename**](signedcode-filename.md) -Eigenschaft angegeben werden.

Wenn die ausführbare Datei bereits signiert ist, überschreibt diese Methode die vorhandene Signatur.

Die folgenden Ergebnisse gelten für den Parameterwert des *Signatur* Gebers:

-   Wenn der *Signatur* Geber Parameter nicht **null** ist, verwendet diese Methode den privaten Schlüssel, auf den das zugehörige Zertifikat zeigt, um die Signatur zu verschlüsseln. Wenn der private Schlüssel, auf den vom Zertifikat verwiesen wird, nicht verfügbar ist, schlägt die Methode fehl.
-   Wenn der *Signatur* Geber Parameter **null** ist und im aktuellen \_ Benutzer mein Speicher, der Zugriff auf einen privaten Schlüssel mit Code Signatur Funktion hat, genau ein Zertifikat vorhanden ist, wird dieses Zertifikat zum Erstellen der Signatur verwendet.
-   Wenn der *Signatur* Geber Parameter den Wert **null** hat, ist der Wert [**Settings. enablepromptforcertifigateeui**](settings-enablepromptforcertificateui.md) Property true, und es gibt mehrere Zertifikate im aktuellen \_ Benutzer My Store mit einem verfügbaren privaten Schlüssel mit Code Signatur Funktion. Daraufhin wird ein Dialogfeld angezeigt, in dem der Benutzer auswählen kann, welches Zertifikat verwendet wird.
-   Wenn der *Signatur* Geber Parameter den Wert **null** hat und die Eigenschaft [**Settings. enablepromptforcertifigateeui**](settings-enablepromptforcertificateui.md) den Wert false hat, schlägt die Methode fehl.
-   Wenn der *Signatur* Geber Parameter **null** ist und im aktuellen \_ Benutzer mein Speicher mit einem verfügbaren privaten Schlüssel mit Code Signatur Funktion keine Zertifikate vorhanden sind, schlägt die Methode fehl.

Diese Methode verwendet den SHA-1-Hash Algorithmus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
