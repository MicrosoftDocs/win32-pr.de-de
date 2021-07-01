---
description: Der Registrierungsschlüssel EUDCCodeRange definiert EUDC-Codebereiche (End-User-Defined Character) für verschiedene Codepages (Zeichensätze).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120675"
---
# <a name="eudccoderange"></a><span data-ttu-id="80cb4-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="80cb4-103">EUDCCodeRange</span></span>

<span data-ttu-id="80cb4-104">Der Registrierungsschlüssel EUDCCodeRange definiert [EUDC-Codebereiche (End-User-Defined Character)](end-user-defined-characters.md) für verschiedene Codepages (Zeichensätze).</span><span class="sxs-lookup"><span data-stu-id="80cb4-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="80cb4-105">Sie wird nur von Tools verwendet, die EUDCs erstellen, und ist für EUDC-Benutzer nicht direkt von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="80cb4-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="80cb4-106">Dieser Registrierungsschlüssel hat den folgenden Registrierungsspeicherort:</span><span class="sxs-lookup"><span data-stu-id="80cb4-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="80cb4-107">HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="80cb4-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="80cb4-108">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="80cb4-108">The format is:</span></span>

<span data-ttu-id="80cb4-109">EUDCCodeRange CodePage=FromTo \[ , FromTo\]</span><span class="sxs-lookup"><span data-stu-id="80cb4-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="80cb4-110">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="80cb4-110">where:</span></span>



| <span data-ttu-id="80cb4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="80cb4-111">Value</span></span>         | <span data-ttu-id="80cb4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80cb4-112">Description</span></span>                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cb4-113">CodePage</span><span class="sxs-lookup"><span data-stu-id="80cb4-113">CodePage</span></span> | <span data-ttu-id="80cb4-114">Eine der Zeichenfolgen "932" (Japanisch), "936" (vereinfachtes Chinesisch), "949" (Koreanisch), "950" (traditionelles Chinesisch) oder "Unicode" (Unicode).</span><span class="sxs-lookup"><span data-stu-id="80cb4-114">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="80cb4-115">Es werden keine anderen Werte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="80cb4-115">No other values are supported.</span></span>                                     |
| <span data-ttu-id="80cb4-116">FromTo</span><span class="sxs-lookup"><span data-stu-id="80cb4-116">FromTo</span></span>   | <span data-ttu-id="80cb4-117">Zeichenfolgenwert, der aus einem Paar aus vierstelligen Hexadezimalwerten besteht, getrennt durch einen Bindestrich (-).</span><span class="sxs-lookup"><span data-stu-id="80cb4-117">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="80cb4-118">Bis zu vier FromTo-Werte können angegeben werden, aber jeder muss durch ein Komma (,) vom vorherigen Wert getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="80cb4-118">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="80cb4-119">Im Folgenden sind die richtigen Werte für den Registrierungseintrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="80cb4-119">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="80cb4-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80cb4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80cb4-121">EUDC-Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="80cb4-121">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="80cb4-122">EUDC</span><span class="sxs-lookup"><span data-stu-id="80cb4-122">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



