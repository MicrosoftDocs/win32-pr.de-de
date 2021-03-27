---
description: Wenn mehrere Monitore als unabhängige anzeigen verwendet werden, enthält der Desktop einen Bildschirm oder eine Reihe von anzeigen.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Verwenden mehrerer Monitore als unabhängige Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980505"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>Verwenden mehrerer Monitore als unabhängige Anzeige

Wenn mehrere Monitore als unabhängige anzeigen verwendet werden, enthält der Desktop einen Bildschirm oder eine Reihe von anzeigen. Diese Gruppe von Anzeigen enthält immer den primären Monitor und verhält sich wie in den anderen Abschnitten dieses Themas beschrieben. Eine Anwendung kann jeden anderen Monitor als unabhängige Anzeige verwenden.

> [!Note]  
> Die Verwendung anderer Monitore als unabhängige anzeigen wird für Treiber, die für das Windows-Anzeigetreiber Modell (WDDM) implementiert sind, nicht unterstützt.

 

Der Fenster-Manager weiß nichts über die unabhängigen anzeigen. Sie werden vollständig von der Anwendung gesteuert, und für die Anwendung sind keine Fenster-Manager-Funktionen verfügbar (alle Fenster-Manager-Aufrufe werden automatisch zur primären Anzeige geleitet). Jede unabhängige Anzeige verfügt über eigene Ursprungs-und horizontale und vertikale Koordinaten, und der Zugriff erfolgt über die GDI-Funktionen wie z. b. " [**kreatedc**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) " oder die DirectX-Funktionen wie " **directdrawcreate**".

Zum Auffinden der unabhängigen Anzeige aufrufen Sie " [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) " und suchen nach den anzeigen, für die das Flag "Gerät anzeigen" \_ \_ \_ \_ in der [**Anzeige \_ Geräte**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) Struktur nicht angezeigt wird.

Eine Anwendung kann eine Anzeige öffnen, indem Sie aufrufen.


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



In diesem Befehl ist der *lpszdisplayname* -Parameter einer der von [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) zurückgegebenen Gerätenamen, und *lpdevmode* ist eine Beschreibung des Grafikmodus für dieses Gerät. Der resultierende HDC kann verwendet werden, um einen beliebigen Grafik Vorgang für das Gerät auszuführen.

 

 



