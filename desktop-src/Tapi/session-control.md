---
description: Eine Sitzung oder ein-Rückruf stellt eine Verbindung zwischen zwei oder mehr Adressen dar.
ms.assetid: f598c1cd-2b50-4ac6-a05e-4fd8eeb5e3e1
title: Sitzungssteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09250a90f978bde9be4f20aad6ee38f5e9766818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760795"
---
# <a name="session-control"></a><span data-ttu-id="180a4-103">Sitzungssteuerung</span><span class="sxs-lookup"><span data-stu-id="180a4-103">Session Control</span></span>

<span data-ttu-id="180a4-104">Eine Sitzung oder ein-Rückruf stellt eine Verbindung zwischen zwei oder mehr Adressen dar.</span><span class="sxs-lookup"><span data-stu-id="180a4-104">A session or call represents a connection between two or more addresses.</span></span> <span data-ttu-id="180a4-105">Diese Verbindung ist dynamisch, und die zugehörigen Programmier Objekte müssen bei Bedarf erstellt, manipuliert und freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="180a4-105">This connection is dynamic, and the associated programming objects must be created, manipulated, and released as needed.</span></span> <span data-ttu-id="180a4-106">Im einfachsten Fall bedeutet dies, dass Sie einen Telefonanruf tätigen und trennen.</span><span class="sxs-lookup"><span data-stu-id="180a4-106">In the simplest case, this means making and disconnecting a phone call.</span></span> <span data-ttu-id="180a4-107">Bei erweiterten Anwendungen kann die Sitzungssteuerung die Verwaltung von Multimedia-Konferenzen über ein IP-Netzwerk bis zu der Ebene einzelner Teilnehmer umfassen.</span><span class="sxs-lookup"><span data-stu-id="180a4-107">For advanced applications, session control may involve managing multimedia conferences over an IP network down to the level of individual participants.</span></span>

<span data-ttu-id="180a4-108">Die Sitzungssteuerung umfasst zwei grundlegende Bereiche:</span><span class="sxs-lookup"><span data-stu-id="180a4-108">Session control involves two basic areas:</span></span>

-   <span data-ttu-id="180a4-109">[Sitzungs Vorgänge](session-operations-ovr.md) sind Steuerelemente, mit denen eine Kommunikationssitzung initiiert, gewartet und beendet wird.</span><span class="sxs-lookup"><span data-stu-id="180a4-109">[Session Operations](session-operations-ovr.md) are controls that initiate, maintain, and terminate a communications session.</span></span>
-   <span data-ttu-id="180a4-110">[Sitzungsinformationen](session-information-ovr.md) beschreiben Daten, die in Bezug auf eine Kommunikationssitzung abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="180a4-110">[Session Information](session-information-ovr.md) describes data that can be obtained concerning a communications session.</span></span>

<span data-ttu-id="180a4-111">Zwei spezialisierte Typen der Sitzungssteuerung werden in diesem Abschnitt nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="180a4-111">Two specialized types of session control are not covered in this section.</span></span> <span data-ttu-id="180a4-112">Informationen zu automatischen Callcenter finden Sie unter [callcentersteuerelement](./call-center-control.md) (TAPI 2. x) oder Informationen [zu callcentersteuerelementen](about-call-center-controls.md) (TAPI 3. x).</span><span class="sxs-lookup"><span data-stu-id="180a4-112">For information on Automatic Call Distribution Centers, see [Call Center Control](./call-center-control.md) (TAPI 2.x) or [About Call Center Controls](about-call-center-controls.md) (TAPI 3.x).</span></span> <span data-ttu-id="180a4-113">Weitere Informationen zu IP-Konferenzen finden Sie unter Informationen [zu Rendezvous-IP-telefoniekonferenzen](about-rendezvous-ip-telephony-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="180a4-113">For information on IP conferencing, see [About Rendezvous IP Telephony Conferencing](about-rendezvous-ip-telephony-conferencing.md).</span></span>

 

 
