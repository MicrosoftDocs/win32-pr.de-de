---
description: Generiert eine sichere Zufallszahl mithilfe des standardmäßigen Kryptografiedienstanbieters (Cryptographic Service Provider, CSP).
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Utilities.GetRandom-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 973d34c77dfed1493ac85fe2a98ed2c2e5dc5ef6f9b9007076fbf732e40c10e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971031"
---
# <a name="utilitiesgetrandom-method"></a>Utilities.GetRandom-Methode

\[Die **GetRandom-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar.\]

Die **GetRandom-Methode** generiert mithilfe des Standardmäßigen [*Kryptografiedienstanbieters (CSP)*](../secgloss/c-gly.md) eine sichere Zufallszahl.

## <a name="syntax"></a>Syntax


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Länge* \[ in, optional\]
</dt> <dd>

Die Länge der zu erstellende Zufallszahl in Bytes. Der Standardwert ist 8 Byte.

</dd> <dt>

*EncodingType* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ ENCODING \_ TYPE-Enumeration,**](capicom-encoding-type.md) der den Typ der Codierung angibt, der für die generierte Zufallszahl verwendet werden soll. Der Standardwert ist CAPICOM \_ ENCODE \_ BINARY. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen. Wenn dieser Wert zum Angeben des Codierungstyps der Ausgabe verwendet wird, wird stattdessen CAPICOM \_ ENCODE \_ BASE64 verwendet. Eingeführt in CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_CAPICOM-CODIERUNG \_ BASE64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_ \_ CAPICOM-CODIERUNGSBINÄRDATEI**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine zufällig generierte Anzahl *von Längenbytes* mit der angegebenen Codierung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hilfsprogramme**](utilities.md)
</dt> </dl>

 

 
