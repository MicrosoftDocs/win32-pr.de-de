---
title: Texture2DArray::Load(int,int,uint)-Funktion
description: Liest Texturdaten und gibt den Status des Vorgangs zurück. | Texture2DArray::Load(int,int,uint)-Funktion
ms.assetid: 551EA931-6D24-478B-B741-3DD5B1E030E2
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
ms.openlocfilehash: 0907ddb4f5100ae6bffc81214ed0bed0d7857462e12c4625f179d6b769915569
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723585"
---
# <a name="texture2darrayloadintintuint-function"></a>Texture2DArray::Load(int,int,uint)-Funktion

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

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture2DArray-Objekt.**](sm5-object-texture2darray.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Laden von Methoden](texture2darray-load.md)
</dt> </dl>

 

 
