---
description: Beschreibung der Möglichkeiten zum Verbessern der Leistung bei Verwendung der StylusInput-APIs (Application Programming Interfaces).
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Überlegungen zur Leistung der StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759805"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a><span data-ttu-id="4d4b9-103">Überlegungen zur Leistung der StylusInput-API</span><span class="sxs-lookup"><span data-stu-id="4d4b9-103">Performance Considerations for the StylusInput API</span></span>

<span data-ttu-id="4d4b9-104">In der folgenden Liste werden einige Möglichkeiten beschrieben, wie Sie die Leistung von Anwendungen verbessern können, die die StylusInput-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d4b9-104">The following list describes some ways in which to improve the performance of applications that use the StylusInput APIs.</span></span>

-   <span data-ttu-id="4d4b9-105">Verwenden Sie die Eigenschaft [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) oder [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) , um nur die für Ihr Plug-in relevanten Daten zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="4d4b9-105">Use the [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) property to subscribe only to the data that is relevant to your plug-in.</span></span> <span data-ttu-id="4d4b9-106">Dadurch wird die Gesamtzahl der Methodenaufrufe verringert, die das [**RealTimeStylus**](realtimestylus-class.md) -Objekt vornimmt, und die Komplexität des Plug-ins wird reduziert.</span><span class="sxs-lookup"><span data-stu-id="4d4b9-106">This reduces the overall number of method calls the [**RealTimeStylus**](realtimestylus-class.md) object makes and also reduces the complexity of your plug-in.</span></span> <span data-ttu-id="4d4b9-107">Das **RealTimeStylus** -Objekt überprüft nur die DataInterest-Eigenschaft, wenn das Plug-in angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4d4b9-107">The **RealTimeStylus** object only checks the DataInterest property when the plug-in is attached.</span></span>
-   <span data-ttu-id="4d4b9-108">Minimieren Sie die Komplexität synchrone Plug-ins. Synchrone Plug-ins, die in der Regel vom Thread des [**RealTimeStylus**](realtimestylus-class.md) -Objekts aufgerufen werden und zu Verzögerungen bei der frei Hand Eingabe beitragen können.</span><span class="sxs-lookup"><span data-stu-id="4d4b9-108">Minimize the complexity of synchronous plug-ins. Synchronous plug-ins generally called by the [**RealTimeStylus**](realtimestylus-class.md) object's thread and may contribute to delays in ink collection.</span></span>
-   <span data-ttu-id="4d4b9-109">Ziehen Sie in Erwägung, das Plug-in asynchron zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="4d4b9-109">Consider making your plug-in asynchronous.</span></span> <span data-ttu-id="4d4b9-110">Wenn das Plug-in Komplex ist und der Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts benutzerdefinierte Daten hinzugefügt werden müssen, empfiehlt es sich, ein kaskadierenden- **RealTimeStylus** -Modell zu verwenden und das Plug-in zur synchronen Plug-in-Auflistung des sekundären **RealTimeStylus** -Objekts hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d4b9-110">If your plug-in is complex and needs to add custom data to the [**RealTimeStylus**](realtimestylus-class.md) object's queue, consider using a cascaded **RealTimeStylus** model and adding the plug-in to the secondary **RealTimeStylus** object's synchronous plug-in collection.</span></span> <span data-ttu-id="4d4b9-111">Weitere Informationen zum kaskadierenden **RealTimeStylus** -Modell finden Sie [im kaskadierenden RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="4d4b9-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

 

 
