---
title: 'Byteaddressbuffer:: Load4 (uint, uint)-Funktion'
description: Ruft vier Werte und den Status des Vorgangs ab.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Load4-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab27ed9002562643ddf4df6b33efe9d8f0454d94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039014"
---
# <a name="load4uint-uint-function"></a>Load4 (uint, uint)-Funktion

Ruft vier Werte und den Status des Vorgangs ab.

## <a name="syntax"></a>Syntax

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **uint**

Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion. **Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint4**

Vier Werte.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load4-Methoden](byteaddressbuffer-load4.md)
</dt> <dt>

[**Byteaddressbuffer**](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 