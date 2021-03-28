---
title: 'RWTexture2D:: Load (int)-Funktion'
description: 'Liest Textur Daten. | RWTexture2D:: Load (int)-Funktion'
ms.assetid: AEBB9C78-BE4B-4121-93CC-EE03B9925CF0
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
ms.openlocfilehash: ab5f8d755ad4af3127a0c238defc9f1c422061bc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995566"
---
# <a name="rwtexture2dloadint-function"></a>RWTexture2D:: Load (int)-Funktion

Liest Textur Daten.

## <a name="syntax"></a>Syntax


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **int**

Der Speicherort der Textur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ:

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture2D**](sm5-object-rwtexture2d.md) -Objekt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Lade Methoden](rwtexture2d-load.md)
</dt> </dl>

 

 




