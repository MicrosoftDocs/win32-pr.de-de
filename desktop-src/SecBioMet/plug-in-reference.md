---
title: Plug-in-Referenz
description: Adapter Funktionen, Wrapper Funktionen und Strukturen zum Erstellen von benutzerdefinierten Plug-in-Adaptern von drei Typen Engine, Sensor und Storage.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API Windows-Biometrieframework API für Windows-Biometrieframework API, Plug-in-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471701"
---
# <a name="plug-in-reference"></a><span data-ttu-id="76d27-104">Plug-in-Referenz</span><span class="sxs-lookup"><span data-stu-id="76d27-104">Plug-in Reference</span></span>

<span data-ttu-id="76d27-105">Biometrische Geräte werden in einer Vielzahl von Typen und Konfigurationen gefertigt.</span><span class="sxs-lookup"><span data-stu-id="76d27-105">Biometric devices are manufactured in a wide variety of types and configurations.</span></span> <span data-ttu-id="76d27-106">Der Windows-Biometrieframework enthält eine erweiterbare Architektur, die es Ihnen ermöglicht, diese Vielfalt durch das Erstellen von benutzerdefinierten Plug-ins zu behandeln. Im Mittelpunkt dieser Architektur befindet sich ein Software Objekt, das als biometrische Einheit bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="76d27-106">The Windows Biometric Framework incorporates an extensible architecture that enables you to deal with this variety by creating custom plug-ins. At the center of this architecture is a software object called a biometric unit.</span></span> <span data-ttu-id="76d27-107">Sie können sich eine biometrische Einheit als Abstraktion vorstellen, die ein biometrisches Gerät für das Framework darstellt.</span><span class="sxs-lookup"><span data-stu-id="76d27-107">You can think of a biometric unit as an abstraction that represents a biometric device to the Framework.</span></span> <span data-ttu-id="76d27-108">Plug-in-Softwarekomponenten, die als Adapter bezeichnet werden, verbinden die biometrische Einheit mit der zugeordneten Hardware.</span><span class="sxs-lookup"><span data-stu-id="76d27-108">Plug-in software components called adapters connect the biometric unit to the associated hardware.</span></span> <span data-ttu-id="76d27-109">Es gibt drei Arten von Adaptern, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="76d27-109">There are three types of adapters that you can create.</span></span> <span data-ttu-id="76d27-110">Ein Engine-Adapter generiert biometrische Vorlagen aus aufgezeichneten Beispielen, entspricht Beispielen für vorhandene Vorlagen und Index Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="76d27-110">An engine adapter generates biometric templates from captured samples, matches samples to existing templates, and indexes templates.</span></span> <span data-ttu-id="76d27-111">Ein Sensor Adapter dient als Wrapper für ein biometrisches Gerät und stellt eine Standardschnittstelle zum Konfigurieren des Sensors, zum Erfassen von Beispielen und zum Steuern des Flusses biometrischer Daten an die Verarbeitungs-Engine bereit.</span><span class="sxs-lookup"><span data-stu-id="76d27-111">A sensor adapter wraps a biometric device and provides a standard interface for configuring the sensor, capturing samples, and controlling the flow of biometric data to the processing engine.</span></span> <span data-ttu-id="76d27-112">Ein Speicher Adapter verwaltet Vorlagen Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="76d27-112">A storage adapter manages template databases.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="76d27-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="76d27-113">In this section</span></span>



| <span data-ttu-id="76d27-114">Thema</span><span class="sxs-lookup"><span data-stu-id="76d27-114">Topic</span></span>                                                                 | <span data-ttu-id="76d27-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76d27-115">Description</span></span>                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76d27-116">Plug-in-Funktionen</span><span class="sxs-lookup"><span data-stu-id="76d27-116">Plug-in Functions</span></span>](plug-in-functions.md)<br/>                 | <span data-ttu-id="76d27-117">Funktionen, die Sie verwenden können, um die Adapter-Plug-ins zu erstellen, die eine biometrische Einheit bilden.</span><span class="sxs-lookup"><span data-stu-id="76d27-117">Functions you can use to create the adapter plug-ins that make up a biometric unit.</span></span><br/>                                                                     |
| [<span data-ttu-id="76d27-118">Plug-in-Strukturen</span><span class="sxs-lookup"><span data-stu-id="76d27-118">Plug-in Structures</span></span>](plug-in-structures.md)<br/>               | <span data-ttu-id="76d27-119">Strukturen für die Entwicklung von Client Anwendungen durch die Windows-Biometrieframework-API.</span><span class="sxs-lookup"><span data-stu-id="76d27-119">Structures for client application development by the Windows Biometric Framework API.</span></span><br/>                                                                   |
| [<span data-ttu-id="76d27-120">Plug-in-Wrapper Funktionen</span><span class="sxs-lookup"><span data-stu-id="76d27-120">Plug-in Wrapper Functions</span></span>](plug-in-wrapper-functions.md)<br/> | <span data-ttu-id="76d27-121">Wrapper Funktionen, die es Ihnen ermöglichen, eine öffentliche Funktion auf jedem Adapter aufzurufen, der an die Pipeline angefügt ist, ohne manuell einen Zeiger auf den Adapter zu beschaffen.</span><span class="sxs-lookup"><span data-stu-id="76d27-121">Wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span><br/> |



 

 

 





