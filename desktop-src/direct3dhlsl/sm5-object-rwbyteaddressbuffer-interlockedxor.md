---
title: RWByteAddressBuffer::InterlockedXor-Funktion
description: Führt einen atomaren XOR für den Wert aus.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- InterlockedXor-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b9e0c719bb72116ba84a33f46c81cf243773d4c66e5ff0997066e7228b19db1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905797"
---
# <a name="interlockedxor-function"></a>InterlockedXor-Funktion

Führt einen atomaren **XOR** für den Wert aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedXor(
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

Dieser Vorgang kann nur für **INT-** oder **UINT-typisierte** Ressourcen und Freigegebene Speichervariablen ausgeführt werden. Es gibt drei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für gemeinsam genutzten Arbeitsspeicher ist. In diesem Fall führt die Funktion ein atomares **XOR** mit dem Wert des Shared Memory-Registers aus, auf das vom *Dest* verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion einen atomaren **XOR** mit dem Wert des Ressourcenspeicherorts aus, auf den vom *Dest* verwiesen wird. Schließlich ist das dritte Szenario, wenn R ein lokaler Variablentyp ist. In diesem Szenario reduziert die Funktion auf einen **XOR** der Werte *dest* und *value*. Das Ergebnis des Vorgangs ersetzt den Wert in *dest*. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von *dest* festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und schreibbar ist.

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| VS  | Hs  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 