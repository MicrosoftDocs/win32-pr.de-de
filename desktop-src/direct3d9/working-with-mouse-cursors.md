---
description: Mit den Maus Cursor Methoden kann die Anwendung einen Farb Cursor angeben, indem eine Oberfläche bereitgestellt wird, die ein Bild enthält.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Arbeiten mit Maus Cursorn (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482414"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Arbeiten mit Maus Cursorn (Direct3D 9)

Mit den Maus Cursor Methoden kann die Anwendung einen Farb Cursor angeben, indem eine Oberfläche bereitgestellt wird, die ein Bild enthält. Das System stellt sicher, dass dieser Cursor zur Hälfte der Anzeige Rate oder mehr aktualisiert wird, wenn die Frame Rate der Anwendung langsam ist. Der Cursor wird jedoch nie häufiger aktualisiert als die Aktualisierungsrate der Anzeige.

Die Position des Mauszeigers ist an den System Cursor gebunden und entsprechend der aktuellen räumlichen Auflösung des Anzeigemodus skaliert, kann aber explizit von der Anwendung verschoben werden. Dies entspricht dem Verhalten des mit der Win32-API unterstützten System Maus Cursors. Weitere Informationen zur Verwendung eines Mauszeigers in ihrer Direct3D-Anwendung finden Sie in den folgenden Referenz Themen.

-   [**IDirect3DDevice9:: ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9:: setcurrsorposition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9:: setcurrsorproperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D stellt sicher, dass die Maus entweder von Hardware Implementierungen oder von der Direct3D-Laufzeit unterstützt wird, die beim Aufrufen von IDirect3DDevice9 die hardwarebeschleunigte Blitvorgänge ausführt, wenn [**::P erneut gesendet**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
