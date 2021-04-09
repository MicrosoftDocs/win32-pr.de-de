---
title: Weitere Verbindungsinformationen
description: Die Member der rasdialparameams-Struktur können auch die folgenden Verbindungsinformationen angeben.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948848"
---
# <a name="other-connection-information"></a><span data-ttu-id="ec770-103">Weitere Verbindungsinformationen</span><span class="sxs-lookup"><span data-stu-id="ec770-103">Other Connection Information</span></span>

<span data-ttu-id="ec770-104">Die Member der [**rasdialparameams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) -Struktur können auch die folgenden Verbindungsinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="ec770-104">The members of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure can also specify the following connection information.</span></span>

-   <span data-ttu-id="ec770-105">Eine Telefonnummer, mit der die Nummer im Telefonbucheintrag überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec770-105">A phone number to override the number in the phone-book entry.</span></span>
-   <span data-ttu-id="ec770-106">Eine [Rückruf](callback-connections.md) Telefonnummer, die vom Remote Server aufgerufen werden kann, um die Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ec770-106">A [callback](callback-connections.md) phone number that the remote server can call back to establish the connection.</span></span>
-   <span data-ttu-id="ec770-107">Der Name der Remote Netzwerk Domäne, in der die Authentifizierung erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="ec770-107">The name of the remote network domain on which the authentication is to occur.</span></span>

<span data-ttu-id="ec770-108">Für die Rückrufnummer und die Domäne können die Mitglieder des [**rasdialparamemes**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) entweder angeben, dass RAS die Informationen im Telefonbucheintrag verwenden soll, oder es können Informationen bereitgestellt werden, die die Telefonbuchdaten überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ec770-108">For the callback number and the domain, the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) members can either indicate that RAS should use the information in the phone-book entry, or it can provide information that overrides the phone-book data.</span></span>

<span data-ttu-id="ec770-109">Ein RAS-Client kann den *lprasdialextensions* -Parameter der [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Funktion verwenden, um zu steuern, ob RAS das in einem Telefonbucheintrag angegebene Telefonnummern Präfix oder-Suffix verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec770-109">A RAS client can use the *lpRasDialExtensions* parameter of the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to control whether RAS uses a phone number prefix or suffix specified in a phone-book entry.</span></span>

 

 