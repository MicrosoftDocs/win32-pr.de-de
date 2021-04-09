---
title: Entwurfs Überlegungen für Proxy Objekte
description: Der Proxy und der barrierefreie Objekt Entwurf hängen vom Entwurf der Benutzeroberflächen Elemente des Servers ab. Unabhängig vom Entwurf muss ein Benutzeroberflächen Element sein Proxy Objekt direkt benachrichtigen, bevor es zerstört wird, damit das Proxy Objekt Aufrufe von Clients entsprechend verarbeitet.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036550"
---
# <a name="design-considerations-for-proxy-objects"></a>Entwurfs Überlegungen für Proxy Objekte

Der Proxy und der barrierefreie Objekt Entwurf hängen vom Entwurf der Benutzeroberflächen Elemente des Servers ab. Unabhängig vom Entwurf muss ein Benutzeroberflächen Element sein Proxy Objekt direkt benachrichtigen, bevor es zerstört wird, damit das Proxy Objekt Aufrufe von Clients entsprechend verarbeitet.

In der folgenden Liste werden zwei Entwurfs Möglichkeiten beschrieben:

-   Platzieren Sie den Code, der die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementiert, im gleichen Modul wie der Code, der das Benutzeroberflächen Element implementiert, wenn der Code der Benutzeroberfläche leicht erweiterbar ist. In diesem Fall ist der Proxy "Lightweight" in dem Sinne, dass er lediglich die Lebensdauer des barrierefreien Objekts überwacht, Aufrufe an das barrierefreie Objekt weiterleiten und die Ergebnisse zurückgibt.
-   Platzieren Sie den Code, der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementiert, im gleichen Modul wie der Code, der das Proxy Objekt implementiert. In diesem Fall verwendet das barrierefreie Objekt interne Funktionen zum Abrufen von Informationen über das UI-Element.

## <a name="trackbar-controls"></a>TrackBar-Steuerelemente

Wenn Sie TrackBar-Steuerelemente implementieren, verwenden Sie die **TSB \_** für das TrackBar-Format, um aussagekräftige Informationen bereitzustellen. Dieser Stil kehrt die von [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)verwendete Skala um.

Bei vertikalen trackbars ohne diesen Stil gibt [**IAccessible:: get- \_ accValue den Wert**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) NULL (0) zurück, wenn sich der TrackBar-Ziehpunkt am oberen Rand des Steuer Elements befindet. die Werte erhöhen sich, wenn Sie den Ziehpunkt auf den unteren Rand verschieben. Beim **\_ umgekehrten TSB** -Format gibt **IAccessible:: get \_ accValue** 100 (100) zurück, wenn sich der TrackBar-Ziehpunkt im oberen Bereich befindet. die Zahlen verringern sich, wenn Sie den TrackBar-Ziehpunkt in den unteren Bereich verschieben.

Bei horizontalen trackbars ohne diesen Stil wird 0 (null) zurückgegeben, wenn sich der TrackBar-Ziehpunkt am linken Ende des Steuer Elements befindet. die Werte erhöhen sich, wenn Sie den TrackBar-Ziehpunkt nach rechts verschieben. Bei einem **\_ umgekehrten TSB** -Stil gibt [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 100 (100) zurück, wenn sich der Ziehpunkt auf der linken Seite befindet. die Werte verringern sich, wenn Sie den TrackBar-Ziehpunkt nach rechts verschieben.

 

 




