---
title: Entwickeln von universelle Windows-Plattform-Apps (UWP)
description: Entwickeln von universelle Windows-Plattform-Apps (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "106340888"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>Entwickeln von universelle Windows-Plattform-Apps (UWP)

Wir empfehlen, dass alle Microsoft Desktop-Apps (Win32) Ihre Desktop-Apps über die Desktop Bridge in die [universelle Windows-Plattform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) übertragen. Da UWP-Apps außerdem im [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/) unterstützt werden, ist es für Sie einfacher, Ihrer Benutzerbasis ein automatisches Update auf eine konsistente Version zu bieten und Ihre Supportkosten zu senken.

Wenn Ihre Desktop-Apps nicht über die Desktop Bridge konvertiert werden können, wird dringend empfohlen, dass Sie ein Installationsprogramm verwenden, das die bewährten Methoden befolgt, und sicherstellen, dass dies vollständig getestet ist. Ein Installer ist die erste Benutzerfreundlichkeit Ihrer APP. Dies ist häufig nicht der Fall, u. a. auch, weil das Programm nicht für alle Szenarien getestet wurde. Das [zertifizierungskit für Windows-apps](https://dev.windows.com/develop/app-certification-kit) kann Ihnen helfen, die Installation und Deinstallation ihrer Win32-APP zu testen und die Verwendung nicht dokumentierter APIs sowie andere grundlegende leistungsbezogene Probleme zu identifizieren, die vor ihren Benutzern auftreten.

## <a name="best-practices"></a>Bewährten Methoden:

-   Verwenden Sie Installationsprogramme, die die 32-Bit- und 64-Bit-Version von Windows unterstützen.
-   Achten Sie beim Entwickeln Ihrer Installationsprogramme darauf, dass sie mehrere Szenarien (sowohl benutzer- als auch computerspezifisch) abdecken.
-   Alle weitervertreibbaren Windows-Komponenten sollten im Originalpaket verbleiben. Durch ein Umpacken kann das Installationsprogramm beschädigt werden.
-   Planen Sie Entwicklungszeit für Ihre Installationsprogramme ein. Häufig wird im Lebenszyklus der Softwareentwicklung übersehen, dass sie zum Lieferumfang dazugehören.

 

 




