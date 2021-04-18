---
title: Is_Protected
description: Das is \_ protected-Attribut ist ein Attribut auf Dateiebene, das angibt, ob der Inhalt in der Datei durch Digital Rights Management (DRM) geschützt wurde.
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected Windows Media-Format
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338436"
---
# <a name="is_protected"></a><span data-ttu-id="3f29e-104">Ist \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="3f29e-104">Is\_Protected</span></span>

<span data-ttu-id="3f29e-105">Das **is \_ Protected** -Attribut ist ein Attribut auf Dateiebene, das angibt, ob der Inhalt in der Datei durch Digital Rights Management (DRM) geschützt wurde.</span><span class="sxs-lookup"><span data-stu-id="3f29e-105">The **Is\_Protected** attribute is a file-level attribute specifying whether the content in the file was protected using digital rights management (DRM).</span></span>

## <a name="global-constant"></a><span data-ttu-id="3f29e-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="3f29e-106">Global Constant</span></span>

<span data-ttu-id="3f29e-107">g \_ wszwmprotected</span><span class="sxs-lookup"><span data-stu-id="3f29e-107">g\_wszWMProtected</span></span>

## <a name="data-type"></a><span data-ttu-id="3f29e-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3f29e-108">Data Type</span></span>

<span data-ttu-id="3f29e-109">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="3f29e-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="3f29e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f29e-110">Remarks</span></span>

<span data-ttu-id="3f29e-111">Dies ist ein codiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="3f29e-111">This is a coded attribute.</span></span> <span data-ttu-id="3f29e-112">Wenn Sie diese Eigenschaft abrufen, werden dieselben Informationen wie beim Aufrufen von [**wmiscontentprotected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3f29e-112">Retrieving this property provides the same information as calling [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span></span>

<span data-ttu-id="3f29e-113">Dieses Attribut kann nicht auf Dateiebene dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="3f29e-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="3f29e-114">Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.</span><span class="sxs-lookup"><span data-stu-id="3f29e-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f29e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f29e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f29e-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="3f29e-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




