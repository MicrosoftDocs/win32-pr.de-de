---
description: Gibt an, ob die Anwendung die Microsoft Direct3D-Unterstützung im Quell-oder senkenwriter erfordert.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: MF_READWRITE_D3D_OPTIONAL-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218239"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a><span data-ttu-id="6a2ad-103">MF, \_ Lese schreiben \_ D3D \_ optionales Attribut</span><span class="sxs-lookup"><span data-stu-id="6a2ad-103">MF\_READWRITE\_D3D\_OPTIONAL attribute</span></span>

<span data-ttu-id="6a2ad-104">Gibt an, ob die Anwendung die Microsoft Direct3D-Unterstützung im [Quell](source-reader.md) -oder [senkenwriter](sink-writer.md)erfordert.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-104">Specifies whether the application requires Microsoft Direct3D support in the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="6a2ad-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6a2ad-105">Data type</span></span>

<span data-ttu-id="6a2ad-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a2ad-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6a2ad-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a2ad-107">Remarks</span></span>

<span data-ttu-id="6a2ad-108">Dieses Attribut gilt nur, wenn die Anwendung die Direct3D-Unterstützung mithilfe des [MF- \_ Quell \_ Readers \_ D3D \_ Manager](mf-source-reader-d3d-manager.md) -oder [MF \_ Sink \_ Writer \_ D3D \_ Manager](mf-sink-writer-d3d-manager.md) -Attributs ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-108">This attribute applies only if the application enables Direct3D support using the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) or [MF\_SINK\_WRITER\_D3D\_MANAGER](mf-sink-writer-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="6a2ad-109">Wenn die Anwendung die Direct3D-Unterstützung aktiviert, versuchen sowohl der Quell-als auch der senkwriter, Direct3D-Oberflächen für Videos zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-109">If the application enables Direct3D support, the Source Reader and Sink Writer will both try to allocate Direct3D surfaces for video.</span></span> <span data-ttu-id="6a2ad-110">Wenn dies nicht der Fall ist und das Attribut "read Read D3D optional" den Wert " \_ \_ \_ **true**" hat, wird der quelllese-/senkwriter auf die Zuordnung von Video Oberflächen im Systemspeicher zurückgegriffen.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-110">If this fails, and the MF\_READWRITE\_D3D\_OPTIONAL attribute is **TRUE**, the Source Reader/Sink Writer will fall back to allocating video surfaces in system memory.</span></span> <span data-ttu-id="6a2ad-111">Andernfalls tritt bei der Verarbeitung ein Fehler auf, wenn Direct3D-Oberflächen nicht zugeordnet werden können und der MF- \_ Lesevorgang \_ D3D \_ optional **false** ist.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-111">Otherwise, if Direct3D surfaces cannot be allocated and MF\_READWRITE\_D3D\_OPTIONAL is **FALSE**, an error occurs during processing.</span></span>

<span data-ttu-id="6a2ad-112">Wenn die Anwendung die Direct3D-Unterstützung nicht aktiviert, verwendet der Quell-/senuswriter System Arbeitsspeicher und ignoriert den Wert von MF- \_ lesenschreib \_ D3D \_ optional.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-112">If the application does not enable Direct3D support, the Source Reader/Sink Writer uses system memory, and ignores the value of MF\_READWRITE\_D3D\_OPTIONAL.</span></span>

<span data-ttu-id="6a2ad-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-113">This attribute is optional.</span></span> <span data-ttu-id="6a2ad-114">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-114">The default value is **FALSE**.</span></span> <span data-ttu-id="6a2ad-115">Legen Sie das-Attribut fest, wenn Sie den Quell-oder Senke-Writer erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a2ad-115">Set the attribute when you create the Source Reader or Sink Writer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a2ad-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a2ad-116">Requirements</span></span>



| <span data-ttu-id="6a2ad-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a2ad-117">Requirement</span></span> | <span data-ttu-id="6a2ad-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6a2ad-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a2ad-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a2ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a2ad-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a2ad-120">Windows 8 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6a2ad-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a2ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a2ad-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a2ad-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a2ad-123">Header</span><span class="sxs-lookup"><span data-stu-id="6a2ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a2ad-124"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6a2ad-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a2ad-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a2ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a2ad-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6a2ad-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a2ad-127">Senkenwriter-Attribute</span><span class="sxs-lookup"><span data-stu-id="6a2ad-127">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a2ad-128">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="6a2ad-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




