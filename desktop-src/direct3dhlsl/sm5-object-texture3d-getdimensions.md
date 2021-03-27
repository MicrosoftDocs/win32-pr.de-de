---
title: 'Texture3D:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture3D:: GetDimensions-Funktion'
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
keywords:
- GetDimensions-Funktion HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a700e0ff065e5f4758241ee0c8252965209a21f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995752"
---
# <a name="texture3dgetdimensions-function"></a>Texture3D:: GetDimensions-Funktion

Gibt die Dimensionen der Ressource zurück.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Miplevel* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Optional. MipMap-Ebene (muss angegeben werden, wenn " *numoflevels* " verwendet wird).

</dd> <dt>

*Breite* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcen Breite in Texels.

</dd> <dt>

*Höhe* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcen Höhe in Texels.

</dd> <dt>

*Tiefe* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcen Tiefe in Texels.

</dd> <dt>

*Nummerige* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl von MipMap-Ebenen (erfordert auch *miplevel* ).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nichts

## <a name="remarks"></a>Bemerkungen

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
