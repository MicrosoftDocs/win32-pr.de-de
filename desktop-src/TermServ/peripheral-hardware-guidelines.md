---
title: Richtlinien für Peripheriegeräte
description: Wenn Ihr Hardware Gerät nicht für eine Remote Sitzung konzipiert ist, müssen die Anbieter sicherstellen, dass die Gerätetreibersoftware die Deaktivierung der Umleitung des Geräts mithilfe einer System Richtlinie oder Gruppenrichtlinie erzwingt.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388549"
---
# <a name="peripheral-hardware-guidelines"></a><span data-ttu-id="747da-103">Richtlinien für Peripheriegeräte</span><span class="sxs-lookup"><span data-stu-id="747da-103">Peripheral hardware guidelines</span></span>

<span data-ttu-id="747da-104">Bei einem Remotedesktopverbindung-Client (RDC) ist der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server der lokale Computer.</span><span class="sxs-lookup"><span data-stu-id="747da-104">To a Remote Desktop Connection (RDC) client, the Remote Desktop Session Host (RD Session Host) server is the local computer.</span></span> <span data-ttu-id="747da-105">Folglich werden Geräte, z. b. Laufwerke und Drucker, die an den Server angefügt sind, als lokale Geräte für einen Client angezeigt.</span><span class="sxs-lookup"><span data-stu-id="747da-105">Consequently, devices such as disk drives and printers attached to the server appear as local devices to a client.</span></span> <span data-ttu-id="747da-106">Im Gegensatz dazu können Laufwerke und Drucker, die an ein Client Terminal angeschlossen sind, als Remote Geräte angezeigt werden. Dies hängt von den Optionen ab, die für die Verbindung ausgewählt wurden, dem verwendeten Server und der Version der verwendeten Client Software.</span><span class="sxs-lookup"><span data-stu-id="747da-106">In contrast, drives and printers attached to a client terminal can appear to be remote devices, depending on the options selected for the connection, the server used, and the version of the client software used.</span></span>

<span data-ttu-id="747da-107">In der ersten Version von Remotedesktopdienste wurden keine Anwendungen unterstützt, die die Ausgabe direkt an serielle, parallele und Audioports senden, die an das Client Terminal angeschlossen sind. in den aktuellen Versionen können diese Geräte beispielsweise als lokale Geräte für Anwendungen angezeigt werden, die in der Remotedesktopdienste Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="747da-107">While the initial release of Remote Desktop Services did not support applications that send output directly to serial, parallel, and sound ports attached to the client terminal, the current versions do allow these devices to appear as local devices to applications running in the Remote Desktop Services session.</span></span>

<span data-ttu-id="747da-108">Wenn Ihr Hardware Gerät nicht für eine Remote Sitzung konzipiert ist, müssen die Anbieter sicherstellen, dass die Gerätetreibersoftware die Deaktivierung der Umleitung des Geräts mithilfe einer System Richtlinie oder Gruppenrichtlinie erzwingt.</span><span class="sxs-lookup"><span data-stu-id="747da-108">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

 

 




