---
title: RWByteAddressBuffer::InterlockedMax-Funktion
description: Sucht den maximal zulässigen Wert atomisch.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
keywords:
- InterlockedMax-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ca02966843d74aa17c3f5292ee3edf868140ae5722c26f47ec0270722cbbae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790275"
---
# <a name="interlockedmax-function"></a>InterlockedMax-Funktion

Sucht den maximal zulässigen Wert atomisch.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedMax(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*dest* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Zieladresse.

</dd> <dt>

*value* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Eingabewert.

</dd> <dt>

*ursprünglicher \_ Wert* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der ursprüngliche Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Vorgang kann nur für int- und uint-typierte Ressourcen und Freigegebene Arbeitsspeichervariablen ausgeführt werden. Es gibt drei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für freigegebenen Arbeitsspeicher ist. In diesem Fall führt die Funktion einen atomaren Höchstwert des Werts für das Shared Memory-Register aus, auf das von dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion ein atomares Maximum des Werts für den Ressourcenspeicherort aus, auf den vom dest verwiesen wird. Schließlich ist das dritte Szenario, wenn R ein lokaler Variablentyp ist. In diesem Szenario wird die -Funktion auf einen Höchstwert von dest und value reduziert, der in dest gespeichert ist. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| VS  | Hs  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 