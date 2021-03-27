---
title: 'Texture2DMSArray:: Load (int, int)-Funktion'
description: 'Ruft einen Wert ab. | Texture2DMSArray:: Load (int, int)-Funktion'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Ladefunktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961497"
---
# <a name="texture2dmsarrayloadintint-function"></a>Texture2DMSArray:: Load (int, int)-Funktion

Ruft einen Wert ab.

## <a name="syntax"></a>Syntax

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Koord* \[ in\]
</dt> <dd>

Typ: **int3**

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
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Lade Methoden](texture2dmsarray-load.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
