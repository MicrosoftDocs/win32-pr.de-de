---
description: Nachdem Sie ein Handle für eine INF-Datei haben, können Sie auf verschiedene Weise Informationen daraus abrufen. Funktionen wie setupgetinfinformation, setupqueryinffileinformation und setupqueryinfversioninformation rufen Informationen zur INF-Datei selbst ab.
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: Abrufen von Informationen aus einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347609"
---
# <a name="retrieving-information-from-an-inf-file"></a><span data-ttu-id="57f21-104">Abrufen von Informationen aus einer INF-Datei</span><span class="sxs-lookup"><span data-stu-id="57f21-104">Retrieving Information From an INF File</span></span>

<span data-ttu-id="57f21-105">Nachdem Sie ein Handle für eine INF-Datei haben, können Sie auf verschiedene Weise Informationen daraus abrufen.</span><span class="sxs-lookup"><span data-stu-id="57f21-105">After you have a handle to an INF file, you can retrieve information from it in a variety of ways.</span></span> <span data-ttu-id="57f21-106">Funktionen wie [**setupgetinfinformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**setupqueryinffileinformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)und [**setupqueryinfversioninformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) rufen Informationen zur INF-Datei selbst ab.</span><span class="sxs-lookup"><span data-stu-id="57f21-106">Functions such as [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa), and [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) retrieve information about the INF file itself.</span></span>

<span data-ttu-id="57f21-107">Andere Funktionen, wie z. b. [**setupgetsourceinfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) und [**setupgettargetpath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) , rufen Informationen zu den Quelldateien und Zielverzeichnissen ab.</span><span class="sxs-lookup"><span data-stu-id="57f21-107">Other functions such as [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) and [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) acquire information about the source files and target directories.</span></span>

<span data-ttu-id="57f21-108">Auf Low-Level-Funktionen wie " [**setupgetlinetext**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) " und " [**setupgetstringfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) " können Sie direkt auf Informationen zugreifen, die in einer Zeile oder einem Feld einer INF-Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="57f21-108">Low-level functions like [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) and [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) enable you to directly access information stored in a line or field of an INF file.</span></span> <span data-ttu-id="57f21-109">Diese Funktionen werden intern von den Funktionen auf höherer Ebene verwendet, sind aber auch verfügbar, wenn Sie auf der Zeilen-oder Feldebene auf INF-Informationen zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="57f21-109">These functions are used internally by the higher-level functions, but are also available should you need to access INF information at the line or field level.</span></span>

 

 



