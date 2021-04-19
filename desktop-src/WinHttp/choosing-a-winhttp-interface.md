---
description: Bevor Sie mit der Entwicklung einer Microsoft Windows HTTP-Dienste (WinHTTP)-Anwendung beginnen, müssen Sie zunächst entscheiden, ob Sie die C/C++-API oder die COM-Schnittstelle verwenden möchten.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Auswählen einer WinHTTP-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362523"
---
# <a name="choosing-a-winhttp-interface"></a><span data-ttu-id="0945d-103">Auswählen einer WinHTTP-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0945d-103">Choosing a WinHTTP Interface</span></span>

<span data-ttu-id="0945d-104">Bevor Sie mit der Entwicklung einer Microsoft Windows HTTP-Dienste (WinHTTP)-Anwendung beginnen, müssen Sie zunächst entscheiden, ob Sie die C/C++-API oder die COM-Schnittstelle verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="0945d-104">Before you begin to develop a Microsoft Windows HTTP Services (WinHTTP) application, you must first decide whether to use the C/C++ API or the COM interface.</span></span> <span data-ttu-id="0945d-105">In der folgenden Tabelle werden die vor-und Nachteile der einzelnen Ansätze zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="0945d-105">The following table summarizes the advantages and disadvantages associated with each of these approaches.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0945d-106">C/C++-API</span><span class="sxs-lookup"><span data-stu-id="0945d-106">C/C++ API</span></span></th>
<th><span data-ttu-id="0945d-107">COM-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0945d-107">COM interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0945d-108">Vorteile</span><span class="sxs-lookup"><span data-stu-id="0945d-108">Advantages</span></span></td>
<td><ul>
<li><span data-ttu-id="0945d-109">Antworten können in Blöcken verarbeitet werden, was effizienter ist.</span><span class="sxs-lookup"><span data-stu-id="0945d-109">Responses can be processed in chunks, which is more efficient.</span></span></li>
<li><span data-ttu-id="0945d-110">Post-Vorgänge können auch in Blöcken verarbeitet werden, um die Verarbeitungszeit zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="0945d-110">POST operations can also be processed in chunks, speeding processing time.</span></span></li>
<li><span data-ttu-id="0945d-111">AutoProxy-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="0945d-111">AutoProxy support.</span></span></li>
<li><span data-ttu-id="0945d-112">Zugriff auf den vollständigen Featuresatz von WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="0945d-112">Access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="0945d-113">Binäre Daten können problemlos behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="0945d-113">Binary data can easily be handled.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0945d-114">Das Erstellen einer Anwendung ist einfach und erfordert weniger Codezeilen als die C/C++-API.</span><span class="sxs-lookup"><span data-stu-id="0945d-114">Creating an application is easy and requires fewer lines of code than the C/C++ API.</span></span></li>
<li><span data-ttu-id="0945d-115">Die-Schnittstelle kann von Skriptsprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0945d-115">The interface can be used by scripting languages.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0945d-116">Nachteile</span><span class="sxs-lookup"><span data-stu-id="0945d-116">Disadvantages</span></span></td>
<td><ul>
<li><span data-ttu-id="0945d-117">Die Verarbeitung ist komplexer.</span><span class="sxs-lookup"><span data-stu-id="0945d-117">Processing is more complex.</span></span></li>
<li><span data-ttu-id="0945d-118">Die C/C++-API erfordert mehr Schritte als die COM-Schnittstelle, um die gleichen Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0945d-118">The C/C++ API requires more steps than the COM interface to perform the same actions.</span></span></li>
<li><span data-ttu-id="0945d-119">Das Einrichten einer Anforderung erfordert mehr Code.</span><span class="sxs-lookup"><span data-stu-id="0945d-119">Setting up a request takes more code.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0945d-120">Die COM-Schnittstelle bietet keinen Zugriff auf den vollständigen Featuresatz von WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="0945d-120">The COM interface does not provide access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="0945d-121">Es ist schwierig, Binär Datentypen in einigen Skriptsprachen wie VBScript und JScript zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0945d-121">It is difficult to handle binary data types in some scripting languages, such as VBScript and JScript.</span></span></li>
<li><span data-ttu-id="0945d-122">Die COM-Schnittstelle unterstützt AutoProxy nicht.</span><span class="sxs-lookup"><span data-stu-id="0945d-122">The COM interface does not support AutoProxy.</span></span></li>
<li><span data-ttu-id="0945d-123">Anwendungen müssen das com-APARTMENT_THREADED Modell verwenden.</span><span class="sxs-lookup"><span data-stu-id="0945d-123">Applications must use the COM APARTMENT_THREADED model.</span></span></li>
<li><span data-ttu-id="0945d-124">Bevor eine Antwort verarbeitet werden kann, muss zuerst die gesamte Antwort empfangen und gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="0945d-124">Before a response can begin being processed, the entire response must first be received and buffered.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



