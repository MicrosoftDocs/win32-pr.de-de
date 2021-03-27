---
title: 'Rwbyteaddressbuffer:: interlockedand-Funktion'
description: Stellt den Wert atomarisch dar.
ms.assetid: c4024be0-3884-4af9-8075-76774c7c6178
keywords:
- Interlockedand-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a389da886b193815c7d4b2c1fe0a86db1f068fc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390498"
---
# <a name="interlockedand-function"></a>Interlockedand-Funktion

Stellt den Wert atomarisch dar.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedAnd(
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

Dieser Vorgang kann nur für typisierte int-oder uint-Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt drei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion eine atomarische und einen Wert für das Shared Memory-Register aus, auf das von dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die Funktion eine atomarische und von einem Wert für den Ressourcen Speicherort aus, auf den von dest verwiesen wird. Das dritte Szenario ist, dass R ein lokaler Variablentyp ist. In diesem Szenario wird die-Funktion auf einen und den Wert von dest und Value reduziert, der in dest gespeichert ist. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| VS  | Jh  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   |  x  | x   | x   | x   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Rwbyteaddressbuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 