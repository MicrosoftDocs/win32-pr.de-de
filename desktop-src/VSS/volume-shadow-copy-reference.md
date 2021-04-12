---
description: Der Volumeschattenkopie-Dienst (VSS) ist ein Satz von com-und C++-APIs, mit denen Volumesicherungen ausgeführt werden können, während Anwendungen auf dem System (als Writer bezeichnet) weiterhin auf den Volumes schreiben.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Volumen Schatten Kopie-API-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526294"
---
# <a name="volume-shadow-copy-api-reference"></a><span data-ttu-id="2f900-103">Volumen Schatten Kopie-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="2f900-103">Volume Shadow Copy API Reference</span></span>

<span data-ttu-id="2f900-104">Der Volumeschattenkopie-Dienst (VSS) ist ein Satz von com-und C++-APIs, mit denen Volumesicherungen ausgeführt werden können, während Anwendungen auf dem System (als Writer bezeichnet) weiterhin auf den Volumes schreiben.</span><span class="sxs-lookup"><span data-stu-id="2f900-104">The Volume Shadow Copy Service (VSS) is a set of COM and C++ APIs that enable volume backups to be performed while applications on the system (called writers) continue to write to the volumes.</span></span>

<span data-ttu-id="2f900-105">VSS unterstützt diese Sicherungen durch die Erstellung von Schatten Kopien, ein Duplikat des ursprünglichen Volumes zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="2f900-105">VSS supports these backups through the creation of shadow copies, a duplicate of the original volume at a given point in time.</span></span>

<span data-ttu-id="2f900-106">Entwickler von Drittanbietern können mit der VSS-API Anforderer (z. b. eine Sicherungs Anwendung) zum Erstellen und Verwalten von Schatten Kopien erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f900-106">Third-party developers can use the VSS API to create requesters (such as a backup application) to create and manage shadow copies.</span></span>

<span data-ttu-id="2f900-107">Die tatsächliche Erstellung und Darstellung von Schatten Kopien erfolgt durch Anwendungen auf Systemebene, die als Anbieter bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="2f900-107">The actual work of creating and representing shadow copies is conducted by system-level applications known as providers.</span></span>

<span data-ttu-id="2f900-108">Entwickler können die API auch zum Erstellen von Writern verwenden: VSS-fähige Anwendungen, die e/a-Vorgänge mit der Erstellung und Bearbeitung von Schatten Kopien koordinieren können.</span><span class="sxs-lookup"><span data-stu-id="2f900-108">Developers can also use the API to construct writers: VSS-aware applications that are able to coordinate I/O operations with the creation and manipulation of shadow copies.</span></span>

-   [<span data-ttu-id="2f900-109">Volumen Schatten Kopie-API-Klassen</span><span class="sxs-lookup"><span data-stu-id="2f900-109">Volume Shadow Copy API Classes</span></span>](volume-shadow-copy-api-classes.md)
-   [<span data-ttu-id="2f900-110">Datentypen der Volumeschattenkopie-API</span><span class="sxs-lookup"><span data-stu-id="2f900-110">Volume Shadow Copy API Data Types</span></span>](volume-shadow-copy-api-data-types.md)
-   [<span data-ttu-id="2f900-111">Volumeschattenkopie-API-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="2f900-111">Volume Shadow Copy API Enumerations</span></span>](volume-shadow-copy-api-enumeration-types.md)
-   [<span data-ttu-id="2f900-112">Volumen Schatten Kopie-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2f900-112">Volume Shadow Copy API Functions</span></span>](volume-shadow-copy-api-functions.md)
-   [<span data-ttu-id="2f900-113">Volumeschattenkopie-API</span><span class="sxs-lookup"><span data-stu-id="2f900-113">Volume Shadow Copy API Interfaces</span></span>](volume-shadow-copy-api-interfaces.md)
-   [<span data-ttu-id="2f900-114">Volumen Schatten Kopie-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2f900-114">Volume Shadow Copy API Structures</span></span>](volume-shadow-copy-api-structures.md)
-   [<span data-ttu-id="2f900-115">Glossar der Volumeschattenkopie</span><span class="sxs-lookup"><span data-stu-id="2f900-115">Volume Shadow Copy Glossary</span></span>](volume-shadow-copy-glossary.md)

<span data-ttu-id="2f900-116">Weitere Informationen zum Schreiben von Anforderern und Writern finden [Sie unter Verwenden der Volumeschattenkopie-Dienst](using-the-volume-shadow-copy-service.md).</span><span class="sxs-lookup"><span data-stu-id="2f900-116">For more information on writing requesters and writers, see [Using the Volume Shadow Copy Service](using-the-volume-shadow-copy-service.md).</span></span>

 

 



