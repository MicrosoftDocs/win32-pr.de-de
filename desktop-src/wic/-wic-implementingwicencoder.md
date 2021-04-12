---
description: Implementieren eines WIC-Enabled Encoders
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementieren eines WIC-Enabled Encoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216968"
---
# <a name="implementing-a-wic-enabled-encoder"></a><span data-ttu-id="b3ef8-103">Implementieren eines WIC-Enabled Encoders</span><span class="sxs-lookup"><span data-stu-id="b3ef8-103">Implementing a WIC-Enabled Encoder</span></span>

## <a name="introduction"></a><span data-ttu-id="b3ef8-104">Einführung</span><span class="sxs-lookup"><span data-stu-id="b3ef8-104">Introduction</span></span>

<span data-ttu-id="b3ef8-105">Zum Implementieren eines WIC-Encoders (Windows Imaging Component) müssen zwei Klassen geschrieben werden, ebenso wie bei der Implementierung eines WIC-Decoders.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-105">Implementing a Windows Imaging Component (WIC) encoder requires writing two classes, as is also true for implementing a WIC decoder.</span></span> <span data-ttu-id="b3ef8-106">Die Schnittstellen dieser Klassen entsprechen direkt den [Codierungs](-wic-howwicworks.md) Aufgaben, die im Abschnitt Codierung der Funktionsweise der Windows-Abbild Erstellungs Komponente beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-106">The interfaces on these classes correspond directly to the encoder responsibilities outlined in the [Encoding](-wic-howwicworks.md) section of How The Windows Imaging Component Works.</span></span>

<span data-ttu-id="b3ef8-107">Eine der-Klassen stellt Dienste auf Container Ebene bereit und verwaltet die Serialisierung der einzelnen Bildframes innerhalb des Containers.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-107">One of the classes provides container-level services and manages the serialization of the individual image frames within the container.</span></span> <span data-ttu-id="b3ef8-108">Diese Klasse implementiert die [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-108">This class implements the [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) interface.</span></span> <span data-ttu-id="b3ef8-109">Wenn Ihr Bildformat Metadaten auf Container Ebene unterstützt, müssen Sie auch die [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) -Schnittstelle für diese Klasse implementieren.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-109">If your image format supports container-level metadata, you must also implement the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface on this class.</span></span>

<span data-ttu-id="b3ef8-110">Die andere Klasse stellt Dienste auf Frame-Ebene bereit und übernimmt die eigentliche Codierung der Bildbits für jeden Frame im Container.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-110">The other class provides frame-level services and does the actual encoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="b3ef8-111">Außerdem durchläuft Sie die Metadatenblöcke für jeden Frame und fordert die entsprechenden metadatenwriter zum Serialisieren der Blöcke an.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-111">It also iterates through the metadata blocks for each frame and requests the appropriate metadata writers to serialize the blocks.</span></span> <span data-ttu-id="b3ef8-112">Diese Klasse implementiert die **iwicbitmapframekocode** -Schnittstelle und die [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-112">This class implements the **IWICBitmapFrameEncode** interface and the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface.</span></span> <span data-ttu-id="b3ef8-113">Diese Klasse sollte über einen IStream-Member verfügen, den die Klasse auf Container Ebene bei der Instanziierung initialisiert, in der die **Commit** -Methode die Frame Daten serialisiert.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-113">This class should have an IStream member that the container-level class initializes on instantiation, into which the **Commit** method will serialize the frame data.</span></span>

<span data-ttu-id="b3ef8-114">In einigen Fällen, z. b. in unformatierten Formaten, möchte der Codec-Autor möglicherweise nicht, dass Anwendungen in das RAW-Format codieren oder erneut codieren können, da der Zweck einer Rohdatendatei darin besteht, die Sensordaten genau so wie von der Kamera zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-114">In some cases, such as raw formats, the codec author may not want applications to be able to encode or re-encode to the raw format, because the purpose of a raw file is to contain the sensor data exactly as it came from the camera.</span></span> <span data-ttu-id="b3ef8-115">In Fällen, in denen der Codec-Autor die Codierung nicht aktivieren möchte, ist es immer noch erforderlich, einen rudimentären Encoder zu implementieren, um das Hinzufügen von Metadaten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-115">In cases where the codec author doesn’t want to enable encoding, it is still necessary to implement a rudimentary encoder just to enable adding metadata.</span></span> <span data-ttu-id="b3ef8-116">In diesem Fall muss der Encoder nur die Methoden unterstützen, die für das Schreiben von Metadaten erforderlich sind, und die Bildbits können unverändert vom Decoder kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="b3ef8-116">In that case, the encoder need only support those methods necessary for writing metadata, and can copy the image bits untouched from the decoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3ef8-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3ef8-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3ef8-118">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="b3ef8-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b3ef8-119">**Iwicbitmapcoder**</span><span class="sxs-lookup"><span data-stu-id="b3ef8-119">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

<span data-ttu-id="b3ef8-120">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b3ef8-120">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b3ef8-121">Implementieren von IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="b3ef8-121">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="b3ef8-122">Encoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b3ef8-122">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="b3ef8-123">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="b3ef8-123">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="b3ef8-124">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="b3ef8-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



