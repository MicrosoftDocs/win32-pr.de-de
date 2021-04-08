---
description: Enthält einen Zeiger auf einen Eigenschaften Speicher mit Codierungs Eigenschaften.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: MF_SINK_WRITER_ENCODER_CONFIG-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757399"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a><span data-ttu-id="c974a-103">Konfigurations Attribut für den MF- \_ \_ senderwriter \_ \_</span><span class="sxs-lookup"><span data-stu-id="c974a-103">MF\_SINK\_WRITER\_ENCODER\_CONFIG attribute</span></span>

<span data-ttu-id="c974a-104">Enthält einen Zeiger auf einen Eigenschaften Speicher mit Codierungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c974a-104">Contains a pointer to a property store with encoding properties.</span></span>

## <a name="data-type"></a><span data-ttu-id="c974a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c974a-105">Data type</span></span>

<span data-ttu-id="c974a-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="c974a-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="c974a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c974a-107">Remarks</span></span>

<span data-ttu-id="c974a-108">Der Wert dieses Attributs ist ein [_ *IPropertyStore* \*](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c974a-108">The value of this attribute is an [_ *IPropertyStore*\*](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer.</span></span>

<span data-ttu-id="c974a-109">Dieses Attribut ermöglicht es einer Anwendung, Codierungs Eigenschaften festzulegen, wenn der [Senke-Writer](sink-writer.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c974a-109">This attribute enables an application to set encoding properties when using the [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="c974a-110">Führen Sie die folgenden Schritte aus, um dieses Attribut festzulegen:</span><span class="sxs-lookup"><span data-stu-id="c974a-110">To set this attribute, perform the following steps:</span></span>

1.  <span data-ttu-id="c974a-111">Rufen Sie [**pscreatememorypropertystore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) auf, um einen neuen Eigenschaften Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c974a-111">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a new property store.</span></span>
2.  <span data-ttu-id="c974a-112">Legen Sie die Codierungs Eigenschaften für den Eigenschaften Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="c974a-112">Set encoder properties on the property store.</span></span> <span data-ttu-id="c974a-113">Die verfügbaren Eigenschaften hängen vom Encoder ab.</span><span class="sxs-lookup"><span data-stu-id="c974a-113">The available properties depends on the encoder.</span></span> <span data-ttu-id="c974a-114">Weitere Informationen finden Sie unter [Codec-Objekte](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="c974a-114">For more information, see [Codec Objects](codecobjects.md).</span></span>
3.  <span data-ttu-id="c974a-115">Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c974a-115">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
4.  <span data-ttu-id="c974a-116">Aufrufen von [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) , um den [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger auf den Attribut Speicher festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c974a-116">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer on the attribute store.</span></span>
5.  <span data-ttu-id="c974a-117">Erstellen Sie eine neue Instanz des Senke Writers.</span><span class="sxs-lookup"><span data-stu-id="c974a-117">Create a new instance of the Sink Writer.</span></span> <span data-ttu-id="c974a-118">Übergeben Sie den [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger an die Erstellungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="c974a-118">Pass the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer to the creation function.</span></span> <span data-ttu-id="c974a-119">Weitere Informationen finden Sie unter [senkenwriter-Attribute](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="c974a-119">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

<span data-ttu-id="c974a-120">Der senkwriter legt die Eigenschaften für den Encoder vor dem Festlegen der Medientypen fest.</span><span class="sxs-lookup"><span data-stu-id="c974a-120">The Sink Writer sets the properties on the encoder before setting the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="c974a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c974a-121">Requirements</span></span>



| <span data-ttu-id="c974a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c974a-122">Requirement</span></span> | <span data-ttu-id="c974a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c974a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c974a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c974a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c974a-125">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c974a-125">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c974a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c974a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c974a-127">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c974a-127">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c974a-128">Header</span><span class="sxs-lookup"><span data-stu-id="c974a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c974a-129"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c974a-129"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c974a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c974a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c974a-131">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c974a-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c974a-132">**Imbersink Writer**</span><span class="sxs-lookup"><span data-stu-id="c974a-132">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="c974a-133">Senkenwriter-Attribute</span><span class="sxs-lookup"><span data-stu-id="c974a-133">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 
