---
description: Mit den Mauszeigermethoden kann die Anwendung einen Farbcursor angeben, indem eine Oberfläche mit einem Bild angegeben wird.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Arbeiten mit Mauscursorn (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999bd324c8c3a1a2c743b5417f5d316a9d0f9493ccb4b749545e53e23e58917f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518918"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Arbeiten mit Mauscursorn (Direct3D 9)

Mit den Mauszeigermethoden kann die Anwendung einen Farbcursor angeben, indem eine Oberfläche mit einem Bild angegeben wird. Das System stellt sicher, dass dieser Cursor bei halber Anzeigerate oder mehr aktualisiert wird, wenn die Bildfrequenz der Anwendung langsam ist. Der Cursor wird jedoch nie häufiger aktualisiert als die Aktualisierungsrate der Anzeige.

Die Position des Mauszeigers ist an den Systemcursor gebunden und entsprechend für die aktuelle räumliche Auflösung des Anzeigemodus skaliert, kann jedoch explizit von der Anwendung verschoben werden. Dies entspricht dem Verhalten der Win32-API– unterstützter Systemmauscursor. Weitere Informationen zur Verwendung eines Mauszeigers in Ihrer Direct3D-Anwendung finden Sie in den folgenden Referenzthemen.

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D stellt sicher, dass die Maus entweder von Hardwareimplementierungen oder von der Direct3D-Laufzeit unterstützt wird, die hardwarebeschleunigte Blittingvorgänge ausführt, wenn [**IDirect3DDevice9::P resent aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren Tipps](programming-tips.md)
</dt> </dl>

 

 
