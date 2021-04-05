---
title: Handlerarchitektur
description: Handlerarchitektur
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037064"
---
# <a name="handler-architecture"></a><span data-ttu-id="abbd7-103">Handlerarchitektur</span><span class="sxs-lookup"><span data-stu-id="abbd7-103">Handler Architecture</span></span>

<span data-ttu-id="abbd7-104">Die interne Funktion eines Datei-oder streamhandlers wird vom Handler selbst definiert.</span><span class="sxs-lookup"><span data-stu-id="abbd7-104">The internal function of a file or stream handler is defined by the handler itself.</span></span> <span data-ttu-id="abbd7-105">Für eine Anwendung wird in der Regel ein Datei Handler als Modul zum Lesen und Schreiben von AVI-Dateien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="abbd7-105">To an application, a file handler typically appears as a module to read and write AVI files.</span></span> <span data-ttu-id="abbd7-106">Entsprechend wird ein Datenstrom Handler als Modul angezeigt, um einen bestimmten Typ von Datenstrom zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="abbd7-106">Similarly, a stream handler appears as a module to read and write a specific type of data stream.</span></span> <span data-ttu-id="abbd7-107">Die konsistente Stream-Schnittstelle macht die Quelle und das Ziel des Streams unwichtig für die Anwendung, die den Handler verwendet.</span><span class="sxs-lookup"><span data-stu-id="abbd7-107">The consistent stream interface makes the source and destination of the stream unimportant to the application that uses the handler.</span></span>

<span data-ttu-id="abbd7-108">Ein Datei Handler ermöglicht den Zugriff auf eine Datenquelle, die aus einem oder mehreren Datenströmen besteht.</span><span class="sxs-lookup"><span data-stu-id="abbd7-108">A file handler provides access to a data source consisting of one or more data streams.</span></span> <span data-ttu-id="abbd7-109">Datei Handler ermöglichen in der Regel den Zugriff auf Datenträger Dateien, die einen oder mehrere Datenströme enthalten, und die internen Funktionen des Datei Handler lesen und schreiben die Multimedia-Daten.</span><span class="sxs-lookup"><span data-stu-id="abbd7-109">File handlers typically provide access to disk files containing one or more data streams, and the internal functions of the file handler read and write the multimedia data.</span></span> <span data-ttu-id="abbd7-110">Datei Handler können jedoch mit jeder beliebigen Datenquelle arbeiten, z. b. einem digitalen Übertragungskanal, der mehrere gemischte Datenströme enthält.</span><span class="sxs-lookup"><span data-stu-id="abbd7-110">However, file handlers can work with any data source, such as a digital transmission channel containing several intermingled data streams.</span></span>

<span data-ttu-id="abbd7-111">Im Gegensatz dazu verarbeitet ein Datenstrom Handler einen Datentyp und wird als Datenstrom zu einer Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="abbd7-111">In contrast, a stream handler processes one type of data and appears as a data stream to an application.</span></span> <span data-ttu-id="abbd7-112">Ein Datenstrom Handler kann Daten bereitstellen, die er herstellt, oder er kann Daten aus einer Datei oder einer externen Quelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="abbd7-112">A stream handler can provide data that it manufactures, or it can retrieve data from a file or an external source.</span></span> <span data-ttu-id="abbd7-113">Die Daten werden in einem Format bereitstellt, das von der Anwendung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="abbd7-113">It supplies its data in a format that your application can use.</span></span>

 

 




