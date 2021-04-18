---
description: Ableiten von cbasepin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Ableiten von cbasepin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344581"
---
# <a name="deriving-from-cbasepin"></a>Ableiten von cbasepin

Zum Implementieren einer PIN mit [**cbasepin**](cbasepin.md)müssen Sie eine neue Klasse von der Basisklasse ableiten und mehrere ihrer Methoden überschreiben. Sie müssen die folgenden Methoden überschreiben:

-   [**Cbasepin:: checkmediatype**](cbasepin-checkmediatype.md)
-   [**Cbasepin:: getmediatype**](cbasepin-getmediatype.md)

Sie müssen diese zusätzlichen Methoden wahrscheinlich außer Kraft setzen:

-   [**Cbasepin:: Active**](cbasepin-active.md)
-   [**Cbasepin:: breakconnect**](cbasepin-breakconnect.md)
-   [**Cbasepin:: checkConnect**](cbasepin-checkconnect.md)
-   [**Cbasepin:: completeconnect**](cbasepin-completeconnect.md)
-   [**Cbasepin:: EndOf Stream**](cbasepin-endofstream.md)
-   [**Cbasepin:: inaktiv**](cbasepin-inactive.md)
-   [**Cbasepin:: notify**](cbasepin-notify.md)
-   [**Cbasepin:: Run**](cbasepin-run.md)

Schließlich müssen Sie die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -und [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methoden implementieren.

Einige dieser Methoden werden in Basisklassen implementiert, die von **cbasepin** abgeleitet werden, z. b. [**cbaseingeputpin**](cbaseinputpin.md) und [**cbaseoutputpin**](cbaseoutputpin.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cbasepin**](cbasepin.md)
</dt> </dl>

 

 



