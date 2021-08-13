---
title: ByteAddressBuffer::Load4(uint, uint)-Funktion
description: Ruft vier Werte und den Status des Vorgangs ab.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Load4-Funktion HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9e65738acfa8a795dc1431bc3c6bb6242d810227bcdc40abcc8cfdf43dea934
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790378"
---
# <a name="load4uint-uint-function"></a>Load4(uint, uint)-Funktion

Ruft vier Werte und den Status des Vorgangs ab.

## <a name="syntax"></a>Syntax

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Standort* \[ In\]
</dt> <dd>

Typ: **uint**

Die Eingabeadresse in Bytes, die ein Vielfaches von 4 sein muss.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die systeminterne [**CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE** zurück, wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte aus einer nicht zugeordneten Kachel stammen, gibt **CheckAccessFullyMapped** **FALSE** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint4**

Vier Werte.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load4-Methoden](byteaddressbuffer-load4.md)
</dt> <dt>

[**ByteAddressBuffer**](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 