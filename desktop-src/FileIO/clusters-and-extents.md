---
description: 'Auf Cluster kann aus zwei unterschiedlichen Perspektiven verwiesen werden: innerhalb der Datei und auf dem Volume.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Cluster und Blöcke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358933"
---
# <a name="clusters-and-extents"></a><span data-ttu-id="da7fe-103">Cluster und Blöcke</span><span class="sxs-lookup"><span data-stu-id="da7fe-103">Clusters and Extents</span></span>

<span data-ttu-id="da7fe-104">Auf Cluster kann aus zwei unterschiedlichen Perspektiven verwiesen werden: innerhalb der Datei und auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="da7fe-104">Clusters may be referred to from two different perspectives: within the file and on the volume.</span></span> <span data-ttu-id="da7fe-105">Jeder Cluster in einer Datei verfügt über eine *Virtuelle Cluster Nummer* (VCN), bei der es sich um den relativen Offset vom Anfang der Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="da7fe-105">Any cluster in a file has a *virtual cluster number* (VCN), which is its relative offset from the beginning of the file.</span></span> <span data-ttu-id="da7fe-106">Beispielsweise gibt eine Suche nach einer doppelten Größe eines Clusters, gefolgt von einem Lesevorgang, Daten ab der dritten VCN zurück.</span><span class="sxs-lookup"><span data-stu-id="da7fe-106">For example, a seek to twice the size of a cluster, followed by a read, will return data beginning at the third VCN.</span></span> <span data-ttu-id="da7fe-107">In einer *logischen Cluster Nummer* (LCN) wird der Offset eines Clusters von einem beliebigen Punkt innerhalb des Volumes beschrieben.</span><span class="sxs-lookup"><span data-stu-id="da7fe-107">A *logical cluster number* (LCN) describes the offset of a cluster from some arbitrary point within the volume.</span></span> <span data-ttu-id="da7fe-108">Lcns sollte nur als Ordinalzahl oder relative Zahlen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="da7fe-108">LCNs should be treated only as ordinal, or relative, numbers.</span></span> <span data-ttu-id="da7fe-109">Es gibt keine garantierte Zuordnung logischer Cluster zu physischen Festplatten Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="da7fe-109">There is no guaranteed mapping of logical clusters to physical hard disk drive sectors.</span></span>

<span data-ttu-id="da7fe-110">Ein *Block ist eine* Zusammenführung zusammenhängender Cluster.</span><span class="sxs-lookup"><span data-stu-id="da7fe-110">An *extent* is a run of contiguous clusters.</span></span> <span data-ttu-id="da7fe-111">Nehmen wir beispielsweise an, eine Datei, die aus 30 Clustern besteht, wird in zwei Blöcken aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="da7fe-111">For example, suppose a file consisting of 30 clusters is recorded in two extents.</span></span> <span data-ttu-id="da7fe-112">Der erste Block besteht möglicherweise aus fünf zusammenhängenden Clustern, den anderen verbleibenden 25 Clustern.</span><span class="sxs-lookup"><span data-stu-id="da7fe-112">The first extent might consist of five contiguous clusters, the other of the remaining 25 clusters.</span></span>

<span data-ttu-id="da7fe-113">Es gibt keine Garantie für eine Beziehung auf dem Datenträger in einem beliebigen Bereich in einem anderen Block.</span><span class="sxs-lookup"><span data-stu-id="da7fe-113">There is no guarantee of any relationship on the disk of any extent to any other extent.</span></span> <span data-ttu-id="da7fe-114">Der erste Block kann beispielsweise eine höhere LCN als nachfolgende Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="da7fe-114">For example, the first extent may be at a higher LCN than a subsequent extent.</span></span>

 

 



