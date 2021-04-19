---
description: Gibt an, ob ein Byte Strom Handler einen Bytestream verwenden kann, der zum Schreiben durch einen anderen Thread geöffnet ist.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356864"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a><span data-ttu-id="26ba5-103">MF \_ bytestreamhandler \_ akzeptiert \_ Freigabe- \_ Schreib Attribute</span><span class="sxs-lookup"><span data-stu-id="26ba5-103">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute</span></span>

<span data-ttu-id="26ba5-104">Gibt an, ob ein Byte Strom Handler einen Bytestream verwenden kann, der zum Schreiben durch einen anderen Thread geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="26ba5-104">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread.</span></span>

## <a name="data-type"></a><span data-ttu-id="26ba5-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="26ba5-105">Data type</span></span>

<span data-ttu-id="26ba5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="26ba5-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="26ba5-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="26ba5-107">Get/set</span></span>

<span data-ttu-id="26ba5-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="26ba5-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="26ba5-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="26ba5-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="26ba5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26ba5-110">Remarks</span></span>

<span data-ttu-id="26ba5-111">Bytestreamhandler können dieses Attribut unterstützen.</span><span class="sxs-lookup"><span data-stu-id="26ba5-111">Byte-stream handlers can support this attribute.</span></span> <span data-ttu-id="26ba5-112">Um das Attribut zu erhalten oder festzulegen, Fragen Sie zuerst den bytestreamhandler für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="26ba5-112">To get or set the attribute, first query the byte-stream handler for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="26ba5-113">Anschließend wird [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) oder [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="26ba5-113">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) or [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span></span>

<span data-ttu-id="26ba5-114">Wenn dieses Attribut **true** ist, bedeutet dies, dass der Byte Datenstrom Handler aus einem Stream lesen kann, während ein anderer Thread in denselben Stream schreibt.</span><span class="sxs-lookup"><span data-stu-id="26ba5-114">If this attribute is **TRUE**, it means that the byte-stream handler can read from a stream while another thread writes to the same stream.</span></span> <span data-ttu-id="26ba5-115">Wenn ein Stream zum Schreiben durch einen anderen Thread geöffnet wird, gibt die [**imfbytestream:: getfunktionalitäten**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) -Methode das **mfbytestream-freigabeflag für die \_ Freigabe \_** zurück.</span><span class="sxs-lookup"><span data-stu-id="26ba5-115">When a stream is opened for writing by another thread, the [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) method returns the **MFBYTESTREAM\_SHARE\_WRITE** flag.</span></span>

<span data-ttu-id="26ba5-116">Dieses Attribut wirkt sich auf die Quell Auflösung aus.</span><span class="sxs-lookup"><span data-stu-id="26ba5-116">This attribute affects source resolution.</span></span> <span data-ttu-id="26ba5-117">Wenn für einen Bytestream das **\_ \_ kennschreibflag für die mfbytestream-Freigabe** festgelegt ist, übergibt der [quellresolver](source-resolver.md) diesen Stream nicht an einen Byte Datenstrom-Handler, es sei denn, der Handler hat den MF \_ bytestreamhandler \_ akzeptiert das \_ \_ Attribut für Freigabe Schreibzugriff auf **true**</span><span class="sxs-lookup"><span data-stu-id="26ba5-117">If a byte stream has the **MFBYTESTREAM\_SHARE\_WRITE** flag set, the [Source Resolver](source-resolver.md) will not pass that stream to a byte-stream handler unless the handler has the MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute set to **TRUE**.</span></span>

<span data-ttu-id="26ba5-118">Das **MF Bytestream- \_ Freigabe \_ Schreib** Flag ist ein Hinweis darauf, dass sich die Länge des Streams ändern kann, während der Handler aus ihm liest.</span><span class="sxs-lookup"><span data-stu-id="26ba5-118">The **MFBYTESTREAM\_SHARE\_WRITE** flag is a hint that the length of the stream might change while the handler is reading from it.</span></span>

<span data-ttu-id="26ba5-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="26ba5-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="26ba5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26ba5-120">Requirements</span></span>



| <span data-ttu-id="26ba5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26ba5-121">Requirement</span></span> | <span data-ttu-id="26ba5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="26ba5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26ba5-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26ba5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="26ba5-124">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="26ba5-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="26ba5-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26ba5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="26ba5-126">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="26ba5-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="26ba5-127">Header</span><span class="sxs-lookup"><span data-stu-id="26ba5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="26ba5-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ba5-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ba5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26ba5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ba5-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="26ba5-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26ba5-131">Schema Handler und Byte-Stream Handler</span><span class="sxs-lookup"><span data-stu-id="26ba5-131">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




