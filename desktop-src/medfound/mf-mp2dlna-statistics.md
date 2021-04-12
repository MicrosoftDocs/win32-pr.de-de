---
description: Ruft Statistiken aus der Datenträger-Senke der digitalen Lebens Netzwerk-Allianz (DLNA) ab.
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: MF_MP2DLNA_STATISTICS-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528256"
---
# <a name="mf_mp2dlna_statistics-attribute"></a><span data-ttu-id="d4d72-103">MF \_ MP2DLNA \_ Statistics-Attribut</span><span class="sxs-lookup"><span data-stu-id="d4d72-103">MF\_MP2DLNA\_STATISTICS attribute</span></span>

<span data-ttu-id="d4d72-104">Ruft Statistiken aus der Datenträger-Senke der digitalen Lebens Netzwerk-Allianz (DLNA) ab.</span><span class="sxs-lookup"><span data-stu-id="d4d72-104">Gets statistics from the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4d72-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d4d72-105">Data type</span></span>

<span data-ttu-id="d4d72-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** als **Byte \[ \]** gespeichert</span><span class="sxs-lookup"><span data-stu-id="d4d72-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="d4d72-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="d4d72-107">Get/set</span></span>

<span data-ttu-id="d4d72-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d4d72-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d72-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4d72-109">Remarks</span></span>

<span data-ttu-id="d4d72-110">Während des Streamings aktualisiert die DLNA-Medien Senke dieses Attribut mit Statistiken über die Codierung und das Multiplexing der MPEG-2-Streams.</span><span class="sxs-lookup"><span data-stu-id="d4d72-110">During streaming, the DLNA media sink updates this attribute with statistics about the encoding and multiplexing of the MPEG-2 streams.</span></span> <span data-ttu-id="d4d72-111">Die Anwendung kann dieses Attribut jederzeit Abfragen, um die aktuellen Werte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4d72-111">The application can query this attribute at any time to get the latest values.</span></span>

<span data-ttu-id="d4d72-112">Das Festlegen dieses Attributs für die DLNA-Medien Senke hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="d4d72-112">Setting this attribute on the DLNA media sink has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d72-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4d72-113">Requirements</span></span>



| <span data-ttu-id="d4d72-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4d72-114">Requirement</span></span> | <span data-ttu-id="d4d72-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d4d72-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d72-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4d72-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d72-117">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d72-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d4d72-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4d72-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d72-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d72-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d4d72-120">Header</span><span class="sxs-lookup"><span data-stu-id="d4d72-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d72-121"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d72-121"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d72-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4d72-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d72-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d4d72-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




