---
description: Der Positionstyp eines Inhaltsverzeichnisses.
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Der Positionstyp eines Inhaltsverzeichnisses.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348904"
---
# <a name="the-position-type-of-a-table-of-contents"></a><span data-ttu-id="26912-103">Der Positionstyp eines Inhaltsverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="26912-103">The Position Type of a Table of Contents</span></span>

<span data-ttu-id="26912-104">Einige Methoden der [**idecparser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) -Schnittstelle verfügen über einen Parameter mit dem Namen *enumerationstype* , der den Typ des [**\_ \_ Enumerationstyps**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type)Enumerationstyp hat.</span><span class="sxs-lookup"><span data-stu-id="26912-104">Some methods of the [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface have a parameter named *enumTocPosType* that has a type of [**enum TOC\_POS\_TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span></span> <span data-ttu-id="26912-105">Dieser Parameter gibt die Position in einer Mediendatei an, in der ein Inhaltsverzeichnis gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="26912-105">This parameter specifies the position in a media file where a table of contents is stored.</span></span> <span data-ttu-id="26912-106">Die Absicht war, dass das Inhaltsverzeichnis entweder im Dateiheader oder im Text der Datei als Objekt der obersten Ebene gespeichert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="26912-106">The intent was that the table of contents could be stored either in the file header or in the body of the file as a top level object.</span></span> <span data-ttu-id="26912-107">Diese Funktionalität wurde noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="26912-107">This functionality has not, as yet, been implemented.</span></span>

<span data-ttu-id="26912-108">Tabellen mit Inhalten können derzeit nur als Objekte der obersten Ebene gespeichert werden. Daher müssen Sie den Enumerations Parameter " *enumcpostype* " immer auf " **TC \_ POS \_ toplevelobject**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="26912-108">Currently, tables of contents can only be stored as top level objects, so you must always set the *enumTocPosType* parameter to **TOC\_POS\_TOPLEVELOBJECT**.</span></span> <span data-ttu-id="26912-109">Wenn Sie " *enumercpostype* " auf " **Dec \_ POS \_ inheader**" festlegen, gibt die Methode " **E \_ notimpl**" zurück.</span><span class="sxs-lookup"><span data-stu-id="26912-109">If you set *enumTocPosType* to **TOC\_POS\_INHEADER**, the method will return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="26912-110">Die folgenden Methoden verfügen über einen *enumycpostype* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="26912-110">The following methods have an *enumTocPosType* parameter.</span></span>

-   [<span data-ttu-id="26912-111">**Getdeccount**</span><span class="sxs-lookup"><span data-stu-id="26912-111">**GetTocCount**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [<span data-ttu-id="26912-112">**Getdecbyindex**</span><span class="sxs-lookup"><span data-stu-id="26912-112">**GetTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [<span data-ttu-id="26912-113">**Getdecbytype**</span><span class="sxs-lookup"><span data-stu-id="26912-113">**GetTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [<span data-ttu-id="26912-114">**Addinhalts Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="26912-114">**AddToc**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [<span data-ttu-id="26912-115">**Removedecbyindex**</span><span class="sxs-lookup"><span data-stu-id="26912-115">**RemoveTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [<span data-ttu-id="26912-116">**Removedecbytype**</span><span class="sxs-lookup"><span data-stu-id="26912-116">**RemoveTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a><span data-ttu-id="26912-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26912-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26912-118">Programmier Handbuch für das Inhaltsverzeichnis des Parsers</span><span class="sxs-lookup"><span data-stu-id="26912-118">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



