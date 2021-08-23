---
title: RWByteAddressBuffer::Load4(uint,uint)-Funktion
description: Ruft vier Werte ab und gibt den Status des Vorgangs zurück.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
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
ms.openlocfilehash: 0f64fe84f17ee4cc1fed25b870b2142b474e753fa41e82cd0d385c9ef185ee9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672110"
---
# <a name="load4uintuint-function"></a>Load4(uint,uint)-Funktion

Ruft vier Werte ab und gibt den Status des Vorgangs zurück.

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

Die Position des Puffers.

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



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Load4-Methoden](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 