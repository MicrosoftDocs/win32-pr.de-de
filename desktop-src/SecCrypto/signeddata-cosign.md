---
description: Erstellt eine digitale Signatur für zuvor signierten Inhalt.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: SignedData. cosign-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352125"
---
# <a name="signeddatacosign-method"></a>SignedData. cosign-Methode

\[Die Methode " **cosign** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die Methode " **cosign** " erstellt eine [*digitale Signatur*](../secgloss/d-gly.md) für zuvor signierten Inhalt.

## <a name="syntax"></a>Syntax


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Signatur Geber* \[ in, optional\]
</dt> <dd>

Ein Verweis auf das [**Signatur**](signer.md) Geber Objekt des Signatur Gebers der Daten. Das **Signatur** Geber Objekt muss Zugriff auf den privaten Schlüssel des Zertifikats haben, das zum Signieren verwendet wird. Dieser Parameter kann **null** sein. Weitere Informationen finden Sie unter "Hinweise".

</dd> <dt>

*EncodingType* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, der angibt, wie die signierten Daten codiert werden sollen. Der Standardwert ist CAPICOM- \_ Codieren \_ Base64. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Codieren \_ Any**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen. Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet. Eingeführt in CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ Codieren \_ Base64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine Zeichenfolge zurück, die die codierten, signierten Daten enthält.

Wenn diese Methode fehlschlägt, wird ein Fehler ausgelöst. Das **Err** -Objekt enthält zusätzliche Informationen über den Fehler.

## <a name="remarks"></a>Bemerkungen

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript den [*privaten Schlüssel*](../secgloss/p-gly.md) verwenden, um eine digitale Signatur zu erstellen. Es ist ein Sicherheitsrisiko, nicht vertrauenswürdige Websites den privaten Schlüssel zu verwenden. Wenn diese Methode erstmals aufgerufen wird, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob die Website den privaten Schlüssel verwenden kann. Wenn Sie zulassen, dass das Skript den privaten Schlüssel zum Erstellen einer digitalen Signatur verwendet, und wählen Sie "dieses Dialogfeld nicht mehr anzeigen" aus, wird das Dialogfeld nicht mehr für ein Skript in dieser Domäne angezeigt, das den privaten Schlüssel verwendet, um eine digitale Signatur zu erstellen. Skripts außerhalb dieser Domäne, die versuchen, den privaten Schlüssel zum Erstellen einer digitalen Signatur zu verwenden, führen jedoch weiterhin dazu, dass dieses Dialogfeld angezeigt wird. Wenn Sie das Skript nicht für die Verwendung Ihres privaten Schlüssels zulassen und das Kontrollkästchen Dieses Dialogfeld nicht mehr anzeigen aktivieren, wird die Möglichkeit der Verwendung Ihres privaten Schlüssels für die Erstellung digitaler Signaturen automatisch verweigert.

 

Es ist nicht gewährleistet, dass die cosigner in einer bestimmten Reihenfolge vorliegen.

Die folgenden Ergebnisse gelten für den Parameterwert des *Signatur* Gebers:

-   Wenn der *Signatur* Geber Parameter nicht **null** ist, verwendet diese Methode den privaten Schlüssel, auf den das zugehörige Zertifikat zeigt, um die cosignatur zu verschlüsseln. Wenn der private Schlüssel, auf den vom Zertifikat verwiesen wird, nicht verfügbar ist, schlägt die Methode fehl.
-   Wenn der *Signatur* Geber Parameter **null** ist und im Speicher des aktuellen Benutzers genau ein Zertifikat vorhanden ist, \_ das Zugriff auf einen privaten Schlüssel hat, wird dieses Zertifikat verwendet, um die cosignatur zu erstellen.
-   Wenn der *Signatur* Geber Parameter den Wert **null** hat, lautet der Wert [**Settings. enablepromptforcertifisineui**](settings-enablepromptforcertificateui.md) Property auf true, und es gibt mehr als ein Zertifikat im aktuellen \_ Benutzer My Store mit einem verfügbaren privaten Schlüssel. Daraufhin wird ein Dialogfeld angezeigt, in dem der Benutzer auswählen kann, welches Zertifikat verwendet wird.
-   Wenn der *Signatur* Geber Parameter den Wert **null** hat und die Eigenschaft [**Settings. enablepromptforcertifigateeui**](settings-enablepromptforcertificateui.md) den Wert false hat, schlägt die Methode fehl.
-   Wenn der *Signatur* Geber Parameter **null** ist und im aktuellen \_ Benutzer mein Speicher mit einem verfügbaren privaten Schlüssel kein Zertifikat vorhanden ist, schlägt die Methode fehl.

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

 

 
