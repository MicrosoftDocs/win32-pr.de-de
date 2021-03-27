---
title: 'Texture2D:: Load (int, int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | Texture2D:: Load (int, int, uint)-Funktion'
ms.assetid: 05A12BE2-4604-470B-9EE8-F03F51E6D254
keywords:
- Ladefunktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c591b92b64641e169023f30663d8f5c6ef8a6c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353259"
---
# <a name="texture2dloadintintuint-function"></a>Texture2D:: Load (int, int, uint)-Funktion

Liest Textur Daten und gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **int**

Texturkoordinaten

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Typ: **int**

Ein Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion. **Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ:

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture2D**](sm5-object-texture2d.md) -Objekt.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Lade Methoden](texture2d-load.md)
</dt> </dl>

 

 
