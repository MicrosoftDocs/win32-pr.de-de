---
title: Erweiterte Fehlerinformationen für den Benutzer
description: Wenn erweiterte Fehlerinformationen verfügbar sind, müssen die Komponenten, die an der Erstellung der erweiterten Fehlerinformationen beteiligt sind, das Problem leichter finden.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856303"
---
# <a name="extended-error-information-for-the-user"></a><span data-ttu-id="f1ede-103">Erweiterte Fehlerinformationen für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="f1ede-103">Extended Error Information for the User</span></span>

<span data-ttu-id="f1ede-104">Wenn erweiterte Fehlerinformationen verfügbar sind, müssen die Komponenten, die an der Erstellung der erweiterten Fehlerinformationen beteiligt sind, das Problem leichter finden.</span><span class="sxs-lookup"><span data-stu-id="f1ede-104">If extended error information is available, the components participating in the creation of the extended error information must make it easy to find the problem.</span></span> <span data-ttu-id="f1ede-105">Der erste Schritt besteht darin, den letzten erweiterten Fehler Daten Satz zu überprüfen und zu ermitteln, auf welchem Computer und an welchem Prozess das Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f1ede-105">The first step is to review the last extended error record, and determine on which computer and which process the problem originated.</span></span> <span data-ttu-id="f1ede-106">Dies ist häufig die Ursache für den RPC \_ - \_ \* Fehler.</span><span class="sxs-lookup"><span data-stu-id="f1ede-106">This is often the cause of the RPC\_S\_\* error.</span></span> <span data-ttu-id="f1ede-107">Suchen Sie den Erkennungs Speicherort, und legen Sie fest, was die Parameter für diesen Erkennungs Speicherort bedeuten.</span><span class="sxs-lookup"><span data-stu-id="f1ede-107">Find the detection location, and determine what the parameters for this detection location mean.</span></span> <span data-ttu-id="f1ede-108">Normalerweise geben Sie einen Fehler eines Funktions Aufrufes oder einer bestimmten Überprüfung an.</span><span class="sxs-lookup"><span data-stu-id="f1ede-108">Usually they indicate a failure of a function call or particular check.</span></span> <span data-ttu-id="f1ede-109">Legen Sie von dort aus fest, warum die Funktion oder die Überprüfung fehlschlägt, und ergreifen Sie Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="f1ede-109">From there, determine why the function or check fails, and take corrective action.</span></span>

<span data-ttu-id="f1ede-110">Die Datensätze vor dem letzten Datensatz geben den Pfad an, in dem der Fehler aufgetreten ist, und dienen in der Regel als Integritätsprüfung und nicht als hilfsanmeldungs Prozess.</span><span class="sxs-lookup"><span data-stu-id="f1ede-110">The records before the last record indicate the path by which the error arrived, and generally serve as a sanity check rather than an aide in the troubleshooting process.</span></span>

 

 




