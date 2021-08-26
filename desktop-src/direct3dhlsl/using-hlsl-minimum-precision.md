---
title: Verwenden der minimalen Genauigkeit von HLSL
description: Ab Windows 8 können Grafiktreiber HLSL-Skalardatentypen mit minimaler Genauigkeit implementieren, indem eine genauigkeit verwendet wird, die größer oder gleich der angegebenen Bitgenauigkeit ist.
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4981cd80fdd80fbccf1b2610cbfeb210a9894a857fb2d7af1ddd84b9e2772e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067280"
---
# <a name="using-hlsl-minimum-precision"></a>Verwenden der minimalen Genauigkeit von HLSL

Ab Windows 8 können Grafiktreiber HLSL-Skalardatentypen mit minimaler Genauigkeit implementieren, indem sie eine genauigkeit verwenden, die größer oder gleich der angegebenen Bitgenauigkeit ist. [](dx-graphics-hlsl-scalar.md) Wenn Ihr HLSL-Shadercode mit minimaler Genauigkeit auf Hardware verwendet wird, die die minimale Genauigkeit von HLSL implementiert, verwenden Sie weniger Arbeitsspeicherbandbreite und damit auch weniger Systemleistung.

Sie können die minimale Genauigkeitsunterstützung abfragen, die der Grafiktreiber bietet, indem Sie [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) mit dem [**Wert D3D11 \_ FEATURE \_ SHADER MIN PRECISION \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) aufrufen. Weitere Informationen finden Sie unter [UNTERSTÜTZUNG der minimalen Genauigkeit von HLSL.](/windows/desktop/direct3d11/direct3d-11-1-features)

-   [Deklarieren von Variablen mit Minimalgenauigkeitsdatentypen](#declare-variables-with-minimum-precision-data-types)
-   [Testen des Shadercodes mit minimaler Genauigkeit](#testing-your-minimum-precision-shader-code)
-   [Zugehörige Themen](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>Deklarieren von Variablen mit Minimalgenauigkeitsdatentypen

Um die minimale Genauigkeit im HLSL-Shadercode zu verwenden, deklarieren Sie einzelne Variablen mit Typen wie **min16float** (**min16float4** für einen Vektor), **min16int,** **min10float** und so weiter. Mit diesen Variablen gibt Der Shadercode an, dass er nicht mehr Genauigkeit erfordert, als die Variablen angeben. Hardware kann jedoch die Minimalgenauigkeitsindikatoren ignorieren und mit vollständiger 32-Bit-Genauigkeit ausgeführt werden. Wenn Ihr Shadercode auf Hardware verwendet wird, die die minimale Genauigkeit nutzt, verwenden Sie weniger Arbeitsspeicherbandbreite und verwenden daher auch weniger Systemleistung, solange Ihr Shadercode nicht mehr Genauigkeit erwartet als angegeben.

Sie müssen nicht mehrere Shader erstellen, die die minimale Genauigkeit verwenden und nicht verwenden. Erstellen Sie stattdessen Shader mit minimaler Genauigkeit, und die Minimalgenauigkeitsvariablen verhalten sich mit voller 32-Bit-Genauigkeit, wenn der Grafiktreiber meldet, dass er keine minimale Genauigkeit unterstützt. HLSL-Shader mit minimaler Genauigkeit funktionieren nicht auf Betriebssystemen vor Windows 8 wenn Sie also planen, frühere Betriebssysteme als Ziel zu verwenden, müssen Sie mehrere Shader erstellen, von denen einige dies tun, und andere, die keine minimale Genauigkeit verwenden.

> [!Note]  
> Nehmen Sie keine Datenwechsel zwischen verschiedenen Genauigkeitsstufen innerhalb eines Shaders vor, da diese Arten von Konvertierungen verschwendet sind und die Leistung verringern. Die Ausnahme ist, dass Shaderkonst constants immer noch 32 Bit sind, aber Anbieter können Grafikhardware entwerfen, die frei in eine niedrigere Genauigkeit konvertiert werden kann, die der HLSL-Anweisungsleser verwenden kann.

 

Mit minimaler Genauigkeit können Sie die Genauigkeit von Berechnungen in verschiedenen Teilen ihres Shadercodes steuern.

Die Regeln für die minimale GENAUIGKEIT von HLSL ähneln C/C++, wobei die Typen in einem Ausdruck die Genauigkeit des Vorgangs und nicht den Typ bestimmen, in den schließlich geschrieben wird.

## <a name="testing-your-minimum-precision-shader-code"></a>Testen des Shadercodes mit minimaler Genauigkeit

Der Referenzraster ([**D3D \_ DRIVER \_ TYPE \_ REFERENCE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) gibt Ihnen einen groben Überblick darüber, wie sich die minimale Genauigkeit im HLSL-Shadercode verhält, indem jede HLSL-Anweisung auf die angegebene Genauigkeit quantisiert wird. Auf diese Weise können Sie Code finden, der versehentlich auf mehr als die minimale Genauigkeit angewiesen ist. Der Referenzraster wird nicht schneller ausgeführt, wenn der HLSL-Shadercode eine minimale Genauigkeit verwendet, aber Sie können ihn verwenden, um die Richtigkeit des Codes zu überprüfen. [WARP](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) ([**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) unterstützt nicht die Verwendung der minimalen Genauigkeit im HLSL-Shadercode. WARP wird nur mit vollständiger 32-Bit-Genauigkeit ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 