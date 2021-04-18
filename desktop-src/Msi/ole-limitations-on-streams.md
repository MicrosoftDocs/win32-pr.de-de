---
description: Entwickler von Installations Datenbanken müssen zwei Einschränkungen bei der Behandlung von Streams durch die strukturierte Win32 OLE-Speicher Implementierung beachten.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: OLE-Einschränkungen für Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214952"
---
# <a name="ole-limitations-on-streams"></a><span data-ttu-id="d3409-103">OLE-Einschränkungen für Streams</span><span class="sxs-lookup"><span data-stu-id="d3409-103">OLE Limitations on Streams</span></span>

<span data-ttu-id="d3409-104">Entwickler von Installations Datenbanken müssen zwei Einschränkungen bei der Behandlung von Streams durch die strukturierte Win32 OLE-Speicher Implementierung beachten.</span><span class="sxs-lookup"><span data-stu-id="d3409-104">Developers of installation databases need to be aware of two limitations on the handling of streams by the Win32 OLE structured storage implementation.</span></span> <span data-ttu-id="d3409-105">Diese Einschränkungen können sich durch Transformationen und andere Daten, die in der Datenbank als Stream gespeichert werden können, indirekt auf die Installer-Funktionen auswirken.</span><span class="sxs-lookup"><span data-stu-id="d3409-105">These limitations can affect installer functions indirectly through transforms and other data that may be stored in the database as a stream.</span></span>

<span data-ttu-id="d3409-106">Es gibt zwei relevante Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="d3409-106">There are two relevant limitations:</span></span>

-   <span data-ttu-id="d3409-107">Binärdaten werden mit einem Indexnamen gespeichert, der erstellt wird, indem der Tabellenname und die Werte der Primärschlüssel des Datensatzes mithilfe eines Punkte Trennzeichens verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="d3409-107">Binary data is stored with an index name created by concatenating the table name and the values of the record's primary keys using a period delimiter.</span></span> <span data-ttu-id="d3409-108">OLE schränkt Streamnamen auf 32 Zeichen ein (31 + null-Terminator).</span><span class="sxs-lookup"><span data-stu-id="d3409-108">OLE limits stream names to 32 characters (31 + null terminator).</span></span> <span data-ttu-id="d3409-109">Windows Installer verwendet einen Komprimierungs Algorithmus, der das Limit je nach Zeichen auf 62 Zeichen erweitern kann.</span><span class="sxs-lookup"><span data-stu-id="d3409-109">Windows Installer uses a compression algorithm that can expand the limit to 62 characters depending upon the character.</span></span> <span data-ttu-id="d3409-110">Beachten Sie, dass Doppelbyte Zeichen als 2 gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="d3409-110">Note that double-byte characters count as 2.</span></span>
-   <span data-ttu-id="d3409-111">Obwohl mehrere Streams gleichzeitig geöffnet sein können, können Sie einen Stream nicht ein zweites Mal öffnen, bis der erste Verweis geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d3409-111">Although you can have multiple streams open at one time, you cannot open a stream a second time until the first reference is closed.</span></span> <span data-ttu-id="d3409-112">Dies bedeutet, dass Sie nicht denselben binären Datenstrom auswählen können, der gleichzeitig in mehreren Datensätzen geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3409-112">This means you cannot select the same binary data stream to be open in multiple records simultaneously.</span></span> <span data-ttu-id="d3409-113">Der Versuch, die Binärdaten aus dem zweiten Datensatz zu lesen, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="d3409-113">Attempts to read the binary data from the second record fail.</span></span> <span data-ttu-id="d3409-114">Außerdem können Sie die Primärschlüssel eines Datensatzes nicht umbenennen, während ein binärer Datenstrom in diesem Datensatz geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3409-114">Also you cannot rename the primary keys of a record while a binary data stream in that record is open.</span></span>

 

 



