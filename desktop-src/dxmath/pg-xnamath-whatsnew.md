---
description: Die DirectXMath-Bibliothek basiert auf der XNA Math C++-SIMD-Bibliotheksversion 2.x. Hier wird beschrieben, wie sich DirectXMath von XNA Math unterscheidet und wie sich DirectXMath-Versionen unterscheiden.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Neues (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e94d4ba2433501fb5389b82dab4f5c3de4b8ed80904ed4629729537bbf264a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984710"
---
# <a name="whats-new-directxmath"></a>Neues (DirectXMath)

Die DirectXMath-Bibliothek basiert auf der [XNA Math C++-SIMD-Bibliotheksversion 2.04.](https://walbourn.github.io/xna-math-version-2-04/) Hier wird beschrieben, wie sich DirectXMath von XNA Math unterscheidet und wie sich DirectXMath-Versionen unterscheiden.

-   [Rlease-Verlauf](#release-history)
-   [DirectXMath-Unterschiede zu XNA Math](#directxmath-differences-from-xna-math)
-   [Zugehörige Themen](#related-topics)

## <a name="release-history"></a>Releaseverlauf

<table>
 <tr>
  <td>Windows 10 SDK (20348), Version 2104</td><td>DirectXMath 3.16</td>
 </td>
 <tr>
  <td>Windows 10 Mai 2020 Update SDK</td><td>DirectXMath 3.14</td>
 </tr>
 <tr>
  <td>Windows 10 October 2018 Update Sdk</td><td>DirectXMath 3.13</td>
 </tr>
 <tr>
  <td>Windows 10 Update-SDK für April 2018<br />Windows 10 Fall Creators Update Sdk</td><td>DirectXMath 3.11</td>
 </tr>
 <tr>
  <td>Windows 10 Creators Update Sdk</td><td>DirectXMath 3.10</td>
 </tr>
 <tr>
  <td>SDK für Windows 10 Anniversary</td><td>DirectXMath 3.09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (November 2015)</td><td>DirectXMath 3.08</td>
 </tr>
 <tr>
  <td>Windows SDK für Windows 8.1 (Spring 2015)</td><td>DirectXMath 3.07</td>
 </tr>
 <tr>
  <td>Windows SDK für Windows 8.1</td><td>DirectXMath 3.06</td>
 </tr>
 <tr>
  <td>Windows SDK für Windows 8</td><td>DirectXMath 3.03</td>
 </tr>
</table>

Weitere [Informationen finden Sie unter DirectXMath-Releases.](https://github.com/Microsoft/DirectXMath/releases)

## <a name="directxmath-differences-from-xna-math"></a>DirectXMath-Unterschiede zu XNA Math

Die DirectXMath-Bibliothek unterscheidet sich in erster Linie von der XNA Math-Bibliothek:

-   DirectXMath ist nur C++ (Namespaces, Überladungen, neue Vorlagen und so weiter).
-   Erfordert C++11-Standardbibliotheksunterstützung (d. h. stdint.h und so weiter).
-   Systeminterne ARM-NEON-Unterstützung für die Windows RT Plattform.
-   Neue Farbfunktionalität (Farbraumkonvertierungen, .NET-Farbkonst constants).
-   Begrenzungs-Volumetypen (eine Version von , die zuvor im XNACollision-Header im DirectX SDK-Kollisionsbeispiel enthalten war).
-   Es Xbox 360 Version nicht verfügbar. Das Xbox 360 XDK wird weiterhin XNAMath v2.x liefern. Entfernen von Xbox 360 bestimmten Datentypen und Funktionsvarianten.
-   Überarbeitete [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) für verbesserte Optimierung für systeminterne SSE- und ARM-NEON-Systema.
-   Der [**XMMATRIX-Typ**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) ist vollständig deckend. Um auf einzelne Elemente von **XMMATRIX** zu zugreifen, verwenden Sie andere Typen wie [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Programmierhandbuch](ovw-xnamath-progguide.md)
</dt> <dt>

[DirectXMath-Releases](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
