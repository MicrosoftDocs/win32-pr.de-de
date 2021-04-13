---
description: Erzwungene Keyframe-Einfügung
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Erzwungene Keyframe-Einfügung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484075"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a><span data-ttu-id="15592-103">Erzwungene Keyframe-Einfügung (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="15592-103">Forced Key Frame Insertion (Microsoft Media Foundation)</span></span>

<span data-ttu-id="15592-104">Wenn Sie ein Video Encoder-Objekt konfigurieren, können Sie ein maximales Intervall für Keyframes im codierten Inhalt festlegen.</span><span class="sxs-lookup"><span data-stu-id="15592-104">When you configure a video encoder object, you can set a maximum interval for key frames in the encoded content.</span></span> <span data-ttu-id="15592-105">Der Codec platziert jedoch Keyframes innerhalb dieses Intervalls, wie vom Inhalt vorgegeben. das Keyframe-Intervall ist nicht konstant.</span><span class="sxs-lookup"><span data-stu-id="15592-105">However, the codec will place key frames within that interval as dictated by the content; the key frame interval is not constant.</span></span> <span data-ttu-id="15592-106">Bei manchen Anwendungen ist die Keyframe-Distanz sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="15592-106">For some applications, the key frame distance is very important.</span></span> <span data-ttu-id="15592-107">Beispielsweise benötigt eine Anwendung zur Videobearbeitung Keyframes an Positionen, die für einen Editor logisch sind, wie bei Szenen Umbrüchen und Schlag Übergängen.</span><span class="sxs-lookup"><span data-stu-id="15592-107">For example, a video editing application needs key frames at locations that are logical to an editor, like at scene breaks and shot transitions.</span></span>

<span data-ttu-id="15592-108">Erzwungene Keyframe-Einfügung ist eine Funktion, mit der Sie anfordern können, dass ein Eingabe Frame als Keyframe codiert wird.</span><span class="sxs-lookup"><span data-stu-id="15592-108">Forced key frame insertion is a feature that enables you to request that an input frame be encoded as a key frame.</span></span> <span data-ttu-id="15592-109">Der Encoder versucht, diese Anforderungen zu berücksichtigen, aber die für die Codierungs Sitzung konfigurierten Puffer Einstellungen (Bitrate und Puffer Fenster) haben immer Vorrang.</span><span class="sxs-lookup"><span data-stu-id="15592-109">The encoder will try to honor these requests, but the buffer settings (bit rate and buffer window) configured for the encoding session always take precedence.</span></span>

<span data-ttu-id="15592-110">Die Video Encoder-Objekte implementieren erzwungene Keyframe-Einfügevorgänge als Antwort auf eine an das Eingabe Beispiel angefügte Erweiterung für Dateneinheiten.</span><span class="sxs-lookup"><span data-stu-id="15592-110">The video encoder objects implement forced key frame insertion as a response to a data unit extension attached to the input sample.</span></span> <span data-ttu-id="15592-111">Weitere Informationen zu Dateneinheiten Erweiterungen finden Sie unter [Verwenden von Dateneinheiten Erweiterungen](usingdataunitextensions.md).</span><span class="sxs-lookup"><span data-stu-id="15592-111">For more information about data unit extensions, see [Using Data Unit Extensions](usingdataunitextensions.md).</span></span>

<span data-ttu-id="15592-112">Die Erweiterungs Daten für erzwungene Keyframe-Einfügevorgänge werden durch den folgenden GUID-Wert identifiziert: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span><span class="sxs-lookup"><span data-stu-id="15592-112">The extension data for forced key frame insertion is identified by the following GUID value: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span></span> <span data-ttu-id="15592-113">Die einzelnen Erweiterungen sind **boolesche** Werte.</span><span class="sxs-lookup"><span data-stu-id="15592-113">The individual extensions are **BOOL** values.</span></span> <span data-ttu-id="15592-114">Legen Sie den Wert auf **true** fest, um eine Keyframe-Anforderung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="15592-114">Set the value to **TRUE** to indicate a key frame request.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15592-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15592-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15592-116">Verwenden von Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="15592-116">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
</dt> <dt>

[<span data-ttu-id="15592-117">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="15592-117">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



