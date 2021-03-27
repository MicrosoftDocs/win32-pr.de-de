---
title: 'Rwbyteaddressbuffer:: interlockedcomparestore-Funktion'
description: Vergleicht die Eingabe atomarisch mit dem Vergleichswert.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- Interlockedcomparestore-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858387"
---
# <a name="interlockedcomparestore-function"></a>Interlockedcomparestore-Funktion

Vergleicht die Eingabe atomarisch mit dem Vergleichswert.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*dest* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Zieladresse.

</dd> <dt>

*\_ Wert vergleichen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Vergleichswert.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Vorgang kann nur für typisierte int-oder uint-Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt drei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den "dest" verweist. Das dritte Szenario ist, dass R ein lokaler Variablentyp ist. In diesem Szenario wird die Funktion auf den Vorgang reduziert, der mit lokalen Vorgängen ausgeführt wird.

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

 

 