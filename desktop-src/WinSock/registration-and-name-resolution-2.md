---
description: Windows Sockets 2 ist eine Reihe von Funktionen, die die Art und Weise standardisieren, wie Anwendungen auf die verschiedenen Netzwerk Benennungs Dienste zugreifen und diese verwenden.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Registrierung und Namensauflösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348528"
---
# <a name="registration-and-name-resolution"></a>Registrierung und Namensauflösung

Windows Sockets 2 ist eine Reihe von Funktionen, die die Art und Weise standardisieren, wie Anwendungen auf die verschiedenen Netzwerk Benennungs Dienste zugreifen und diese verwenden. Wenn Sie diese Funktionen verwenden, müssen Anwendungen nicht die weit verbreiteten Protokolle unterscheiden, die mit namens Diensten wie DNS, NIS, X. 500, SAP usw. verknüpft sind. Um vollständige Abwärtskompatibilität mit Windows Sockets 1,1 zu gewährleisten, werden die vorhandenen **getxbyy** -und asynchronen **WSAAsyncGetXbyY** -Datenbank-Lookup-Funktionen weiterhin unterstützt, aber in Bezug auf die neuen Namens Auflösungs Funktionen in der Schnittstelle des Windows Sockets Service-Anbieters implementiert. Weitere Informationen finden Sie unter den Funktionen " [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) " und " [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) ". Weitere Informationen finden Sie auch unter [kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).

In diesem Abschnitt werden die für Winsock-Entwickler verfügbaren Registrierungs-und namens Auflösungs Funktionen beschrieben. In der folgenden Liste werden die Themen in diesem Abschnitt beschrieben:

-   [Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
-   [Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Winsock](about-winsock.md)
</dt> <dt>

[Verwenden von Winsock](using-winsock.md)
</dt> </dl>

 

 



