---
title: Processisolinetess Factors-Funktion
description: Generiert die gerundeten Mosaik Faktoren für eine Isolationsstufe.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Processisolinetess Factors-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718821"
---
# <a name="processisolinetessfactors-function"></a>Processisolinetess Factors-Funktion

Generiert die gerundeten Mosaik Faktoren für eine Isolationsstufe.

## <a name="syntax"></a>Syntax

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Rawdetailfactor* \[ in\]
</dt> <dd>

Typ: **float**

Der gewünschte Detail Faktor.

</dd> <dt>

*Rawdensityfactor* \[ in\]
</dt> <dd>

Typ: **float**

Der gewünschte Dichte Faktor.

</dd> <dt>

*Rounabddetailfactor* \[ vorgenommen\]
</dt> <dd>

Typ: **float**

Der abgerundete Detail Faktor wurde an einen Bereich geklemmt, der vom Mosaik verwendet werden kann.

</dd> <dt>

*Rounzerddensityfactor* \[ vorgenommen\]
</dt> <dd>

Typ: **float**

Der Faktor für die abgerundete Dichte wurde an eine rangegeklammert, die vom Mosaik Prozess verwendet werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




