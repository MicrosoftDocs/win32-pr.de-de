---
title: Texture2DMS::Load(int,int,int,uint)-Funktion
description: Liest Texturdaten und gibt den Status des Vorgangs zurück. | Texture2DMS::Load(int,int,int,uint)-Funktion
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: cb15f420699a9b581a6ac6f498c5e7ff07437ea4371bf1c59b004af1f5a963cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506882"
---
# <a name="texture2dmsloadintintintuint-function"></a>Texture2DMS::Load(int,int,int,uint)-Funktion

Liest Texturdaten und gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Standort* \[ In\]
</dt> <dd>

Typ: **int2**

Texturkoordinaten

</dd> <dt>

*sampleindex* \[ In\]
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Der Beispielindex.

</dd> <dt>

*Offset* \[ In\]
</dt> <dd>

Typ: **int2**

Ein Offset, der vor dem Laden auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die systeminterne [**CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE** zurück, wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte aus einer nicht zugeordneten Kachel stammen, gibt **CheckAccessFullyMapped** **FALSE** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ:

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture2DMS-Objekt.**](sm5-object-texture2dms.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Laden von Methoden](texture2dms-load.md)
</dt> <dt>

[**Texture2DMS**](sm5-object-texture2dms.md)
</dt> </dl>

 

 
