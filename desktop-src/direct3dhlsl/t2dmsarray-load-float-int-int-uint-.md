---
title: Texture2DMSArray::Load(int,int,int,uint)-Funktion
description: Liest Texturdaten und gibt den Status des Vorgangs zurück. | Texture2DMSArray::Load(int,int,int,uint)-Funktion
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: c237de43a52650af1d365a6b95c47f51f525b698152b0be0adf2ffe83f15c1fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506878"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a>Texture2DMSArray::Load(int,int,int,uint)-Funktion

Liest Texturdaten und gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
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

*sampleindex* \[ In\]
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Der Beispielindex.

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

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture2DMSArray-Objekt.**](sm5-object-texture2dmsarray.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Laden von Methoden](texture2dmsarray-load.md)
</dt> <dt>

[**Texture2DMSArray**](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
