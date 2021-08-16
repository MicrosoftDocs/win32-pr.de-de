---
title: Texture1D::GetDimensions-Funktion
description: Gibt die Dimensionen der Ressource zurück. | Texture1D::GetDimensions-Funktion
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: 1cca266d5e921d4f8071123d7b6be8b142ff83b06e2efebbe16fb5970555eaf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508696"
---
# <a name="texture1dgetdimensions-function"></a>Texture1D::GetDimensions-Funktion

Gibt die Dimensionen der Ressource zurück.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*MipLevel* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Optional. Mipmap-Ebene (muss angegeben werden, wenn *NumberOfLevels* verwendet wird).

</dd> <dt>

*Breite* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcenbreite in Texeln.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Mipmap-Ebenen (erfordert *auch MipLevel).*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
