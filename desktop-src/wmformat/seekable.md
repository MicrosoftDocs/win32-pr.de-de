---
title: Durchsuchbar
description: Das suchbare Attribut ist ein Attribut auf Dateiebene, das angibt, ob eine Anwendung auf Punkte innerhalb des Inhalts suchen kann.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Suchbares Windows Media-Format
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314500"
---
# <a name="seekable"></a><span data-ttu-id="c6c42-104">Durchsuchbar</span><span class="sxs-lookup"><span data-stu-id="c6c42-104">Seekable</span></span>

<span data-ttu-id="c6c42-105">Das suchbare Attribut ist **ein Attribut auf** Dateiebene, das angibt, ob eine Anwendung auf Punkte innerhalb des Inhalts suchen kann.</span><span class="sxs-lookup"><span data-stu-id="c6c42-105">The **Seekable** attribute is a file-level attribute specifying whether an application can seek to points within the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c6c42-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="c6c42-106">Global Constant</span></span>

<span data-ttu-id="c6c42-107">g \_ wszwmseekable</span><span class="sxs-lookup"><span data-stu-id="c6c42-107">g\_wszWMSeekable</span></span>

## <a name="data-type"></a><span data-ttu-id="c6c42-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c6c42-108">Data Type</span></span>

<span data-ttu-id="c6c42-109">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c6c42-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c42-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6c42-110">Remarks</span></span>

<span data-ttu-id="c6c42-111">Dies ist ein codiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="c6c42-111">This is a coded attribute.</span></span>

<span data-ttu-id="c6c42-112">Dieses Attribut kann nicht auf Dateiebene dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="c6c42-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="c6c42-113">Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.</span><span class="sxs-lookup"><span data-stu-id="c6c42-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="c6c42-114">Der Wert dieses Attributs für eine Datei kann variieren, je nachdem, welches Objekt die zum Abrufen verwendete [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -oder [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="c6c42-114">The value of this attribute for a file may vary depending upon the object exposing the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface used to retrieve it.</span></span> <span data-ttu-id="c6c42-115">Dies liegt daran, dass die Reader-Objekte (sowohl synchrone als auch asynchron) eine gründlichere Überprüfung durchführen als das Metadateneditor-Objekt, um zu ermitteln, ob Sie einen Punkt in einer Datei suchen können.</span><span class="sxs-lookup"><span data-stu-id="c6c42-115">This is because the reader objects (both synchronous and asynchronous) perform a more thorough check than the metadata editor object does, to ascertain whether you can seek to a point in a file.</span></span> <span data-ttu-id="c6c42-116">Der **von** einem Reader-Objekt zurückgegebene suchbare Attribut Wert ist präziser.</span><span class="sxs-lookup"><span data-stu-id="c6c42-116">The **Seekable** attribute value returned by a reader object is more accurate.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6c42-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6c42-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c42-118">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="c6c42-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




