---
title: 'Texture2DMSArray:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture2DMSArray:: GetDimensions-Funktion'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
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
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353719"
---
# <a name="texture2dmsarraygetdimensions-function"></a>Texture2DMSArray:: GetDimensions-Funktion

Gibt die Dimensionen der Ressource zurück.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

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

*Elemente* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Elemente im Array.

</dd> <dt>

*Anzahl von Beispielen* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Beispiel Speicherorte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nichts

## <a name="remarks"></a>Bemerkungen

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
