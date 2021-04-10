---
description: Die audiostreamsavailable-Eigenschaft ruft die Anzahl der Audiostreams ab, die im aktuellen Titel verfügbar sind.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Audiostreamsavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860198"
---
# <a name="audiostreamsavailable-property"></a><span data-ttu-id="9d349-103">Audiostreamsavailable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9d349-103">AudioStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="9d349-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9d349-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9d349-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9d349-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9d349-106">Die `AudioStreamsAvailable` -Eigenschaft ruft die Anzahl der Audiostreams ab, die im aktuellen Titel verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9d349-106">The `AudioStreamsAvailable` property retrieves the number of audio streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="9d349-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d349-107">Return Value</span></span>

<span data-ttu-id="9d349-108">Gibt einen ganzzahligen Wert zwischen 1 und 8 zurück, der die Anzahl der im aktuellen Titel verfügbaren Audiostreams darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d349-108">Returns an integer value from 1 through 8 representing the number of audio streams available in the current title.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d349-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d349-109">Remarks</span></span>

<span data-ttu-id="9d349-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="9d349-110">This property is read-only with no default value.</span></span> <span data-ttu-id="9d349-111">Die primäre Verwendung mehrerer Audiodatenströme besteht darin, Movie Soundtracks in mehr als einer Sprache bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d349-111">The primary use of multiple audio streams is to provide movie soundtracks in more than one language.</span></span> <span data-ttu-id="9d349-112">In der Regel sind nicht für alle Titel auf einem Datenträger alle Audiostreams aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9d349-112">Typically, not every title on a disc has all audio streams enabled.</span></span> <span data-ttu-id="9d349-113">Beispielsweise kann der Feature Movie Soundtracks in drei verschiedenen Sprachen enthalten, aber die nach spannenden enthalten möglicherweise nur einen englischen Sound.</span><span class="sxs-lookup"><span data-stu-id="9d349-113">For example, the feature movie might have soundtracks in three different languages, but the trailers might have only an English soundtrack.</span></span> <span data-ttu-id="9d349-114">Bevor ein Benutzer einen Stream auswählen kann, muss die Anwendung bestimmen, welche Streams innerhalb des aktuellen Titels verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9d349-114">Before a user can select a stream, the application must determine which streams are available within the current title.</span></span> <span data-ttu-id="9d349-115">Beachten Sie, dass bestimmte Streams durch einen Index von 0 bis 7 identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9d349-115">Note that particular streams are identified by an index from zero through 7.</span></span>

<span data-ttu-id="9d349-116">Auf den Datenträgern wird in der Regel ein Menü mit den verfügbaren Sound Spuren angezeigt, sodass der Benutzer den Audiostream auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="9d349-116">Discs generally present a menu showing the available soundtracks, enabling the user to select the audio stream to enable.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d349-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d349-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d349-118">**Getaudiolanguage**</span><span class="sxs-lookup"><span data-stu-id="9d349-118">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> </dl>

 

 



