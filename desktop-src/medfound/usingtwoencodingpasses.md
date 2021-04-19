---
description: Die zwei-Pass-Codierung kann für die Konstante Bitrate (CBR) und für die Codierung der Variablen Bitrate (VBR) mit einigen Windows Media-Codecs verwendet werden.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Verwenden von Two-Pass Encoding (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356889"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a><span data-ttu-id="6b2da-103">Verwenden von Two-Pass Encoding (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="6b2da-103">Using Two-Pass Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="6b2da-104">Die zwei-Pass-Codierung kann für die Konstante Bitrate (CBR) und für die Codierung der Variablen Bitrate (VBR) mit einigen Windows Media-Codecs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2da-104">Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs.</span></span> <span data-ttu-id="6b2da-105">Sie können die maximale Anzahl von Codierungs Durchläufen ermitteln, die von einem Codec unterstützt werden, indem Sie die Eigenschaft " [mfpkey \_ passesrecommended](mfpkey-passesrecommendedproperty.md) " abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b2da-105">You can find the maximum number of encoding passes supported by a codec by retrieving the [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) property.</span></span> <span data-ttu-id="6b2da-106">Keines der Codecs unterstützt mehr als zwei Durchgänge.</span><span class="sxs-lookup"><span data-stu-id="6b2da-106">None of the codecs supports more than two passes.</span></span> <span data-ttu-id="6b2da-107">Konfigurieren Sie den DMO so, dass zwei Durchgänge verwendet werden, indem Sie die Eigenschaft " [ \_ passesused" für mfpkey](mfpkey-passesusedproperty.md) auf 2</span><span class="sxs-lookup"><span data-stu-id="6b2da-107">Configure the DMO to use two passes by setting the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2.</span></span>

<span data-ttu-id="6b2da-108">Übermitteln Sie die Beispiele für den Encoder DMO nacheinander, wie Sie es in einem Modus mit nur einem Durchlauf tun würden.</span><span class="sxs-lookup"><span data-stu-id="6b2da-108">Deliver the samples to the encoder DMO one at a time, as you would in a one-pass mode.</span></span> <span data-ttu-id="6b2da-109">Wenn Sie die Eingabe Beispiele für den Vorverarbeitungs Durchlauf verarbeiten, werden bei Aufrufen von [**imediaobject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) oder [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) **S \_ false** zurückgegeben, um anzugeben, dass keine Ausgabe erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="6b2da-109">When you process the input samples for your preprocessing pass, the calls to [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) or [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will return **S\_FALSE**, to indicate that no output is produced.</span></span>

<span data-ttu-id="6b2da-110">Am Ende der ersten Ausführung (nachdem die letzte Eingabe zum ersten Mal verarbeitet wurde) müssen Sie die Eigenschaft " [mfpkey \_ endofpass](mfpkey-endofpassproperty.md) " so festlegen, dass der Codec benachrichtigt wird, dass die nächste verarbeitete Eingabe die erste Eingabe des zweiten bestanden ist.</span><span class="sxs-lookup"><span data-stu-id="6b2da-110">At the end of the first pass (after the last input is processed for the first time), you then must set the [MFPKEY\_ENDOFPASS](mfpkey-endofpassproperty.md) property to notify the codec that the next input processed is the first input of the second pass.</span></span> <span data-ttu-id="6b2da-111">Für diese Eigenschaft ist kein Wert erforderlich. Daher sollten Sie eine leere **Variant** -Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b2da-111">No value is required for this property, so you should use an empty **VARIANT** structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b2da-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b2da-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b2da-113">Windows Media-Codecs</span><span class="sxs-lookup"><span data-stu-id="6b2da-113">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 
