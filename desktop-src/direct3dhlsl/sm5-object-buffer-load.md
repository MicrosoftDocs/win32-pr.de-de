---
title: 'Buffer:: Load (int, uint)-Funktion'
description: 'Liest Puffer Daten und gibt den Status des Vorgangs zurück. | Buffer:: Load (int, uint)-Funktion'
ms.assetid: 0C7FC522-C962-4467-AA3E-6611064C188B
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
ms.openlocfilehash: eccd5c367e593559b6a719777dfd1535ae2d423a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981088"
---
# <a name="bufferloadint-uint-function"></a>Buffer:: Load (int, uint)-Funktion

Liest Puffer Daten und gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax

``` syntax
 Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **int**

Der Speicherort des Puffers.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion. **Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ:

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**buffer**](sm5-object-buffer.md) -Objekt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="examples"></a>Beispiele

Dieses Beispiel zeigt die Verwendung von **Load**:

``` syntax
Buffer<float4> myBuffer;
float loc;
uint status;
float4 myColor = myBuffer.Load( loc , status );
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Lade Methoden](buffer-load.md)
</dt> </dl>

 

 
