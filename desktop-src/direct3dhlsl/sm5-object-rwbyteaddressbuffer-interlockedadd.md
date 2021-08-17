---
title: RWByteAddressBuffer::InterlockedAdd-Funktion
description: Fügt den Wert atomar hinzu.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- InterlockedAdd-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fb2f9dd6b2e42cb8f63a7c77186386c7cff06e9008a5b45cc7e95a7d9c0e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790295"
---
# <a name="interlockedadd-function"></a>InterlockedAdd-Funktion

Fügt den Wert atomar hinzu.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedAdd(
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

Dieser Vorgang kann nur für int- oder uint-typisierte Ressourcen und Freigegebene Arbeitsspeichervariablen ausgeführt werden. Es gibt drei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für gemeinsam genutzten Arbeitsspeicher ist. In diesem Fall führt die Funktion eine atomare Add-of-Value-Funktion zum Shared Memory-Register aus, auf das vom Dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion eine atomare Hinzufügefunktion des Werts zum Ressourcenspeicherort aus, auf den vom Dest verwiesen wird. Schließlich ist das dritte Szenario, wenn R ein lokaler Variablentyp ist. In diesem Szenario reduziert sich die Funktion auf eine Summe aus dem Wert dest und dem Wert, der in dest gespeichert ist. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| VS  | Hs  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="requirements"></a>Anforderungen




## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

