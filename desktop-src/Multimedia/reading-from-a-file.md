---
title: Lesen aus einer Datei
description: Lesen aus einer Datei
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- Avifileingefo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037379"
---
# <a name="reading-from-a-file"></a><span data-ttu-id="a4617-104">Lesen aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="a4617-104">Reading from a File</span></span>

<span data-ttu-id="a4617-105">Mithilfe der [**avifileinfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) -Funktion können Sie Informationen zu einer geöffneten Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="a4617-105">You can retrieve information about an open file by using the [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) function.</span></span> <span data-ttu-id="a4617-106">Diese Funktion füllt die [**avifileinfo**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) -Struktur mit den folgenden Informationen aus: die maximale Datenrate, die Anzahl der Streams in der Datei, ob die Datei einen Index verwendet und ob die Datei urheberrechtlich geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="a4617-106">This function fills the [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) structure with such information as the maximum data rate, the number of streams in the file, whether the file uses an index, and whether the file is copyrighted.</span></span>

<span data-ttu-id="a4617-107">Um ergänzende Informationen in einer AVI-Datei abzurufen, verwenden Sie die [**avifilereaddata**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a4617-107">To retrieve supplementary information in an AVI file, use the [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) function.</span></span> <span data-ttu-id="a4617-108">Ergänzende Informationen gelten für die gesamte Datei und sind nicht in den normalen Datei Headern enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4617-108">Supplementary information is applicable to the entire file and is not included in the normal file headers.</span></span> <span data-ttu-id="a4617-109">Beispielsweise kann der Name des Unternehmens oder der Person, der die Urheberrechte einer Datei besitzt, zusätzliche Informationen sein.</span><span class="sxs-lookup"><span data-stu-id="a4617-109">For example, the name of the company or person who holds the copyrights of a file could be supplementary information.</span></span> <span data-ttu-id="a4617-110">Ergänzende Informationen entsprechen nicht einem bestimmten Format. Sie kann Datei spezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="a4617-110">Supplementary information does not adhere to a specific format; it can be file specific.</span></span> <span data-ttu-id="a4617-111">**Avifilereaddata** gibt die ergänzenden Informationen in einem von der Anwendung bereitgestellten Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="a4617-111">**AVIFileReadData** returns the supplementary information in an application-supplied buffer.</span></span>

 

 




