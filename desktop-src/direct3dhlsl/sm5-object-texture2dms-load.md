---
title: Texture2DMS::Load(int,int)-Funktion
description: Ruft einen Wert ab. | Texture2DMS::Load(int,int)-Funktion
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- DXGI der Load-Funktion
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0997a1bd30b4912864674015057fcafec227d90ad05b16b88fd3f05b671f155c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285728"
---
# <a name="texture2dmsloadintint-function"></a>Texture2DMS::Load(int,int)-Funktion

Ruft einen Wert ab.

## <a name="syntax"></a>Syntax

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*coord* \[ In\]
</dt> <dd>

Typ: **int2**

Die Eingabeposition.

</dd> <dt>

*sampleindex* \[ In\]
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Der Beispielindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **T**

Ein -Wert, dessen Typ mit dem Texturvorlagentyp übereinstimmt.

## <a name="remarks"></a>Hinweise

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Laden von Methoden](texture2dms-load.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
