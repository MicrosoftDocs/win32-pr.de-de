---
title: Verwenden der minimalen Genauigkeit von HLSL
description: Ab Windows 8 können Grafiktreiber minimale Genauigkeit der HLSL-Skalardatentypen implementieren, indem Sie eine beliebige Genauigkeit angeben, die größer oder gleich der angegebenen bitgenauigkeit ist.
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7f66f35aef3e870edb4e8564a280be89ce34be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728168"
---
# <a name="using-hlsl-minimum-precision"></a>Verwenden der minimalen Genauigkeit von HLSL

Ab Windows 8 können Grafiktreiber minimale Genauigkeit der [HLSL-Skalardatentypen](dx-graphics-hlsl-scalar.md) implementieren, indem Sie eine beliebige Genauigkeit angeben, die größer oder gleich der angegebenen bitgenauigkeit ist. Wenn der HLSL-Shader-Code mit minimaler Genauigkeit auf Hardware verwendet wird, die die minimale Genauigkeit von HLSL implementiert, werden weniger Speicherbandbreite verwendet, und daher wird auch weniger Systemleistung verwendet.

Sie können die Unterstützung der minimalen Genauigkeit Abfragen, die der Grafiktreiber bietet, indem Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) mit dem [**D3D11 \_ Feature- \_ Shader- \_ \_ \_ Unterstützungs**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) Wert für minimale Genauigkeit aufrufen. Weitere Informationen finden Sie [unter Unterstützung der Unterstützung von HLSL-Mindestgenauigkeit](/windows/desktop/direct3d11/direct3d-11-1-features)

-   [Deklarieren von Variablen mit minimalen Genauigkeits Datentypen](#declare-variables-with-minimum-precision-data-types)
-   [Testen des Shader-Codes mit minimaler Genauigkeit](#testing-your-minimum-precision-shader-code)
-   [Zugehörige Themen](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>Deklarieren von Variablen mit minimalen Genauigkeits Datentypen

Um die minimale Genauigkeit im HLSL-Shader-Code zu verwenden, deklarieren Sie einzelne Variablen mit Typen wie **min16float** (**min16float4** für einen Vektor), **min16int**, **min10float** usw. Mit diesen Variablen gibt der Shader-Code an, dass er keine höhere Genauigkeit erfordert, als die Variablen angeben. Hardware kann jedoch die minimalen Genauigkeits Indikatoren ignorieren und mit vollständiger 32-Bit-Genauigkeit ausgeführt werden. Wenn Ihr Shader-Code auf Hardware verwendet wird, die die minimale Genauigkeit nutzt, verwenden Sie weniger Speicherbandbreite. Daher verwenden Sie auch weniger Systemleistung, solange Ihr shadercode nicht mehr Genauigkeit erwartet, als er festgelegt wurde.

Sie müssen nicht mehrere Shader erstellen, die die minimale Genauigkeit nicht verwenden. Erstellen Sie stattdessen Shader mit minimaler Genauigkeit, und die minimalen Genauigkeits Variablen verhalten sich bei vollständiger 32-Bit-Genauigkeit, wenn der Grafiktreiber meldet, dass keine minimale Genauigkeit unterstützt wird. HLSL-Shader mit minimaler Genauigkeit funktionieren nicht für Betriebssysteme vor Windows 8. Wenn Sie also frühere Betriebssysteme als Ziel verwenden möchten, müssen Sie mehrere Shader erstellen, von denen einige etwas tun und andere keine minimale Genauigkeit verwenden.

> [!Note]  
> Nehmen Sie keine Daten Wechsel zwischen verschiedenen Genauigkeits Stufen innerhalb eines Shaders vor, da diese Konvertierungs Typen verschwendet werden und die Leistung reduzieren. Die Ausnahme besteht darin, dass shaderkonstanten immer noch 32 Bit sind, aber die Hersteller können Grafikhardware entwerfen, die auf die niedrigere Genauigkeit zurück konvertiert werden kann, die für das Lesen der HLSL-Anweisung verwendet werden kann.

 

Mithilfe der minimalen Genauigkeit können Sie die Genauigkeit von Berechnungen in verschiedenen Teilen des Shader-Codes steuern.

Die Regeln für die minimale Genauigkeit von HLSL sind vergleichbar mit C/C++, wobei die Typen in einem Ausdruck die Genauigkeit des Vorgangs bestimmen, nicht den Typ, in den schließlich geschrieben wird.

## <a name="testing-your-minimum-precision-shader-code"></a>Testen des Shader-Codes mit minimaler Genauigkeit

Der verweisrasterizer ([**D3D \_ Driver \_ Type \_ Reference**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) gibt Ihnen einen groben Eindruck, wie sich die minimale Genauigkeit im HLSL-Shader-Code verhält, indem jede HLSL-Anweisung mit der angegebenen Genauigkeit quantifiziert wird. Dies hilft Ihnen dabei, Code zu ermitteln, der versehentlich mehr als die minimale Genauigkeit benötigt. Der Verweis Raster wird nicht schneller ausgeführt, wenn der HLSL-Shader-Code eine minimale Genauigkeit verwendet, Sie können ihn jedoch verwenden, um die Richtigkeit des Codes zu überprüfen. [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) ([**D3D \_ Driver \_ Type \_ Warp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) unterstützt die Verwendung der minimalen Genauigkeit im HLSL-Shader-Code nicht. Warp wird nur mit vollständiger 32-Bit-Genauigkeit ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 