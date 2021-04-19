---
description: Um die Elemente eines Pfads abzurufen, rufen Sie die pdhparser-counterpath-Funktion auf. Die-Funktion analysiert die Elemente eines Counter-Pfads und gibt Sie in einer PDH- \_ counter- \_ Pfad \_ Elementstruktur zurück.
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Abrufen von Counter-Pfad Elementen aus einem Counter-Pfad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362470"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a><span data-ttu-id="c7bb7-104">Abrufen von Counter-Pfad Elementen aus einem Counter-Pfad</span><span class="sxs-lookup"><span data-stu-id="c7bb7-104">Obtaining Counter Path Elements from a Counter Path</span></span>

<span data-ttu-id="c7bb7-105">Um die Elemente eines Pfads abzurufen, rufen Sie die [**pdhparser-counterpath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="c7bb7-105">To retrieve the elements of a path, call the [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) function.</span></span> <span data-ttu-id="c7bb7-106">Die-Funktion analysiert die Elemente eines Counter-Pfads und gibt Sie in einer [**PDH- \_ counter- \_ Pfad \_ Element**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="c7bb7-106">The function parses the elements of a counter path and returns them in a [**PDH\_COUNTER\_PATH\_ELEMENTS**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) structure.</span></span>

<span data-ttu-id="c7bb7-107">Wenn Sie über einen komplexen Instanznamen verfügen (einen, der eine übergeordnete Instanz und einen Instanzindex enthält), können Sie die [**pdhparser seinstancename**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) -Funktion aufrufen, um den Instanznamen, den Instanzindex und den übergeordneten Namen zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c7bb7-107">If you have a complex instance name (one that contains a parent instance and instance index), you can call the [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) function to extract the instance name, instance index, and parent name.</span></span>

 

 



