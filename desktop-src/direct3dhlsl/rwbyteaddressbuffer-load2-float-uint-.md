---
title: 'Rwbyteaddressbuffer:: Load2 (uint, uint)-Funktion'
description: Ruft zwei Werte ab und gibt den Status des Vorgangs zurück.
ms.assetid: E6BBA8A7-D53F-4718-B007-EBDE50FADB06
keywords:
- Load2-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92fc492fddb6ad024a4507829e81dab4886af590
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101655"
---
# <a name="load2uintuint-function"></a>Load2 (uint, uint)-Funktion

Ruft zwei Werte ab und gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **uint**

Der Speicherort des Puffers.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion. **Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint2**

Zwei-Werte.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load2-Methoden](rwbyteaddressbuffer-load2.md)
</dt> </dl>

 

 