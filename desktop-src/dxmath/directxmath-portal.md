---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a041696daf5d5cad8467d01f8ef7912d177ba63a7193945b4cb52a430f4afc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118501767"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>Zweck

Die DirectXMath-API stellt SIMD-freundliche C++-Typen und -Funktionen für allgemeine lineare Algebra- und Grafikmathematikoperationen bereit, die directX-Anwendungen gemeinsam sind. Die Bibliothek stellt optimierte Versionen für Windows 32-Bit (x86), Windows 64-Bit (x64) und Windows auf ARM/ARM64 über die systeminternen Funktionen SSE, AVX und ARM-NEON im Visual C++ Compiler bereit.

Für Entwickler, die noch nicht mit DirectXMath arbeiten, sollten Sie den SimpleMath-Wrapper im *DirectX Tool Kit* für [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) als Ausgangspunkt in Erwägung ziehen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | BESCHREIBUNG                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [DirectXMath-Programmierhandbuch](ovw-xnamath-progguide.md)<br/>     | DirectXMath bietet eine mathematische Lösung, die für Windows optimiert ist.<br/>           |
| [DirectXMath-Programmierreferenz](ovw-xnamath-reference.md)<br/> | Dieser Abschnitt enthält Referenzmaterial für die DirectXMath-Bibliothek.<br/> |



 

## <a name="developer-audience"></a>Entwicklergruppe

Die DirectXMath-Bibliothek ist für C++-Entwickler konzipiert, die an Spielen und DirectX-Grafiken in Windows Store-Apps, Xbox-Spielen und herkömmlichen Desktop-Apps für Windows arbeiten.

## <a name="obtaining-directxmath"></a>Abrufen von DirectXMath
 
Die DirectXMath-Header sind im Windows SDK enthalten, das Visual Studio 2012 oder höher enthält, und als all-Inlineheader gibt es keine DLL oder statische Bibliothek, mit der verknüpft werden kann. Es ist auch als Paket auf [NuGet](https://www.nuget.org/packages/directxmath/)verfügbar.

DirectXMath ist open source unter der [MIT-Lizenz,](https://opensource.org/licenses/MIT) die auf [GitHub](https://github.com/Microsoft/DirectXMath)gehostet wird.




