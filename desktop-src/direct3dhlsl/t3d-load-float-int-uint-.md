---
title: Texture3D::Load(int,int,uint)-Funktion
description: Liest Texturdaten und gibt den Status des Vorgangs zurück. | Texture3D::Load(int,int,uint)-Funktion
ms.assetid: 3F562ADB-225F-462B-A7AC-40797BBB632A
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
ms.openlocfilehash: 84f19f75c7765c409b67deb5d7115d2d699fecb6cb03e77cb9223f6af4a363e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506866"
---
# <a name="texture3dloadintintuint-function"></a>Texture3D::Load(int,int,uint)-Funktion

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

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die [**systeminterne CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE zurück,** wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource zugegriffen haben.](/windows/desktop/direct3d11/direct3d-11-2-features) Wenn Werte aus einer nicht zugeordneten Kachel übernommen wurden, gibt **CheckAccessFullyMapped** **FALSE zurück.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ:

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture3D-Objekt.**](sm5-object-texture3d.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Laden von Methoden](texture3d-load.md)
</dt> <dt>

[**Texture3D**](sm5-object-texture3d.md)
</dt> </dl>

 

 
