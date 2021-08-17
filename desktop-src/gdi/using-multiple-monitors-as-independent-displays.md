---
description: Wenn mehrere Monitore als unabhängige Anzeigen verwendet werden, enthält der Desktop eine Anzeige oder eine Gruppe von Anzeigen.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Verwenden mehrerer Monitore als unabhängige Anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710672e02e8ea7244e09c21b876197033e5f17144433b8f530ad8e52cd6806e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468250"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>Verwenden mehrerer Monitore als unabhängige Anzeigen

Wenn mehrere Monitore als unabhängige Anzeigen verwendet werden, enthält der Desktop eine Anzeige oder eine Gruppe von Anzeigen. Diese Gruppe von Anzeigen enthält immer den primären Monitor und verhält sich wie in den anderen Abschnitten dieses Themas erwähnt. Eine Anwendung kann einen beliebigen anderen Monitor als unabhängige Anzeige verwenden.

> [!Note]  
> Die Verwendung anderer Monitore als unabhängige Anzeige wird auf Treibern, die in das Windows Display Driver Model (WDDM) implementiert sind, nicht unterstützt.

 

Der Fenster-Manager weiß nichts über die unabhängigen Anzeigen. Sie werden vollständig von der Anwendung gesteuert, und es sind keine Fenster-Manager-Funktionen für die Anwendung verfügbar (alle Fenster-Manager-Aufrufe werden automatisch an die primäre Anzeige gestellt). Jede unabhängige Anzeige hat ihren eigenen Ursprung sowie horizontale und vertikale Koordinaten und wird über die GDI-Funktionen wie [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) oder directX-Funktionen wie **DirectDrawCreate aufgerufen.**

Um die unabhängigen Anzeigen zu finden, rufen Sie [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) auf, und suchen Sie in der DISPLAY DEVICE-Struktur nach den Anzeigen, für die das Flag DISPLAY DEVICE ATTACHED TO DESKTOP nicht \_ \_ \_ \_ [**\_ angezeigt**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) wird.

Eine Anwendung kann eine Anzeige öffnen, indem sie aufruft.


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



In diesem Aufruf ist der *lpszDisplayName-Parameter* einer der gerätenamen, die von [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) zurückgegeben werden, und *lpDevMode* ist eine Beschreibung des Grafikmodus für dieses Gerät. Die resultierende HDC kann verwendet werden, um alle Grafikvorgang auf dem Gerät durchzuführen.

 

 



