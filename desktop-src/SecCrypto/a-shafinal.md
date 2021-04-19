---
description: Berechnet den abschließenden Hash der Daten, die von der MD5Update-Funktion eingegeben werden.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: A_SHAFinal-Funktion (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369937"
---
# <a name="a_shafinal-function"></a>Eine " \_ shafinal"-Funktion

Berechnet den abschließenden Hash der Daten, die von der MD5Update-Funktion eingegeben werden.

## <a name="syntax"></a>Syntax


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kontext* \[ in, out\]
</dt> <dd>

Der SHA-Kontext.

</dd> <dt>

*Ergebnis* \[ vorgenommen\]
</dt> <dd>

Die resultierende Hash Tabelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ähnelt der Verwendung von "shafinal", wird aber direkt aus der Bibliothek aufgerufen, anstatt durch die kryptografieinfrastruktur weitergeleitet zu werden. Weitere Informationen finden Sie unter [Windows-ntkryptografieanbieter](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Bibliothek<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
