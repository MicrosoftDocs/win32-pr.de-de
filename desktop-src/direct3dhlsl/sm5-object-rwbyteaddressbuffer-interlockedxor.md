---
title: 'Rwbyteaddressbuffer:: interlockedxor-Funktion'
description: Führt einen atomaren XOR-Wert für den Wert aus.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- Interlockedxor-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948762"
---
# <a name="interlockedxor-function"></a>Interlockedxor-Funktion

Führt einen atomaren **Xor** -Wert für den Wert aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedXor(
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

Dieser Vorgang kann nur für typisierte **int** -oder **uint** -Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt drei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion einen atomaren **Xor** -Wert mit dem Wert des freigegebenen Speicher Registers aus, auf das von *dest* verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die-Funktion einen atomaren **Xor** -Wert mit dem Wert des Ressourcen Speicher Orts aus, auf den " *dest*" verweist. Das dritte Szenario ist, dass R ein lokaler Variablentyp ist. In diesem Szenario wird die Funktion auf einen **Xor** -Wert der Werte " *dest* " und " *value*" reduziert. Das Ergebnis des Vorgangs ersetzt den Wert in *dest*. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von *dest* festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| VS  | Jh  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Rwbyteaddressbuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 