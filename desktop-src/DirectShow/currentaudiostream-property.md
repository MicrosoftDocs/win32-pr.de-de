---
description: Die currentaudiostream-Eigenschaft legt die Nummer des aktivierten Audiostreams fest oder ruft Sie ab.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Currentaudiostream (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346823"
---
# <a name="currentaudiostream-property"></a><span data-ttu-id="d4070-103">Currentaudiostream (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d4070-103">CurrentAudioStream Property</span></span>

> [!Note]  
> <span data-ttu-id="d4070-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4070-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d4070-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d4070-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d4070-106">Die `CurrentAudioStream` -Eigenschaft legt die Nummer des aktivierten Audiostreams fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="d4070-106">The `CurrentAudioStream` property sets or retrieves the number of the enabled audio stream.</span></span>

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a><span data-ttu-id="d4070-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4070-107">Return Value</span></span>

<span data-ttu-id="d4070-108">Gibt einen ganzzahligen Wert von 0 bis 7 zurück, der den aktuellen Audiostream angibt.</span><span class="sxs-lookup"><span data-stu-id="d4070-108">Returns an integer value from 0 through 7 indicating the current audio stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4070-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4070-109">Remarks</span></span>

<span data-ttu-id="d4070-110">Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="d4070-110">This property is read/write with no default value.</span></span> <span data-ttu-id="d4070-111">Bevor Sie versuchen, einen neuen Audiostream festzulegen, wenden Sie [**isaudiostreamaktivierte**](isaudiostreamenabled-method.md) an, um sicherzustellen, dass der Stream verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d4070-111">Before attempting to set a new audio stream, call [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) to verify that the stream is available.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4070-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4070-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4070-113">**Audiostreamsavailable**</span><span class="sxs-lookup"><span data-stu-id="d4070-113">**AudioStreamsAvailable**</span></span>](audiostreamsavailable-property.md)
</dt> </dl>

 

 



