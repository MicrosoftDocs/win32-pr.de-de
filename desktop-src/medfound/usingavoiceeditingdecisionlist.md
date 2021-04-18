---
description: Verwenden einer Bearbeitungs Entscheidungs Liste zum Codieren von Stimme
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Verwenden einer Bearbeitungs Entscheidungs Liste zum Codieren von Stimme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343421"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a><span data-ttu-id="e5937-103">Verwenden einer Bearbeitungs Entscheidungs Liste zum Codieren von Stimme</span><span class="sxs-lookup"><span data-stu-id="e5937-103">Using an Editing Decision List for Encoding Voice</span></span>

<span data-ttu-id="e5937-104">Bei einer Bearbeitungs Entscheidungs Liste (EDL) handelt es sich um Daten, die einem Codec übergeben werden und Informationen darüber bereitstellen, wie bestimmte Inhalts Teile codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5937-104">An editing decision list (EDL), is data given to a codec that provides information about how specific portions of content should be encoded.</span></span> <span data-ttu-id="e5937-105">Der Windows Media Audio 9 Voice Codec unterstützt eine einfache EDL, in der Sie die Teile von Inhalten angeben können, die Musik enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5937-105">The Windows Media Audio 9 Voice codec supports a simple EDL in which you can specify the portions of content that contain music.</span></span> <span data-ttu-id="e5937-106">Standardmäßig erkennt der Codec bei der Konfiguration zum Codieren von gemischtem Inhalt selbst Durchgänge von Musik selbst.</span><span class="sxs-lookup"><span data-stu-id="e5937-106">By default, the codec detects passages of music itself when configured to encode mixed content.</span></span> <span data-ttu-id="e5937-107">Sie sollten eine EDL nur dann verwenden, wenn der Codec die Inhaltstypen nicht ordnungsgemäß erkennt.</span><span class="sxs-lookup"><span data-stu-id="e5937-107">You should use an EDL only if the codec is not detecting the content types correctly.</span></span>

<span data-ttu-id="e5937-108">Um eine EDL zu verwenden, muss der sprach Encoder so festgelegt werden, dass gemischter Inhalt codiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5937-108">To use an EDL, the voice encoder must be set to encode mixed content.</span></span> <span data-ttu-id="e5937-109">Konfigurieren Sie den Modus des voicecodec als "gemischt", indem Sie die Eigenschaft " [mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) " auf "2" festlegen.</span><span class="sxs-lookup"><span data-stu-id="e5937-109">Configure the mode of the voice codec to "mixed" by setting the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to 2.</span></span> <span data-ttu-id="e5937-110">Legen Sie die EDL mithilfe der Eigenschaft [mfpkey \_ wmavoice \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) fest.</span><span class="sxs-lookup"><span data-stu-id="e5937-110">Set the EDL using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span> <span data-ttu-id="e5937-111">Der Wert dieser Eigenschaft ist eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste der Zeit Bereiche im Inhalt enthält, die als Musik codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5937-111">The value of this property is a string containing a comma-delimited list of the time ranges in the content that should be encoded as music.</span></span> <span data-ttu-id="e5937-112">Das erste Element in der Liste ist die Version von EDL, die immer 1 ist.</span><span class="sxs-lookup"><span data-stu-id="e5937-112">The first item in the list is the version of the EDL, which is always 1.</span></span> <span data-ttu-id="e5937-113">Das zweite Element ist die Anzahl der in der Liste beschriebenen Musik Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="e5937-113">The second item is the number of music sections described in the list.</span></span> <span data-ttu-id="e5937-114">Auf das zweite Element folgt eine Reihe von Werten, die dem zweiten Element entsprechen. Jedes Wertepaar beschreibt den Anfang und den Endpunkt einer Musik Passage im Inhalt in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="e5937-114">Following the second item are a number of pairs of values equal to the second item; each pair of values describes the starting and ending point of a music passage in the content, in milliseconds.</span></span>

<span data-ttu-id="e5937-115">Beispielsweise gibt die EDL-Zeichenfolge "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" vier musikalische Passagen an, von denen jede eine Sekunde lang ist.</span><span class="sxs-lookup"><span data-stu-id="e5937-115">For example, the EDL string "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifies four musical passages, each of which is one second long.</span></span> <span data-ttu-id="e5937-116">Wenn die Informationen in der EDL-Zeichenfolge ungültig sind, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e5937-116">If the information in the EDL string is invalid, it is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5937-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5937-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5937-118">Verwenden des Windows Media Audio 9-Sprach Codecs</span><span class="sxs-lookup"><span data-stu-id="e5937-118">Using the Windows Media Audio 9 Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="e5937-119">Arbeiten mit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="e5937-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



