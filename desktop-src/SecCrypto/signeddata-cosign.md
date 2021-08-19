---
description: Erstellt eine digitale Signatur für zuvor signierten Inhalt.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: SignedData.CoSign-Methode
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
ms.openlocfilehash: ed4feb55420ebf9d3bc43496fe3004a4d1b55e1ae8add4e3d5b40ec2ac4ba4ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973890"
---
# <a name="signeddatacosign-method"></a>SignedData.CoSign-Methode

\[Die **CoSign-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**Namespace System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **CoSign-Methode** erstellt eine [*digitale Signatur für*](../secgloss/d-gly.md) zuvor signierten Inhalt.

## <a name="syntax"></a>Syntax


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Signer* \[ in, optional\]
</dt> <dd>

Ein Verweis auf das [**Signer-Objekt**](signer.md) des Signers der Daten. Das **Signer-Objekt** muss Zugriff auf den privaten Schlüssel des Zertifikats haben, das zum Signieren verwendet wird. Dieser Parameter kann NULL **sein.** Weitere Informationen finden Sie unter Hinweise.

</dd> <dt>

*EncodingType* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ ENCODING \_ TYPE-Enumeration,**](capicom-encoding-type.md) der angibt, wie die signierten Daten codiert werden sollen. Der Standardwert ist CAPICOM \_ ENCODE \_ BASE64. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp haben. Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen CAPICOM \_ ENCODE \_ BASE64 verwendet. Eingeführt in CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_CAPICOM-CODIERUNG \_ BASE64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BINARY**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine Zeichenfolge zurück, die die codierten signierten Daten enthält.

Wenn diese Methode fehlschlägt, wird ein Fehler ausgelöst. Das **Err-Objekt** enthält zusätzliche Informationen zum Fehler.

## <a name="remarks"></a>Hinweise

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript Ihren privaten Schlüssel verwenden, [*um*](../secgloss/p-gly.md) eine digitale Signatur zu erstellen. Nicht vertrauenswürdigen Websites die Verwendung Ihres privaten Schlüssels zu erlauben, ist ein Sicherheitsrisiko. Ein Dialogfeld, in dem sie gefragt wird, ob die Website Ihren privaten Schlüssel verwenden kann, wird angezeigt, wenn diese Methode zum ersten Mal aufgerufen wird. Wenn Sie zulassen, dass das Skript Ihren privaten Schlüssel zum Erstellen einer digitalen Signatur verwendet und "Dieses Dialogfeld nicht mehr anzeigen" auswählt, wird das Dialogfeld nicht mehr für Skripts innerhalb dieser Domäne angezeigt, die Ihren privaten Schlüssel zum Erstellen einer digitalen Signatur verwenden. Skripts außerhalb dieser Domäne, die versuchen, Ihren privaten Schlüssel zum Erstellen einer digitalen Signatur zu verwenden, führen jedoch weiterhin dazu, dass dieses Dialogfeld angezeigt wird. Wenn Sie nicht zulassen, dass das Skript Ihren privaten Schlüssel verwendet und "Dieses Dialogfeld nicht mehr anzeigen" auswählt, wird Skripts innerhalb dieser Domäne automatisch die Möglichkeit verweigert, Ihren privaten Schlüssel zum Erstellen digitaler Signaturen zu verwenden.

 

Es ist nicht garantiert, dass sich Cosignierer in einer bestimmten Reihenfolge befinden.

Die folgenden Ergebnisse gelten für den *Signer-Parameterwert:*

-   Wenn der *Signer-Parameter* nicht **NULL ist,** verwendet diese Methode den privaten Schlüssel, auf den das zugeordnete Zertifikat verweist, um die Cosignatur zu verschlüsseln. Wenn der private Schlüssel, auf den das Zertifikat verweist, nicht verfügbar ist, schlägt die Methode fehl.
-   Wenn der *Signer-Parameter* **NULL ist** und genau ein Zertifikat im SPEICHER CURRENT USER MY enthalten ist, das Zugriff auf einen privaten Schlüssel hat, wird dieses Zertifikat zum Erstellen der \_ Cosignatur verwendet.
-   Wenn der *Signer-Parameter* **NULL ist,** wird [**Einstellungen. Der EnablePromptForCertificateUI-Eigenschaftswert**](settings-enablepromptforcertificateui.md) ist true, und es gibt mehrere Zertifikate im Speicher CURRENT USER MY mit einem verfügbaren privaten Schlüssel. Es wird ein Dialogfeld angezeigt, in dem der Benutzer auswählen kann, welches Zertifikat verwendet \_ wird.
-   Wenn der *Signer-Parameter* **NULL ist und** die [**Einstellungen. Die EnablePromptForCertificateUI-Eigenschaft**](settings-enablepromptforcertificateui.md) ist false, die Methode schlägt fehl.
-   Wenn der *Signer-Parameter* **NULL ist** und im SPEICHER CURRENT USER MY kein Zertifikat mit einem verfügbaren privaten Schlüssel vorhanden \_ ist, schlägt die Methode fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
