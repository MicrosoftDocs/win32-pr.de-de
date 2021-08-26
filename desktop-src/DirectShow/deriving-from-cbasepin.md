---
description: Ableiten von CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Ableiten von CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07eb76fc2913152a69ec729f49826e8b35f1524a3841c5e0d3085ea0634f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079260"
---
# <a name="deriving-from-cbasepin"></a>Ableiten von CBasePin

Um einen Pin mit [**CBasePin**](cbasepin.md)zu implementieren, müssen Sie eine neue Klasse von der Basisklasse ableiten und mehrere ihrer Methoden überschreiben. Sie müssen die folgenden Methoden überschreiben:

-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Sie müssen wahrscheinlich diese zusätzlichen Methoden überschreiben:

-   [**CBasePin::Active**](cbasepin-active.md)
-   [**CBasePin::BreakConnect**](cbasepin-breakconnect.md)
-   [**CBasePin::CheckConnect**](cbasepin-checkconnect.md)
-   [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md)
-   [**CBasePin::EndOfStream**](cbasepin-endofstream.md)
-   [**CBasePin::Inactive**](cbasepin-inactive.md)
-   [**CBasePin::Notify**](cbasepin-notify.md)
-   [**CBasePin::Run**](cbasepin-run.md)

Schließlich müssen Sie die [**Methoden IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) und [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) implementieren.

Einige dieser Methoden werden in Basisklassen implementiert, die von **CBasePin** abgeleitet werden, z. B. [**CBaseInputPin**](cbaseinputpin.md) und [**CBaseOutputPin.**](cbaseoutputpin.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



