---
description: Eine smartcardschnittstelle besteht aus einem vordefinierten Satz von Diensten, die auf einer Smartcard verfügbar sind, den Protokollen, die zum Aufrufen der Dienste erforderlich sind, und Annahmen über den Kontext der Dienste.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Smartcardschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758389"
---
# <a name="smart-card-interfaces"></a><span data-ttu-id="67055-103">Smartcardschnittstellen</span><span class="sxs-lookup"><span data-stu-id="67055-103">Smart Card Interfaces</span></span>

<span data-ttu-id="67055-104">Eine [*smartcardschnittstelle*](../secgloss/s-gly.md) besteht aus einem vordefinierten Satz von Diensten, die auf einer *Smartcard* verfügbar sind, den Protokollen, die zum Aufrufen der Dienste erforderlich sind, und Annahmen über den Kontext der Dienste.</span><span class="sxs-lookup"><span data-stu-id="67055-104">A [*smart card*](../secgloss/s-gly.md) interface consists of a predefined set of services available within a *smart card*, the protocols necessary to invoke the services, and any assumptions regarding the context of the services.</span></span>

<span data-ttu-id="67055-105">In Bezug auf Smartcards ähnelt der Begriff "Interface" der Art und Weise, wie er in com verwendet wird, was wiederum dem Konzept des ISO 7816/5-Anwendungs Bezeichners ähnlich ist, jedoch mit einem anderen Bereich.</span><span class="sxs-lookup"><span data-stu-id="67055-105">With respect to smart cards, the term "interface" is similar to how it is used in COM, which in turn is similar in concept to the ISO 7816/5 application identifier but with a different scope.</span></span>

<span data-ttu-id="67055-106">Jede Smartcard-Schnittstelle wird durch eine GUID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="67055-106">Each smart card interface is identified by a GUID.</span></span> <span data-ttu-id="67055-107">Beispielsweise kann eine Schnittstelle definiert werden, die dem Inhaber Biorhythmus Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="67055-107">For example, an interface might be defined that provides biorhythm information to its holder.</span></span> <span data-ttu-id="67055-108">Wenn dieser Dienst von einer bestimmten Smartcard unterstützt wird, kann dieser Anspruch darauf beanspruchen, diese Schnittstellen-GUID zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67055-108">If a given smart card supports this service, then it may claim to support that interface GUID.</span></span> <span data-ttu-id="67055-109">Mithilfe der Schnittstellen-GUIDs kann eine Anwendung nach einem bestimmten Satz von Schnittstellen suchen, um eine beliebige Karte zu suchen, die diese Gruppe unterstützt, um eine Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="67055-109">Using the interface GUIDs, an application may search for a particular set of interfaces, locating any card that supports that set, to complete a task.</span></span>

<span data-ttu-id="67055-110">Obwohl eine Schnittstelle über eine GUID verfügt, kann Sie auf unterschiedlichen Karten anders implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="67055-110">Although an interface has one GUID, it might be implemented differently on different cards.</span></span> <span data-ttu-id="67055-111">Die oben erwähnte Biorhythm-Schnittstelle kann z. b. über mehrere verschiedene Implementierungen verfügen, aber auf alle wird mit derselben GUID verwiesen.</span><span class="sxs-lookup"><span data-stu-id="67055-111">For example, the biorhythm interface mentioned above can have several different implementations, yet all are referenced using the same GUID.</span></span> <span data-ttu-id="67055-112">Durch die verschiedenen Implementierungen wird die Interaktion zwischen der Anwendung und der Smartcard nicht geändert. die Interaktion zwischen dem [*Dienstanbieter*](../secgloss/c-gly.md) und den Smartcards kann jedoch abhängig von der Implementierung der Schnittstelle abweichen.</span><span class="sxs-lookup"><span data-stu-id="67055-112">The different implementations would not change the interaction between the application and the smart card; however, the interaction between the [*service provider*](../secgloss/c-gly.md) and the smart cards may differ depending on the interface's implementation.</span></span>

<span data-ttu-id="67055-113">Der Satz von Schnittstellen, die von einer Smartcard unterstützt werden, wird während der Einführung in die Smartcard definiert (Weitere Informationen finden [Sie unter Einführung in Smartcards](introducing-smart-cards-to-the-system.md)</span><span class="sxs-lookup"><span data-stu-id="67055-113">The set of interfaces supported by a smart card is defined during smart card introduction (see [Introducing Smart Cards to the System](introducing-smart-cards-to-the-system.md)).</span></span>

 

 
