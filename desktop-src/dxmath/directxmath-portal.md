---
description: .
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f316939514d9a186fcd5ef36372f31709b69a7a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351999"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>Zweck

Die directxmath-API bietet SIMD-freundliche C++-Typen und-Funktionen für häufige lineare Algebra-und Grafik mathematische Operationen, die für DirectX-Anwendungen gemeinsam sind. Die Bibliothek bietet optimierte Versionen für Windows 32-Bit (x86), Windows 64-Bit (x64) und Windows auf Arm/ARM64 durch SSE, AVX und systeminterne Unterstützung für Arm-Neon im Visual C++ Compiler.

Für Entwickler, die noch nicht mit directxmath vertraut sind, sollten Sie den simplemath-Wrapper im *DirectX-Toolkit* für [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) als Ausgangspunkt verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | BESCHREIBUNG                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Directxmath-Programmier Handbuch](ovw-xnamath-progguide.md)<br/>     | Directxmath bietet eine mathematische Lösung, die für Windows optimiert ist.<br/>           |
| [Directxmath-Programmier Referenz](ovw-xnamath-reference.md)<br/> | Dieser Abschnitt enthält Referenzmaterial für die directxmath-Bibliothek.<br/> |



 

## <a name="developer-audience"></a>Entwicklergruppe

Die directxmath-Bibliothek ist für C++-Entwickler konzipiert, die an spielen und DirectX-Grafiken in Windows Store-Apps, Xbox-spielen und herkömmlichen Desktop-Apps für Windows arbeiten.

## <a name="obtaining-directxmath"></a>Abrufen von directxmath
 
Die directxmath-Header werden in der Windows SDK geliefert, die in Visual Studio 2012 oder höher enthalten ist, und als alle Inline Header gibt es keine DLL oder statische Bibliothek, mit der eine Verknüpfung hergestellt werden kann. Es ist auch als Paket auf [nuget](https://www.nuget.org/packages/directxmath/)verfügbar.

Directxmath ist Open Source unter der [mit-Lizenz](https://opensource.org/licenses/MIT) , die auf [GitHub](https://github.com/Microsoft/DirectXMath)gehostet wird.




