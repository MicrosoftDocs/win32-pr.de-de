---
title: CheckAccessFullyMapped-Funktion
description: Bestimmt, ob alle Werte aus einem Sample-, Gather- oder Load-Vorgang auf zugeordnete Kacheln in einer gekachelten Ressource zugegriffen haben.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- CheckAccessFullyMapped-Funktion HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e7241fa5546edffb2b7c5ff36d2e43919e6d0b6fef9ff617c0fb63a674ffee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516673"
---
# <a name="checkaccessfullymapped-function"></a>CheckAccessFullyMapped-Funktion

Bestimmt, ob alle Werte aus einem **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [kachelgekachelten Ressource zugegriffen haben.](/windows/desktop/direct3d11/direct3d-11-2-features)

## <a name="syntax"></a>Syntax

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ In\]
</dt> <dd>

Typ: **nur \_ uint**

Der Statuswert, der von einem **Sample-,** **Gather- oder** **Load-Vorgang zurückgegeben** wird. Da Sie nicht direkt auf diesen Statuswert zugreifen können, müssen Sie ihn an **CheckAccessFullyMapped übergeben.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Gibt einen **booleschen Wert** zurück, der angibt, ob alle Werte aus einem **Sample-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource zugegriffen haben.](/windows/desktop/direct3d11/direct3d-11-2-features) Gibt **TRUE zurück,** wenn auf alle Werte des Vorgangs zugegriffen wird, auf die zugeordnete Kacheln zugegriffen haben. andernfalls gibt **FALSE zurück,** wenn Werte aus einer nicht zugeordneten Kachel übernommen wurden.

## <a name="remarks"></a>Hinweise

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher – Shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 