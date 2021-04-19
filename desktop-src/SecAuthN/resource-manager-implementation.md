---
description: Der Ressourcen-Manager wird als vertrauenswürdiger Dienst in einem einzelnen Prozess ausgeführt. Alle Anforderungen für den Smartcardzugriff werden auf den Ressourcen-Manager gerichtet, der Sie an den Reader weiterleitet, der die Ziel Karte enthält.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Ressourcen-Manager-Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348590"
---
# <a name="resource-manager-implementation"></a><span data-ttu-id="c5f9c-104">Ressourcen-Manager-Implementierung</span><span class="sxs-lookup"><span data-stu-id="c5f9c-104">Resource Manager Implementation</span></span>

<span data-ttu-id="c5f9c-105">Der [*Ressourcen-Manager*](../secgloss/r-gly.md) wird als vertrauenswürdiger Dienst in einem einzelnen Prozess ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5f9c-105">The [*resource manager*](../secgloss/r-gly.md) runs as a trusted service in a single process.</span></span> <span data-ttu-id="c5f9c-106">Alle Anforderungen für den [*Smartcardzugriff*](../secgloss/s-gly.md) werden auf den Ressourcen-Manager gerichtet, der Sie an den [*Reader*](../secgloss/r-gly.md) weiterleitet, der die Ziel Karte enthält.</span><span class="sxs-lookup"><span data-stu-id="c5f9c-106">All requests for [*smart card*](../secgloss/s-gly.md) access are made to the resource manager, which routes them to the [*reader*](../secgloss/r-gly.md) that contains the targeted card.</span></span>

<span data-ttu-id="c5f9c-107">Smartcards werden häufig in Verbindung mit der Sicherheit und der persönlichen Privatsphäre verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5f9c-107">Smart cards are often used in conjunction with security and personal privacy.</span></span> <span data-ttu-id="c5f9c-108">Wenn möglich, verwendet der Ressourcen-Manager die Sicherheitsmechanismen, die im zugrunde liegenden Betriebssystem vorhanden sind, wenn Sie auf einen Reader oder eine Smartcard zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c5f9c-108">Wherever possible, the resource manager uses the security mechanisms existing within the underlying operating system when accessing a reader or smart card.</span></span>

 

 
