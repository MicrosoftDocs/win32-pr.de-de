---
description: Berechnet den endgültigen Hash der von der MD5Update-Funktion eingegebenen Daten.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: A_SHAFinal -Funktion (Sha.h)
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
ms.openlocfilehash: 42a22cfca32409fdfa02586bb90c76f8e8f2489b22cfe2769b50d928d2564af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960289"
---
# <a name="a_shafinal-function"></a>Eine \_ SHAFinal-Funktion

Berechnet den endgültigen Hash der von der MD5Update-Funktion eingegebenen Daten.

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

*Ergebnis* \[ out\]
</dt> <dd>

Die resultierende Hashtabelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion ähnelt SHAFinal sehr, wird jedoch direkt aus der Bibliothek aufgerufen, anstatt über die Kryptografieinfrastruktur geroutet zu werden. Weitere Informationen finden Sie unter [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Bibliothek<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
