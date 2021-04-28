---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd35f1faf004bc55a6802da204a6c2fe4e7869b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113008"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>Zweck

Die DirectXMath-API stellt SIMD-freundliche C++-Typen und -Funktionen für gängige lineare Algebra- und Grafikoperationen bereit, die für DirectX-Anwendungen üblich sind. Die Bibliothek bietet optimierte Versionen für systeminterne Windows 32-Bit-Versionen (x86), Windows 64-Bit (x64) und Windows unter ARM/ARM64 über SSE-, AVX- und ARM-NEON-Unterstützung im Visual C++-Compiler.

Für Entwickler, die noch nicht mit DirectXMath beginnen, sollten Sie erwägen, den SimpleMath-Wrapper im *DirectX Tool Kit* für [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) als Ausgangspunkt zu verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | BESCHREIBUNG                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [DirectXMath-Programmierhandbuch](ovw-xnamath-progguide.md)<br/>     | DirectXMath bietet eine für Windows optimierte mathematische Lösung.<br/>           |
| [DirectXMath-Programmierreferenz](ovw-xnamath-reference.md)<br/> | Dieser Abschnitt enthält Referenzmaterial für die DirectXMath-Bibliothek.<br/> |



 

## <a name="developer-audience"></a>Entwicklergruppe

Die DirectXMath-Bibliothek ist für C++-Entwickler konzipiert, die an Spielen und DirectX-Grafiken in Windows Store-Apps, Xbox-Spielen und herkömmlichen Desktop-Apps für Windows arbeiten.

## <a name="obtaining-directxmath"></a>Abrufen von DirectXMath
 
Die DirectXMath-Header sind im Windows SDK enthalten, die Visual Studio 2012 oder höher enthalten sind, und als All-Inline-Header gibt es keine DLL oder statische Bibliothek, mit der eine Verknüpfung erstellt werden kann. Es ist auch als Paket auf [NuGet verfügbar.](https://www.nuget.org/packages/directxmath/)

DirectXMath ist open source unter der [AUF GitHub](https://opensource.org/licenses/MIT) gehosteten [MIT-Lizenz.](https://github.com/Microsoft/DirectXMath)




