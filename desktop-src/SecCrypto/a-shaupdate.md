---
description: Fügt einem angegebenen Hash Objektdaten hinzu.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: A_SHAUpdate-Funktion (SHA. h)
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
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358225"
---
# <a name="a_shaupdate-function"></a>Eine \_ shaupdate-Funktion

Fügt einem angegebenen Hash Objektdaten hinzu.

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

*Puffer* \[ vorgenommen\]
</dt> <dd>

Die Hash Tabelle.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Die Größe des Puffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann mehrmals aufgerufen werden, um den Hash für lange Datenströme oder diskontinuierliche Datenströme zu berechnen. Vor dem Abrufen des Hashwerts muss vor dem Abrufen des Hashwerts die Funktion "- [**\_ Wellen**](a-shafinal.md) " aufgerufen werden.

Diese Funktion ähnelt von "shaupdate", wird aber direkt aus der Bibliothek aufgerufen, anstatt durch die kryptografieinfrastruktur weitergeleitet zu werden. Weitere Informationen finden Sie unter [Windows-ntkryptografieanbieter](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Bibliothek<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
