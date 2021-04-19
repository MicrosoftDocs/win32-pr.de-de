---
description: Byte Datenstrom Attribute
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Byte Datenstrom Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346053"
---
# <a name="byte-stream-attributes"></a><span data-ttu-id="d2711-103">Byte Datenstrom Attribute</span><span class="sxs-lookup"><span data-stu-id="d2711-103">Byte Stream Attributes</span></span>

<span data-ttu-id="d2711-104">Die folgenden Attribute gelten für einige Byte Datenströme.</span><span class="sxs-lookup"><span data-stu-id="d2711-104">The following attributes apply to some byte streams.</span></span> <span data-ttu-id="d2711-105">Um herauszufinden, ob ein Bytestream Attribute unterstützt, Fragen Sie das bytestreamobjekt nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="d2711-105">To find out whether a byte stream supports attributes, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>



| <span data-ttu-id="d2711-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="d2711-106">Attribute</span></span>                                                                                  | <span data-ttu-id="d2711-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2711-107">Description</span></span>                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="d2711-108">**MF- \_ Bytestream- \_ \_ Inhaltstyp**</span><span class="sxs-lookup"><span data-stu-id="d2711-108">**MF\_BYTESTREAM\_CONTENT\_TYPE**</span></span>](mf-bytestream-content-type-attribute.md)              | <span data-ttu-id="d2711-109">Gibt den MIME-Typ eines Bytestreams an.</span><span class="sxs-lookup"><span data-stu-id="d2711-109">Specifies the MIME type of a byte stream.</span></span>                         |
| [<span data-ttu-id="d2711-110">**MF- \_ \_ bytestreamdauer**</span><span class="sxs-lookup"><span data-stu-id="d2711-110">**MF\_BYTESTREAM\_DURATION**</span></span>](mf-bytestream-duration-attribute.md)                       | <span data-ttu-id="d2711-111">Gibt die Dauer eines Bytestreams in 100-Nanosecond-Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="d2711-111">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="d2711-112">MF- \_ Bytestream- \_ IFO-Datei- \_ \_ URI</span><span class="sxs-lookup"><span data-stu-id="d2711-112">MF\_BYTESTREAM\_IFO\_FILE\_URI</span></span>](mf-bytestream-ifo-file-uri.md)                           | <span data-ttu-id="d2711-113">Gibt die URL einer zugeordneten IFO-Datei an.</span><span class="sxs-lookup"><span data-stu-id="d2711-113">Specifies the URL of an associated IFO file.</span></span>                      |
| [<span data-ttu-id="d2711-114">**\_Zeitpunkt der \_ letzten Änderung des \_ MF-Bytestreams \_**</span><span class="sxs-lookup"><span data-stu-id="d2711-114">**MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME**</span></span>](mf-bytestream-last-modified-time-attribute.md) | <span data-ttu-id="d2711-115">Gibt an, wann ein Bytestream zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d2711-115">Specifies when a byte stream was last modified.</span></span>                   |
| [<span data-ttu-id="d2711-116">**Name des MF- \_ Bytestream- \_ Ursprungs \_**</span><span class="sxs-lookup"><span data-stu-id="d2711-116">**MF\_BYTESTREAM\_ORIGIN\_NAME**</span></span>](mf-bytestream-origin-name-attribute.md)                | <span data-ttu-id="d2711-117">Gibt die ursprüngliche URL für einen Byte Datenstrom an.</span><span class="sxs-lookup"><span data-stu-id="d2711-117">Specifies the original URL for a byte stream.</span></span>                     |



 

<span data-ttu-id="d2711-118">Die folgenden Attribute gelten für Byte Datenstrom Handler.</span><span class="sxs-lookup"><span data-stu-id="d2711-118">The following attributes apply to byte-stream handlers.</span></span>



| <span data-ttu-id="d2711-119">Attribut</span><span class="sxs-lookup"><span data-stu-id="d2711-119">Attribute</span></span>                                                                                    | <span data-ttu-id="d2711-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2711-120">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2711-121">MF \_ bytestreamhandler \_ akzeptiert \_ Freigabe \_ Schreibvorgänge</span><span class="sxs-lookup"><span data-stu-id="d2711-121">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE</span></span>](mf-bytestreamhandler-accepts-share-write.md) | <span data-ttu-id="d2711-122">Gibt an, ob ein Byte Strom Handler einen Bytestream verwenden kann, der zum Schreiben durch einen anderen Thread geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="d2711-122">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d2711-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2711-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2711-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="d2711-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[<span data-ttu-id="d2711-125">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d2711-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



