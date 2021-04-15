---
description: Die isaudiostreamaktivierte-Methode ruft einen Wert ab, der angibt, ob der angegebene Audiostream im aktuellen Titel aktiviert ist.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Isaudiostreamaktivierte Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520395"
---
# <a name="isaudiostreamenabled-method"></a><span data-ttu-id="3b8bf-103">Isaudiostreamaktivierte Methode</span><span class="sxs-lookup"><span data-stu-id="3b8bf-103">IsAudioStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="3b8bf-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3b8bf-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3b8bf-106">Die `IsAudioStreamEnabled` -Methode ruft einen Wert ab, der angibt, ob der angegebene Audiostream im aktuellen Titel aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-106">The `IsAudioStreamEnabled` method retrieves a value indicating whether the specified audio stream is enabled in the current title.</span></span>

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="3b8bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b8bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b8bf-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*</span><span class="sxs-lookup"><span data-stu-id="3b8bf-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="3b8bf-109">Gibt den Audiodatenstrom als ganzzahligen Wert zwischen 0 und 7 an.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-109">Specifies the audio stream as an Integer value from 0 through 7.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b8bf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b8bf-110">Return Value</span></span>

<span data-ttu-id="3b8bf-111">Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Audiodatenstrom für den aktuellen Titel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-111">Returns a Boolean value indicating whether the specified audio stream is available for the current title.</span></span> <span data-ttu-id="3b8bf-112">"True" bedeutet, dass Sie verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-112">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b8bf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b8bf-113">Remarks</span></span>

<span data-ttu-id="3b8bf-114">Obwohl eine CD bis zu acht unabhängige Audiodatenströme enthalten kann, ist jeder Stream nicht notwendigerweise für jeden Titel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-114">Although a disc can contain up to eight independent audio streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="3b8bf-115">Beispielsweise kann ein hauptfilmtitel drei Audiodatenströme für Englisch, Spanisch und Japanisch enthalten, aber der Titel "Kommende Attraktionen" hat möglicherweise nur einen Audiostream in englischer Sprache.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-115">For example, a main movie title might have three audio streams for English, Spanish, and Japanese, but the "Coming Attractions" title might have only one audio stream in English.</span></span> <span data-ttu-id="3b8bf-116">Überprüfen Sie vor dem Festlegen der [**currentaudiostream**](currentaudiostream-property.md) -Eigenschaft immer, ob ein Datenstrom für einen Titel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-116">Always verify that a stream is available for a title before setting the [**CurrentAudioStream**](currentaudiostream-property.md) property.</span></span>

 

 



