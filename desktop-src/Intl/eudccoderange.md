---
description: Der Registrierungsschlüssel eudccoderange definiert Endbenutzer definierte Zeichen (EUDC)-Code Bereiche für verschiedene Codepages (Zeichensätze).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: Eudccoderange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352275"
---
# <a name="eudccoderange"></a><span data-ttu-id="0d099-103">Eudccoderange</span><span class="sxs-lookup"><span data-stu-id="0d099-103">EUDCCodeRange</span></span>

<span data-ttu-id="0d099-104">Der Registrierungsschlüssel eudccoderange definiert [Endbenutzer definierte Zeichen (EUDC)-](end-user-defined-characters.md) Code Bereiche für verschiedene Codepages (Zeichensätze).</span><span class="sxs-lookup"><span data-stu-id="0d099-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="0d099-105">Sie wird nur von Tools verwendet, die eudcs erstellen, und ist nicht für EUDC-Benutzer von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="0d099-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="0d099-106">Dieser Registrierungsschlüssel weist den folgenden Registrierungs Speicherort auf:</span><span class="sxs-lookup"><span data-stu-id="0d099-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="0d099-107">HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ nls \\ Codepage \\ eudccoderange</span><span class="sxs-lookup"><span data-stu-id="0d099-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="0d099-108">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="0d099-108">The format is:</span></span>

<span data-ttu-id="0d099-109">Eudccoderange Codepage = FromTo \[ , FromTo\]</span><span class="sxs-lookup"><span data-stu-id="0d099-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="0d099-110">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="0d099-110">where:</span></span>



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d099-111">CodePage</span><span class="sxs-lookup"><span data-stu-id="0d099-111">CodePage</span></span> | <span data-ttu-id="0d099-112">Eine der Zeichen folgen "932" (Japanisch), "936" (vereinfachtes Chinesisch), "949" (Koreanisch), "950" (traditionelles Chinesisch) oder "Unicode" (Unicode).</span><span class="sxs-lookup"><span data-stu-id="0d099-112">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="0d099-113">Es werden keine anderen Werte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d099-113">No other values are supported.</span></span>                                     |
| <span data-ttu-id="0d099-114">FromTo</span><span class="sxs-lookup"><span data-stu-id="0d099-114">FromTo</span></span>   | <span data-ttu-id="0d099-115">Ein Zeichen folgen Wert, der aus einem Paar von vierstelligen hexadezimalen Werten besteht, die durch einen Bindestrich (-) getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="0d099-115">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="0d099-116">Es können bis zu vier FromTo-Werte angegeben werden, aber beide müssen vom vorherigen Wert durch ein Komma (,) getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="0d099-116">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="0d099-117">Im folgenden finden Sie die richtigen Werte für den Registrierungs Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0d099-117">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="0d099-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d099-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d099-119">EUDC-Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="0d099-119">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="0d099-120">EUDC</span><span class="sxs-lookup"><span data-stu-id="0d099-120">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



