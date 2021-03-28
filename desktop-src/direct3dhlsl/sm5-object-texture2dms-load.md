---
title: 'Texture2DMS:: Load (int, int)-Funktion'
description: 'Ruft einen Wert ab. | Texture2DMS:: Load (int, int)-Funktion'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Load-Funktion DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981592"
---
# <a name="texture2dmsloadintint-function"></a>Texture2DMS:: Load (int, int)-Funktion

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

*Koord* \[ in\]
</dt> <dd>

Typ: **int2**

Der Eingabe Speicherort.

</dd> <dt>

*sampleingedex* \[ in\]
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Der Beispiel Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **T**

Ein-Wert, dessen Typ mit dem Typ der Textur Vorlage übereinstimmt.

## <a name="remarks"></a>Bemerkungen

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Lade Methoden](texture2dms-load.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
