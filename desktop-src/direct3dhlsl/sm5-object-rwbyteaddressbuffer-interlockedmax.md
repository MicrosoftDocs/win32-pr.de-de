---
title: 'Rwbyteaddressbuffer:: interlockedmax-Funktion'
description: Findet atomisch den maximalen Wert.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
keywords:
- Interlockedmax-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e77f925a0950d3731af58c2c6835867640760371
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993463"
---
# <a name="interlockedmax-function"></a>Interlockedmax-Funktion

Findet atomisch den maximalen Wert.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedMax(
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

Dieser Vorgang kann nur für typisierte int-und uint-Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt drei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion einen atomaren Maximalwert des Werts für das Shared Memory-Register aus, auf das von dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die Funktion einen atomaren Maximalwert des Werts für den Ressourcen Speicherort aus, auf den "dest" verweist. Das dritte Szenario ist, dass R ein lokaler Variablentyp ist. In diesem Szenario verringert die-Funktion den Höchstwert von "dest" und "Value", der in dest gespeichert ist. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| VS  | Jh  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Rwbyteaddressbuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 