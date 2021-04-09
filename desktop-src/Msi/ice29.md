---
description: ICE29 überprüft, ob abgeschnittene Streamnamen eindeutig sind. Jede Tabelle, die eine Binär-oder Objekt Spalte aufweist, wird überprüft. Weitere Informationen finden Sie unter Datentyp der Binär Spalte.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f606bd09314d045b643816c08349eba38bde72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959392"
---
# <a name="ice29"></a><span data-ttu-id="3e5e3-105">ICE29</span><span class="sxs-lookup"><span data-stu-id="3e5e3-105">ICE29</span></span>

<span data-ttu-id="3e5e3-106">ICE29 überprüft, ob abgeschnittene Streamnamen eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="3e5e3-106">ICE29 validates that truncated stream names remain unique.</span></span> <span data-ttu-id="3e5e3-107">Jede Tabelle, die eine Binär-oder Objekt Spalte aufweist, wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="3e5e3-107">Any table having a Binary or Object column is validated.</span></span> <span data-ttu-id="3e5e3-108">Weitere Informationen finden Sie unter Datentyp der [Binär](binary.md) Spalte.</span><span class="sxs-lookup"><span data-stu-id="3e5e3-108">See the [Binary](binary.md) column data type.</span></span>

<span data-ttu-id="3e5e3-109">Durch die Verarbeitung von Streams durch die Win32 OLE-strukturierte Speicher Implementierung werden Streamnamen eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="3e5e3-109">Handling of streams by the Win32 OLE structured storage implementation limits stream names.</span></span> <span data-ttu-id="3e5e3-110">Siehe [OLE-Einschränkungen für Datenströme](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="3e5e3-110">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="3e5e3-111">Der Installer kann Streamnamen mit bis zu 62 Zeichen komprimieren.</span><span class="sxs-lookup"><span data-stu-id="3e5e3-111">The installer can compress stream names up to 62 characters in length.</span></span> <span data-ttu-id="3e5e3-112">Namen, die länger sind als diese, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="3e5e3-112">Names longer than this are truncated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e5e3-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e5e3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e5e3-114">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="3e5e3-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



