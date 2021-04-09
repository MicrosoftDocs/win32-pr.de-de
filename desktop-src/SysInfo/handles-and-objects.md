---
description: Bei einem Objekt handelt es sich um eine Datenstruktur, die eine System Ressource darstellt, z. b. eine Datei, einen Thread oder ein Grafik Bild.
ms.assetid: 26aaad09-c1e1-46e8-9cd3-7d795a10d900
title: Handles und Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b5a35d55571a01f2f186f4e756401582474949f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868167"
---
# <a name="handles-and-objects"></a><span data-ttu-id="23cbc-103">Handles und Objekte</span><span class="sxs-lookup"><span data-stu-id="23cbc-103">Handles and Objects</span></span>

<span data-ttu-id="23cbc-104">Bei einem *Objekt* handelt es sich um eine Datenstruktur, die eine System Ressource darstellt, z. b. eine Datei, einen Thread oder ein Grafik Bild.</span><span class="sxs-lookup"><span data-stu-id="23cbc-104">An *object* is a data structure that represents a system resource, such as a file, thread, or graphic image.</span></span> <span data-ttu-id="23cbc-105">Eine Anwendung kann nicht direkt auf Objektdaten oder die System Ressource zugreifen, die ein Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="23cbc-105">An application cannot directly access object data or the system resource that an object represents.</span></span> <span data-ttu-id="23cbc-106">Stattdessen benötigt eine Anwendung ein Objekt *handle*, das zum Überprüfen oder Ändern der System Ressource verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="23cbc-106">Instead, an application must obtain an object *handle*, which it can use to examine or modify the system resource.</span></span> <span data-ttu-id="23cbc-107">Jedes Handle verfügt über einen Eintrag in einer intern verwalteten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="23cbc-107">Each handle has an entry in an internally maintained table.</span></span> <span data-ttu-id="23cbc-108">Diese Einträge enthalten die Adressen der Ressourcen und die Mittel zum Identifizieren des Ressourcentyps.</span><span class="sxs-lookup"><span data-stu-id="23cbc-108">These entries contain the addresses of the resources and the means to identify the resource type.</span></span>

-   [<span data-ttu-id="23cbc-109">Informationen zu Handles und Objekten</span><span class="sxs-lookup"><span data-stu-id="23cbc-109">About Handles and Objects</span></span>](about-handles-and-objects.md)
-   [<span data-ttu-id="23cbc-110">Objektkategorien</span><span class="sxs-lookup"><span data-stu-id="23cbc-110">Object Categories</span></span>](object-categories.md)
-   [<span data-ttu-id="23cbc-111">Handle und Objekt Verweis</span><span class="sxs-lookup"><span data-stu-id="23cbc-111">Handle and Object Reference</span></span>](handle-and-object-reference.md)

 

 



