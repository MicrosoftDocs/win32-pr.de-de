---
title: Texture2D::Load(int,int,uint)-Funktion
description: Liest Texturdaten und gibt den Status des Vorgangs zurück. | Texture2D::Load(int,int,uint)-Funktion
ms.assetid: 05A12BE2-4604-470B-9EE8-F03F51E6D254
keywords:
- Load-Funktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 890f49a0609367dcf91c91146f786568fdd83f0f207f7aa69d8dd7c4019b4d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507383"
---
# <a name="texture2dloadintintuint-function"></a>Texture2D::Load(int,int,uint)-Funktion

Liest Texturdaten und gibt den Status des Vorgangs zurück.

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

*Standort* \[ In\]
</dt> <dd>

Typ: **int**

Texturkoordinaten

</dd> <dt>

*Offset* \[ In\]
</dt> <dd>

Typ: **int**

Ein Offset, der vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die systeminterne [**CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE** zurück, wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte aus einer nicht zugeordneten Kachel stammen, gibt **CheckAccessFullyMapped** **FALSE** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ:

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture2D-Objekt.**](sm5-object-texture2d.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Laden von Methoden](texture2d-load.md)
</dt> </dl>

 

 
