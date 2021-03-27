---
title: 'Rwbyteaddressbuffer:: interlockedcompareexchange-Funktion'
description: Vergleicht die Eingabe mit dem Vergleichswert und tauscht das Ergebnis atomarisch aus.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- Interlockedcompareexchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729144"
---
# <a name="interlockedcompareexchange-function"></a>Interlockedcompareexchange-Funktion

Vergleicht die Eingabe mit dem Vergleichswert und tauscht das Ergebnis atomarisch aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
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

*\_ Wert vergleichen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Vergleichswert.

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

Vergleicht atomisch den Wert von " *dest* " mit dem *Vergleichs \_ Wert*, speichert den Wert in " *dest* ", wenn die Werte entsprechen, und gibt den ursprünglichen Wert von " *dest* " im *ursprünglichen \_ Wert* zurück Dieser Vorgang kann nur für typisierte **int** -oder *uint* -Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt drei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von *dest* verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den " *dest*" verweist. Das dritte Szenario ist, dass R ein lokaler Variablentyp ist. In diesem Szenario wird die Funktion auf den Vorgang reduziert, der mit lokalen Vorgängen ausgeführt wird. Dieser Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

> [!Note]  
> Wenn Sie in einer [**for**](dx-graphics-hlsl-for.md) -oder [**while**](dx-graphics-hlsl-while.md) -Compute-Shader-Schleife **interlockedcompareexchange** aufrufen, müssen Sie für die ordnungsgemäße Kompilierung das Attribut " **\[ \_ UAV- \_ \] Bedingung zulassen** " in dieser Schleife verwenden.

 

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

 

 