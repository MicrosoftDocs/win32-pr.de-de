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
# <a name="registration-and-name-resolution"></a><span data-ttu-id="ea714-103">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="ea714-103">Registration and Name Resolution</span></span>

<span data-ttu-id="ea714-104">Windows Sockets 2 ist eine Reihe von Funktionen, die die Art und Weise standardisieren, wie Anwendungen auf die verschiedenen Netzwerk Benennungs Dienste zugreifen und diese verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea714-104">Windows Sockets 2 is a set of functions that standardizes the way applications access and use the various network naming services.</span></span> <span data-ttu-id="ea714-105">Wenn Sie diese Funktionen verwenden, müssen Anwendungen nicht die weit verbreiteten Protokolle unterscheiden, die mit namens Diensten wie DNS, NIS, X. 500, SAP usw. verknüpft sind. Um vollständige Abwärtskompatibilität mit Windows Sockets 1,1 zu gewährleisten, werden die vorhandenen **getxbyy** -und asynchronen **WSAAsyncGetXbyY** -Datenbank-Lookup-Funktionen weiterhin unterstützt, aber in Bezug auf die neuen Namens Auflösungs Funktionen in der Schnittstelle des Windows Sockets Service-Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="ea714-105">When using these functions, applications need not distinguish the widely differing protocols associated with name services such as DNS, NIS, X.500, SAP, etc. To maintain full backward compatibility with Windows Sockets 1.1, the existing **getXbyY** and asynchronous **WSAAsyncGetXbyY** database-lookup functions continue to be supported, but are implemented in the Windows Sockets service provider interface in terms of the new name resolution capabilities.</span></span> <span data-ttu-id="ea714-106">Weitere Informationen finden Sie unter den Funktionen " [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) " und " [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) ".</span><span class="sxs-lookup"><span data-stu-id="ea714-106">For more information, see the [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions.</span></span> <span data-ttu-id="ea714-107">Weitere Informationen finden Sie auch unter [kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span><span class="sxs-lookup"><span data-stu-id="ea714-107">Also, see [Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span></span>

<span data-ttu-id="ea714-108">In diesem Abschnitt werden die für Winsock-Entwickler verfügbaren Registrierungs-und namens Auflösungs Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea714-108">This section describes registration and name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="ea714-109">In der folgenden Liste werden die Themen in diesem Abschnitt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="ea714-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="ea714-110">Protokoll unabhängige Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="ea714-110">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
-   [<span data-ttu-id="ea714-111">Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API</span><span class="sxs-lookup"><span data-stu-id="ea714-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="ea714-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea714-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea714-113">Informationen zu Winsock</span><span class="sxs-lookup"><span data-stu-id="ea714-113">About Winsock</span></span>](about-winsock.md)
</dt> <dt>

[<span data-ttu-id="ea714-114">Verwenden von Winsock</span><span class="sxs-lookup"><span data-stu-id="ea714-114">Using Winsock</span></span>](using-winsock.md)
</dt> </dl>

 

 



