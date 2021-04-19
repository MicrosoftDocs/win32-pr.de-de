---
description: Die directxmath-Bibliothek basiert auf der XNA Math C++ SIMD Library Version 2. x. Hier wird beschrieben, wie sich directxmath von XNA Math unterscheidet und wie sich directxmath-Versionen unterscheiden.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Neuigkeiten (directxmath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345217"
---
# <a name="whats-new-directxmath"></a>Neuigkeiten (directxmath)

Die directxmath-Bibliothek basiert auf der [XNA Math C++ SIMD Library, Version 2,04](https://walbourn.github.io/). Hier wird beschrieben, wie sich directxmath von XNA Math unterscheidet und wie sich directxmath-Versionen unterscheiden.

-   [Rlease-Verlauf](#release-history)
-   [Directxmath-Unterschiede von XNA math](#directxmath-differences-from-xna-math)
-   [Zugehörige Themen](#related-topics)

## <a name="release-history"></a>Releaseverlauf

<table>
 <tr>
  <td>Windows 10 Mai 2020 Update SDK</td><td>Directxmath 3,14</td>
 </tr>
 <tr>
  <td>SDK für Windows 10-Update vom Oktober 2018</td><td>Directxmath 3,13</td>
 </tr>
 <tr>
  <td>Windows 10 April 2018 Update SDK<br />Windows 10 Fall Creators Update SDK</td><td>Directxmath 3,11</td>
 </tr>
 <tr>
  <td>Windows 10 Creators Update SDK</td><td>Directxmath 3,10</td>
 </tr>
 <tr>
  <td>SDK für Windows 10 Anniversary</td><td>Directxmath 3,09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (November 2015)</td><td>Directxmath 3,08</td>
 </tr>
 <tr>
  <td>Windows SDK für Windows 8.1 (Spring 2015)</td><td>Directxmath 3,07</td>
 </tr>
 <tr>
  <td>Windows SDK für Windows 8.1</td><td>Directxmath 3,06</td>
 </tr>
 <tr>
  <td>Windows SDK für Windows 8</td><td>Directxmath 3,03</td>
 </tr>
</table>

Weitere Informationen finden Sie unter [directxmath-Releases](https://github.com/Microsoft/DirectXMath/releases) .

## <a name="directxmath-differences-from-xna-math"></a>Directxmath-Unterschiede von XNA math

Die directxmath-Bibliothek unterscheidet sich in erster Linie von der XNA-mathematischen Bibliothek:

-   Directxmath ist nur C++ (Namespaces, über Ladungen, neue Vorlagen usw.).
-   Erfordert die c++ 11-Standard Bibliotheks Unterstützung (d. h. stdint. h usw.).
-   Systeminterne Arm-Neon-Unterstützung für die Windows RT-Plattform.
-   Neue Farb Funktionalität (Farb Raum Konvertierungen, .net-Farb Konstanten).
-   Begrenzungs Volumetypen (eine Version von, die sich zuvor im xnacollision-Header im DirectX SDK-Konflikt Beispiel befunden hat).
-   Es ist keine Xbox 360-Version verfügbar. Das Xbox 360-XDK sendet weiterhin xnamath v2. x; Entfernen von Xbox 360-spezifischen Datentypen und Funktionsvarianten.
-   Überarbeitete [**xmvector perstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) Funktionen für eine verbesserte Optimierung der systeminternen SSE-und Arm-Neon-Funktionen.
-   Der [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) -Typ ist vollständig undurchsichtig. Wenn Sie auf einzelne Elemente von **xmmatrix** zugreifen möchten, verwenden Sie andere Typen, z. b. [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Programmier Handbuch](ovw-xnamath-progguide.md)
</dt> <dt>

[Directxmath-Releases](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
