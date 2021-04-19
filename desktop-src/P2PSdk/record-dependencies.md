---
description: Die Peer Infrastruktur garantiert nicht die Reihenfolge für den Empfang und die Verarbeitung von Datensätzen.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Daten Satz Abhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367942"
---
# <a name="record-dependencies"></a><span data-ttu-id="3dea6-103">Daten Satz Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="3dea6-103">Record Dependencies</span></span>

<span data-ttu-id="3dea6-104">Die Peer Infrastruktur garantiert nicht die Reihenfolge für den Empfang und die Verarbeitung von Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="3dea6-104">The Peer Infrastructure does not guarantee the order for receiving and processing records.</span></span> <span data-ttu-id="3dea6-105">Wenn Ihre Anwendung Daten Satz Abhängigkeiten aufweist, was bedeutet, dass die Verarbeitung oder Validierung eines Datensatzes von einem anderen Datensatz abhängig ist, muss die Anwendung in der Lage sein, Situationen zu verarbeiten, in denen Datensätze in beliebiger und unvorhersehbarer Reihenfolge empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="3dea6-105">If your application has record dependencies, which means that the processing or validation of one record relies on another record, then your application must be able to handle situations when records might be received in an arbitrary and unpredictable order.</span></span> <span data-ttu-id="3dea6-106">Eine Chat-Anwendung kann z. b. zwei Arten von Datensätzen aufweisen: einen Datensatz, der Informationen zu einem bestimmten Benutzer enthält, und einen Datensatz, der eine Chat Nachricht enthält, die auf den Benutzerdaten Satz verweist.</span><span class="sxs-lookup"><span data-stu-id="3dea6-106">For example, a chat application may have two types of records: a record that contains information about a specific user, and a record that contains a chat message that refers to the user record.</span></span>

<span data-ttu-id="3dea6-107">Eine Anwendung muss in der Lage sein, die Situation zu behandeln, in der ein Chat Nachrichten Daten Satz vor dem Benutzerdaten Satz für die Chat Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="3dea6-107">An application must be able to handle the situation when a chat message record is received before the user record for the chat message.</span></span> <span data-ttu-id="3dea6-108">Eine Möglichkeit, die Situation zu behandeln, besteht darin, auf den Benutzerdaten Satz zu warten, indem eine Liste mit einer **Liste** oder ein Cache und ein Timer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3dea6-108">One way to handle the situation is to wait for the user record by using a **stand-by list**, or a cache and timer.</span></span> <span data-ttu-id="3dea6-109">Die Anwendung kann jeden Datensatz in der Liste oder im Cache regelmäßig überprüfen und dann die Situation behandeln, in der der erforderliche Benutzerdaten Satz empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="3dea6-109">The application can periodically examine each record in the list or cache, and then handle the situation when the required user record is received.</span></span>

<span data-ttu-id="3dea6-110">Zum Verarbeiten von Daten Satz Abhängigkeiten besteht eine gut entworfene Anwendung aus folgendem:</span><span class="sxs-lookup"><span data-stu-id="3dea6-110">To handle record dependencies, a well-designed application consists of the following:</span></span>

-   <span data-ttu-id="3dea6-111">Sucht vor dem Ausführen einer Aktion stets nach Daten Satz Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="3dea6-111">Always checks for record dependencies before performing an action.</span></span>
-   <span data-ttu-id="3dea6-112">Erwartet Bedingungen, die auftreten können, wenn Datensätze in unerwarteter Reihenfolge empfangen werden, und dann die Situation behandelt.</span><span class="sxs-lookup"><span data-stu-id="3dea6-112">Anticipates conditions that might occur when records are received in an unexpected order, and then handles the situation.</span></span>

 

 



