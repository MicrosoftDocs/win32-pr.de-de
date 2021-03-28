---
title: 'Consumestructuredbuffer:: consumerfunktion'
description: Entfernt einen Wert vom Ende des Puffers.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Funktions-HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104038235"
---
# <a name="consume-function"></a>Funktion verarbeiten

Entfernt einen Wert vom Ende des Puffers.

## <a name="syntax"></a>Syntax

``` syntax
T Consume(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **T**

Der entfernte Wert (kann eine Struktur sein).

## <a name="remarks"></a>Bemerkungen

"T" kann ein beliebiger Datentyp sein, einschließlich einer Struktur.

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Consumestructuredbuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




