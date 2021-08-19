---
title: RWByteAddressBuffer::InterlockedOr-Funktion
description: Führt ein atomares OR für den Wert aus.
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
keywords:
- InterlockedOr-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07bcaf2ac9d5523949809b22b37f6a31bee1e7ef4243cfef52b1b034ee2e0cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986010"
---
# <a name="interlockedor-function"></a>InterlockedOr-Funktion

Führt ein **atomares OR für** den Wert aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedOr(
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

Nichts

## <a name="remarks"></a>Hinweise

Dieser Vorgang kann nur für **InT-** oder **UINT-Typressourcen** und Freigegebene Arbeitsspeichervariablen ausgeführt werden. Es gibt drei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für freigegebenen Arbeitsspeicher ist. In diesem Fall führt die Funktion ein atomares **OR** mit dem Wert des Shared Memory-Registers aus, auf das *von dest verwiesen wird.* Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion ein atomares **OR** mit dem Wert des Ressourcenspeicherorts aus, auf den *von dest verwiesen wird.* Schließlich ist das dritte Szenario, wenn R ein lokaler Variablentyp ist. In diesem Szenario reduziert die Funktion auf ein **OR** mit den Werten *dest* und *value*. Das Ergebnis des Vorgangs ersetzt den Wert von *dest.* Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von *dest festgelegt wird.* Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und schreibbar ist.

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

 

 