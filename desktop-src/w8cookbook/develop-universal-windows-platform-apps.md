---
title: Entwickeln von UWP-Apps (Universal Windows Platform)
description: Entwickeln von UWP-Apps (Universal Windows Platform)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 332864b00614ceb494b2832c0b565a5a10819d631ecb6c4098284a94ad2c038e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935440"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>Entwickeln von UWP-Apps (Universal Windows Platform)

Wir empfehlen allen Desktop-App-ISVs (Win32), Ihre Desktop-Apps über die Desktop-Brücke auf die [Universelle Windows-Plattform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) zu übertragen. Da UWP-Apps außerdem im [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/) unterstützt werden, ist es für Sie einfacher, Ihrer Benutzerbasis ein automatisches Update auf eine konsistente Version zu bieten und Ihre Supportkosten zu senken.

Wenn Ihre Desktop-Apps nicht mithilfe des Desktop-Brücke konvertiert werden können, wird dringend empfohlen, ein Installationsprogramm zu verwenden, das den bewährten Methoden folgt, und sicherzustellen, dass dies vollständig getestet wird. Ein Installationsprogramm ist die erste Erfahrung Ihres Benutzers oder Kunden mit Ihrer App. Dies ist häufig nicht der Fall, u. a. auch, weil das Programm nicht für alle Szenarien getestet wurde. Mit [dem Windows App Certification Kit](https://dev.windows.com/develop/app-certification-kit) können Sie die Installation und Deinstallation Ihrer Win32-App testen und die Verwendung von nicht dokumentierten APIs sowie andere grundlegende Leistungsprobleme mit bewährten Methoden identifizieren, bevor Ihre Benutzer dies tun.

## <a name="best-practices"></a>Bewährten Methoden:

-   Verwenden Sie Installationsprogramme, die die 32-Bit- und 64-Bit-Version von Windows unterstützen.
-   Achten Sie beim Entwickeln Ihrer Installationsprogramme darauf, dass sie mehrere Szenarien (sowohl benutzer- als auch computerspezifisch) abdecken.
-   Alle weitervertreibbaren Windows-Komponenten sollten im Originalpaket verbleiben. Durch ein Umpacken kann das Installationsprogramm beschädigt werden.
-   Planen Sie Entwicklungszeit für Ihre Installationsprogramme ein. Häufig wird im Lebenszyklus der Softwareentwicklung übersehen, dass sie zum Lieferumfang dazugehören.

 

 




