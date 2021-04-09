---
description: Nachdem die INF-Datei geöffnet wurde, können Sie Informationen daraus sammeln, um die Benutzeroberfläche zu erstellen, oder den Installationsprozess weiterleiten. Die Setup-Funktionen bieten mehrere Ebenen der Funktionalität zum Sammeln von Informationen aus einer INF-Datei.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Extrahieren von Dateiinformationen aus der INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862999"
---
# <a name="extracting-file-information-from-the-inf-file"></a><span data-ttu-id="70ff2-104">Extrahieren von Dateiinformationen aus der INF-Datei</span><span class="sxs-lookup"><span data-stu-id="70ff2-104">Extracting File Information from the INF file</span></span>

<span data-ttu-id="70ff2-105">Nachdem die INF-Datei geöffnet wurde, können Sie Informationen daraus sammeln, um die Benutzeroberfläche zu erstellen, oder den Installationsprozess weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="70ff2-105">After the INF file is opened, you can gather information from it to build the user interface, or to direct the installation process.</span></span> <span data-ttu-id="70ff2-106">Die Setup-Funktionen bieten mehrere Ebenen der Funktionalität zum Sammeln von Informationen aus einer INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="70ff2-106">The setup functions provide several levels of functionality for gathering information from an INF file.</span></span>



| <span data-ttu-id="70ff2-107">Um Informationen zu erfassen...</span><span class="sxs-lookup"><span data-stu-id="70ff2-107">To gather information…</span></span>                | <span data-ttu-id="70ff2-108">Diese Funktionen verwenden...</span><span class="sxs-lookup"><span data-stu-id="70ff2-108">Use these functions…</span></span>                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="70ff2-109">Informationen zur INF-Datei</span><span class="sxs-lookup"><span data-stu-id="70ff2-109">About the INF file</span></span>                    | [<span data-ttu-id="70ff2-110">**Setupgetinfinformation**</span><span class="sxs-lookup"><span data-stu-id="70ff2-110">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [<span data-ttu-id="70ff2-111">**Setupqueryinffileinformation**</span><span class="sxs-lookup"><span data-stu-id="70ff2-111">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | <span data-ttu-id="70ff2-112">[**Setupqueryinfversioninformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span><span class="sxs-lookup"><span data-stu-id="70ff2-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span></span> |
| <span data-ttu-id="70ff2-113">Informationen zu Quell-und Zieldateien</span><span class="sxs-lookup"><span data-stu-id="70ff2-113">About source and target files</span></span>         | [<span data-ttu-id="70ff2-114">**Setupgetsourcefileloation**</span><span class="sxs-lookup"><span data-stu-id="70ff2-114">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [<span data-ttu-id="70ff2-115">**Setupgetsourcefilesize**</span><span class="sxs-lookup"><span data-stu-id="70ff2-115">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [<span data-ttu-id="70ff2-116">**Setupgettargetpath**</span><span class="sxs-lookup"><span data-stu-id="70ff2-116">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [<span data-ttu-id="70ff2-117">**Setupgetsourceinfo**</span><span class="sxs-lookup"><span data-stu-id="70ff2-117">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| <span data-ttu-id="70ff2-118">Aus einer Zeile einer INF-Datei</span><span class="sxs-lookup"><span data-stu-id="70ff2-118">From a line of an INF file</span></span>            | [<span data-ttu-id="70ff2-119">**Setupgetlinetext**</span><span class="sxs-lookup"><span data-stu-id="70ff2-119">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [<span data-ttu-id="70ff2-120">**Setupfindnextline**</span><span class="sxs-lookup"><span data-stu-id="70ff2-120">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [<span data-ttu-id="70ff2-121">**Setupfindnextmatchline**</span><span class="sxs-lookup"><span data-stu-id="70ff2-121">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [<span data-ttu-id="70ff2-122">**Setupgetlinebyindex**</span><span class="sxs-lookup"><span data-stu-id="70ff2-122">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [<span data-ttu-id="70ff2-123">**Setupfindfirstline**</span><span class="sxs-lookup"><span data-stu-id="70ff2-123">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| <span data-ttu-id="70ff2-124">Aus einem Feld einer Zeile in einer INF-Datei</span><span class="sxs-lookup"><span data-stu-id="70ff2-124">From a field of a line in an INF file</span></span> | [<span data-ttu-id="70ff2-125">**Setupgetstringfield**</span><span class="sxs-lookup"><span data-stu-id="70ff2-125">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [<span data-ttu-id="70ff2-126">**Setupgetintfield**</span><span class="sxs-lookup"><span data-stu-id="70ff2-126">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [<span data-ttu-id="70ff2-127">**Setupgetbinaryfield**</span><span class="sxs-lookup"><span data-stu-id="70ff2-127">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [<span data-ttu-id="70ff2-128">**Setupgetmultiszfield**</span><span class="sxs-lookup"><span data-stu-id="70ff2-128">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

<span data-ttu-id="70ff2-129">Im folgenden Beispiel wird die [**setupgetsourceinfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) -Funktion verwendet, um die lesbare Beschreibung eines Quell Mediums aus einer INF-Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="70ff2-129">The following example uses the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function to retrieve the human-readable description of a source media from an INF file.</span></span>


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



<span data-ttu-id="70ff2-130">Im Beispiel ist myinf das Handle der geöffneten INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="70ff2-130">In the example, MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="70ff2-131">SourceID ist der Bezeichner für ein bestimmtes Quell Medium.</span><span class="sxs-lookup"><span data-stu-id="70ff2-131">SourceId is the identifier for a specific source media.</span></span> <span data-ttu-id="70ff2-132">Der Wert srcinfo \_ Description gibt an, dass die [**setupgetsourceinfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) -Funktion die Quell Medien Beschreibung abrufen soll.</span><span class="sxs-lookup"><span data-stu-id="70ff2-132">The value SRCINFO\_DESCRIPTION specifies that the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function should retrieve the source media description.</span></span> <span data-ttu-id="70ff2-133">Der Puffer zeigt auf eine Zeichenfolge, die die Beschreibung empfängt, maxbufsize gibt die dem Puffer zugeordneten Ressourcen an, und "bufsize" gibt die Ressourcen an, die zum Speichern des Puffers benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="70ff2-133">Buffer points to a string that will receive the description, MaxBufSize indicates the resources allocated to the buffer, and BufSize indicates the resources necessary to store the buffer.</span></span>

<span data-ttu-id="70ff2-134">Wenn "bufsize" größer als "maxbufsize" ist, gibt die Funktion " **false**" zurück, und ein nachfolgendes Aufrufen von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt einen fehlerhaften \_ Puffer zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="70ff2-134">If BufSize is greater than MaxBufSize, the function will return **FALSE**, and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return ERROR\_INSUFFICIENT\_BUFFER.</span></span>

 

 
