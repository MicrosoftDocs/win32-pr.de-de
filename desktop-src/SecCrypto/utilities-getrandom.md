---
description: Generiert eine sichere Zufallszahl unter Verwendung des Standard-Kryptografiedienstanbieters (CSP).
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Utilities. getrandom-Methode
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
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364955"
---
# <a name="utilitiesgetrandom-method"></a>Utilities. getrandom-Methode

\[Die **getrandom** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]

Die **getrandom** -Methode generiert mithilfe des Standard- [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) eine sichere Zufallszahl.

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

Die Länge (in Byte) der zu erstellenden Zufallszahl. Der Standardwert ist 8 Bytes.

</dd> <dt>

*EncodingType* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, die den Codierungstyp angibt, der für die generierte Zufallszahl verwendet werden soll. Der Standardwert ist CAPICOM- \_ \_ codierungsbinär. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Codieren \_ Any**</dt> </dl>          | Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen. Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet. Eingeführt in CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ Codieren \_ Base64**</dt> </dl> | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt> </dl> | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine nach dem Zufallsprinzip generierte Zahlen *Länge* mit der angegebenen Codierung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Versorgungsunternehmen**](utilities.md)
</dt> </dl>

 

 
