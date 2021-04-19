---
description: Gibt eine Zeichen folgen Darstellung der codierten Daten zurück.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Encodeddata. Format-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370281"
---
# <a name="encodeddataformat-method"></a>Encodeddata. Format-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**AsnEncodedData-Klasse**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Format** -Methode gibt eine Zeichen folgen Darstellung der codierten Daten zurück.

## <a name="syntax"></a>Syntax


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bmultilines* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob die zurückgegebene Zeichenfolge mehrere Zeilen enthält. **True** gibt an, dass die zurückgegebene Zeichenfolge mehrere Zeilen enthalten kann, die durch **vbCrLf** getrennt sind. Der Standardwert ist **False**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine lesbare Zeichenfolge, die die codierten Daten darstellt. Wenn CAPICOM die codierten Daten nicht versteht, wird eine hexadezimale Darstellung der Daten zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das Format der zurückgegebenen Zeichenfolge kann sich zwischen verschiedenen Versionen von CAPICOM ändern. Verlassen Sie sich nicht auf ein bestimmtes Format in Ihrer Anwendung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Encoddata**](encodeddata.md)
</dt> </dl>

 

 
