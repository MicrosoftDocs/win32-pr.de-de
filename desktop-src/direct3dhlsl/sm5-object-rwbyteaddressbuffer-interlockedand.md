---
title: RWByteAddressBuffer::InterlockedAnd-Funktion
description: Gibt den Wert atomisch an.
ms.assetid: c4024be0-3884-4af9-8075-76774c7c6178
keywords:
- InterlockedAnd-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8117729543d13b8c5578fd38a829cc0dba2a4d2d77885d32de006f4afad59f24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725165"
---
# <a name="interlockedand-function"></a>InterlockedAnd-Funktion

Gibt den Wert atomisch an.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedAnd(
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

*wert* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Eingabewert.

</dd> <dt>

*Ursprünglicher \_ Wert* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der ursprüngliche Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Vorgang kann nur für int- oder uint-typisierte Ressourcen und Freigegebene Speichervariablen ausgeführt werden. Es gibt drei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für gemeinsam genutzten Arbeitsspeicher ist. In diesem Fall führt die Funktion einen atomaren und einen Wert für das Shared Memory-Register aus, auf das vom Dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion einen atomaren und einen Wert für den Ressourcenspeicherort aus, auf den vom Dest verwiesen wird. Schließlich ist das dritte Szenario, wenn R ein lokaler Variablentyp ist. In diesem Szenario wird die Funktion auf einen und den Wert von dest und value reduziert, die in dest gespeichert sind. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| VS  | Hs  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   |  x  | x   | x   | x   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 