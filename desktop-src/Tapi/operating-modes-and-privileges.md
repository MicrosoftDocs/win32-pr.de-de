---
description: Die Anwendung kann einen von zwei Betriebsmodi anfordern, wenn ein Telefongerät geöffnet wird.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Betriebsmodi und Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755120"
---
# <a name="operating-modes-and-privileges"></a><span data-ttu-id="ac798-103">Betriebsmodi und Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="ac798-103">Operating Modes and Privileges</span></span>

<span data-ttu-id="ac798-104">Die Anwendung kann einen von zwei Betriebsmodi anfordern, wenn ein Telefongerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ac798-104">The application can request one of two operating modes when opening a phone device.</span></span> <span data-ttu-id="ac798-105">Diese Modi entsprechen den Berechtigungen, die die Anwendung für das Gerät anfordert:</span><span class="sxs-lookup"><span data-stu-id="ac798-105">These modes reflect the privileges the application requests for the device:</span></span>

-   <span data-ttu-id="ac798-106">Durch das Öffnen eines Telefons für Monitor Berechtigungen kann die Anwendung den Status des Telefon Geräts ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ac798-106">Opening a phone for monitor privileges lets the application determine the status of the phone device.</span></span> <span data-ttu-id="ac798-107">Nachrichten werden an die Anwendung gesendet, wenn Statusänderungen auf dem Telefongerät erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="ac798-107">Messages are sent to the application when status changes on the phone device are detected.</span></span>
-   <span data-ttu-id="ac798-108">Eine Anwendung, die ein Telefongerät für Besitzer Berechtigungen öffnet, kann Vorgänge verwenden, die den Zustand des Telefon Geräts ändern.</span><span class="sxs-lookup"><span data-stu-id="ac798-108">An application that opens a phone device for owner privileges can use operations that modify the state of the phone device.</span></span> <span data-ttu-id="ac798-109">Die Berechtigung "Besitzer" enthält automatisch auch vollständige Monitor Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="ac798-109">Owner privilege automatically includes full monitor privileges as well.</span></span> <span data-ttu-id="ac798-110">Ein bestimmtes Telefongerät kann jederzeit nur einmal für Besitzer Rechte geöffnet werden, jedoch mehrmals für Überwachungs Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="ac798-110">At any time, a given phone device can be open only once for owner privileges, but multiple times for monitor privileges.</span></span> <span data-ttu-id="ac798-111">Alle **phonesetvorgänge** erfordern Besitzer Berechtigungen, während für alle **phoneget** -Vorgänge nur Monitor Berechtigungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ac798-111">All **phoneSet** operations require owner privileges, while all **phoneGet** operations require only monitor privileges.</span></span>

 

 



