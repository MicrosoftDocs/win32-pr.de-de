---
description: Fügt einem angegebenen Hashobjekt Daten hinzu.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: A_SHAUpdate -Funktion (Sha.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 103438e3ef0747aa6170848398621b0246bd15366be4d1171ce5735942011007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101070"
---
# <a name="a_shaupdate-function"></a>Eine \_ SHAUpdate-Funktion

Fügt einem angegebenen Hashobjekt Daten hinzu.

## <a name="syntax"></a>Syntax


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kontext* \[ in, out\]
</dt> <dd>

Der SHA-Kontext.

</dd> <dt>

*Puffer* \[ out\]
</dt> <dd>

Die Hashtabelle.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Die Größe des Puffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion kann mehrmals aufgerufen werden, um den Hash für lange Datenströme oder diskontinuierlich datenströme zu berechnen. Die [**A \_ SHAFinal-Funktion**](a-shafinal.md) muss aufgerufen werden, bevor der Hashwert abgerufen wird.

Diese Funktion ähnelt SHAUpdate sehr, wird jedoch direkt aus der Bibliothek aufgerufen, anstatt über die Kryptografieinfrastruktur geroutet zu werden. Weitere Informationen finden Sie unter [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Bibliothek<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
