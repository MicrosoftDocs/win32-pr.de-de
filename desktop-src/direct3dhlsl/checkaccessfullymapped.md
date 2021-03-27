---
title: Checkaccessfullymapping-Funktion
description: Bestimmt, ob alle Werte aus einem Sample-, Gather-oder LOAD-Vorgang auf zugeordnete Kacheln in einer gekachelten Ressource zugreifen.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- Checkaccessfullymapping-Funktion HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729369"
---
# <a name="checkaccessfullymapped-function"></a>Checkaccessfullymapping-Funktion

Bestimmt, ob alle Werte aus einem **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugreifen.

## <a name="syntax"></a>Syntax

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ in\]
</dt> <dd>

Typ: **\_ nur uint**

Der Statuswert, der von einem **Sample**-, **Gather**-oder **Load** -Vorgang zurückgegeben wird. Da Sie nicht direkt auf diesen Statuswert zugreifen können, müssen Sie ihn an **checkaccessfullymapping** übergeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Gibt einen **booleschen** Wert zurück, der angibt, ob alle Werte aus einem **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugreifen. Gibt **true** zurück, wenn alle Werte aus dem Vorgang auf zugeordnete Kacheln zugegriffen haben. Andernfalls wird **false** zurückgegeben, wenn Werte von einer nicht zugeordneten Kachel entnommen wurden.

## <a name="remarks"></a>Bemerkungen

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 