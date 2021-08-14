---
description: Erstellen Sie ein Vertex-Shader-Versionsnummerntoken.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: D3DVS_VERSION Makro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 861295c9068bee9e40174d877a78628aa405b9cfa5d46414190fbb7b37904e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527256"
---
# <a name="d3dvs_version-macro"></a>\_D3DVS-VERSIONSmakro

Erstellen Sie ein Vertex-Shader-Versionsnummerntoken.

## <a name="syntax"></a>Syntax


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Hauptversion* 
</dt> <dd>

Die Hauptversion des Vertex-Shaders. Entsprechende Werte finden Sie in den Hinweisen.

</dd> <dt>

*\_Nebenversion* 
</dt> <dd>

Die Nebenversion des Vertex-Shaders. Entsprechende Werte finden Sie in den Hinweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen DWORD-Wert zurück, der eine Vertex-Shaderversion ist.

## <a name="remarks"></a>Hinweise

Versionsnummern

Die Versionsnummer ist eine Kombination aus der Hauptversion und den Nebenversionsnummern des Vertex-Shaders. Gültige Zahlen werden in der Tabelle angezeigt.



| Hauptversion | Nebenversion | Beispiel             |
|-------|-------|---------------------|
| 1     | 1     | D3DVS \_ VERSION(1,1) |
| 2     | 0     | D3DVS \_ VERSION(2,0) |
| 3     | 0     | D3DVS \_ VERSION(3,0) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




