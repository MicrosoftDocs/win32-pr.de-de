---
description: Benutzer können den Status der Teredo-Schnittstelle über die Eingabeaufforderung überprüfen, indem Sie Netsh Interface Teredo Show State eingeben und die Ausgabe untersuchen.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: Die Peer Infrastruktur und Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529120"
---
# <a name="the-peer-infrastructure-and-teredo"></a><span data-ttu-id="a21d4-103">Die Peer Infrastruktur und Teredo</span><span class="sxs-lookup"><span data-stu-id="a21d4-103">The Peer Infrastructure and Teredo</span></span>

<span data-ttu-id="a21d4-104">Benutzer können den Status der [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) -Schnittstelle über die Eingabeaufforderung überprüfen, indem Sie **Netsh Interface Teredo Show State** eingeben und die Ausgabe untersuchen.</span><span class="sxs-lookup"><span data-stu-id="a21d4-104">A user can check the status of the [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) interface from the command prompt by typing **netsh interface teredo show state** and examining the output.</span></span> <span data-ttu-id="a21d4-105">Wenn der Status "Offline" lautet, ist Teredo nicht aktiv, wodurch verhindert wird, dass der Benutzer über seine Teredo-Adressen eine Verbindung mit anderen Benutzern herstellt.</span><span class="sxs-lookup"><span data-stu-id="a21d4-105">If the state is "offline", Teredo is not active, which prevents the user from connecting to other users via their Teredo addresses.</span></span> <span data-ttu-id="a21d4-106">Möglicherweise ist Teredo offline, da die Firewall deaktiviert ist oder [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10))nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a21d4-106">It is possible Teredo may be offline because your firewall is disabled or does not support [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span></span>

 

 
