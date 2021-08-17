---
title: RWByteAddressBuffer::Load3(uint,uint)-Funktion
description: Ruft drei Werte ab und gibt den Status des Vorgangs zurück.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
keywords:
- Load3-Funktion HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91d4a90094d93705e17c9087583974ef8f9d76e1878cb0c5aa8dab21dc82e073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791222"
---
# <a name="load3uintuint-function"></a>Load3(uint,uint)-Funktion

Ruft drei Werte ab und gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
uint3 Load3(
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

Typ: **uint3**

Drei Werte.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load3-Methoden](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 