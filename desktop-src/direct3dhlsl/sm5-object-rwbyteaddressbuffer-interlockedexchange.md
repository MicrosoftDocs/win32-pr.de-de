---
title: 'Rwbyteaddressbuffer:: interlockedexchange-Funktion'
description: Tauscht einen Wert atomarisch aus.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
keywords:
- Interlockedexchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993351"
---
# <a name="interlockedexchange-function"></a>Interlockedexchange-Funktion

Tauscht einen Wert atomarisch aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedExchange(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*dest* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Zieladresse.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Eingabewert.

</dd> <dt>

*ursprünglicher \_ Wert* ausgehend \[\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der ursprüngliche Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Vorgang kann nur für skalartypisierte Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt drei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den "dest" verweist. Das dritte Szenario ist, dass R ein lokaler Variablentyp ist. In diesem Szenario wird die Funktion auf den Vorgang reduziert, der mit lokalen Vorgängen ausgeführt wird. Dieser Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| VS  | Jh  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
|  x  |  x  |  x  |  x  | x   | x   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Rwbyteaddressbuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 