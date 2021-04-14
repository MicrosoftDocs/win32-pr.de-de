---
description: BLOB-Komponenten
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: BLOB-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217174"
---
# <a name="blob-components"></a><span data-ttu-id="04e18-103">BLOB-Komponenten</span><span class="sxs-lookup"><span data-stu-id="04e18-103">BLOB Components</span></span>

<span data-ttu-id="04e18-104">Ein Binary Large Object (BLOB) umfasst die folgenden hierarchischen Komponenten:</span><span class="sxs-lookup"><span data-stu-id="04e18-104">A binary large object (BLOB) includes the following hierarchical components:</span></span>

-   <span data-ttu-id="04e18-105">Besitzer</span><span class="sxs-lookup"><span data-stu-id="04e18-105">Owners</span></span>
-   <span data-ttu-id="04e18-106">Kategorien</span><span class="sxs-lookup"><span data-stu-id="04e18-106">Categories</span></span>
-   <span data-ttu-id="04e18-107">`Tags`</span><span class="sxs-lookup"><span data-stu-id="04e18-107">Tags</span></span>
-   <span data-ttu-id="04e18-108">Werte</span><span class="sxs-lookup"><span data-stu-id="04e18-108">Values</span></span>

## <a name="textual-representation"></a><span data-ttu-id="04e18-109">Textdarstellung</span><span class="sxs-lookup"><span data-stu-id="04e18-109">Textual Representation</span></span>

<span data-ttu-id="04e18-110">Aus praktischer Gründen werden blobdateien im Format owner: Category: Tag: value angezeigt, das Sie beim Speichern in einer Datei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="04e18-110">For convenience, BLOBs appear in the Owner:Category:Tag:Value format that they appear in when saved to a file.</span></span> <span data-ttu-id="04e18-111">Die interne Struktur des BLOBs ist nicht transparent, da Sie Zeiger und Tabellen darstellt.</span><span class="sxs-lookup"><span data-stu-id="04e18-111">The internal structure of the BLOB is opaque because it represents pointers and tables.</span></span> <span data-ttu-id="04e18-112">Hier ist beispielsweise ein Eintrag aus einem BLOB, der zum Konfigurieren eines NPP verwendet werden kann:</span><span class="sxs-lookup"><span data-stu-id="04e18-112">For example, here is an entry from a BLOB that can be used to configure an NPP:</span></span>

``` syntax
NPP:Configure:BufferSize=32768
```

<span data-ttu-id="04e18-113">Der Besitzer ist NPP.</span><span class="sxs-lookup"><span data-stu-id="04e18-113">The Owner is NPP.</span></span> <span data-ttu-id="04e18-114">Die Kategorie ist configure, das Tag ist bufferSize und der Wert 32768.</span><span class="sxs-lookup"><span data-stu-id="04e18-114">The Category is Configure, the Tag is BufferSize, and the Value is 32768.</span></span>

 

 



