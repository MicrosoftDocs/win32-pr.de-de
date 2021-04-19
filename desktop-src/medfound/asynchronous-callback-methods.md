---
description: Asynchrone Rückruf Methoden
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Asynchrone Rückruf Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346470"
---
# <a name="asynchronous-callback-methods"></a>Asynchrone Rückruf Methoden

Media Foundation bietet eine konsistente Methode zum Implementieren von asynchronen Methoden mithilfe einer Rückruf Schnittstelle.

In diesem Abschnitt wird beschrieben, wie die Rückruf Schnittstelle implementiert wird und wie asynchrone Methoden geschrieben werden, die diese Schnittstelle verwenden. Es enthält die folgenden Themen.



| Thema                                                                                | BESCHREIBUNG                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Aufrufen von asynchronen Methoden](calling-asynchronous-methods.md)                     | Vorgehensweise beim Abrufen von asynchronen Methoden in Media Foundation.                                               |
| [Implementieren des asynchronen Rückrufs](implementing-the-asynchronous-callback.md) | Implementierung der Rückruf Methode in der [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle. |
| [Unterstützen mehrerer Rückrufe](supporting-multiple-callbacks.md)                   | Unterstützung mehrerer Rückrufe innerhalb derselben C++-Klasse.                                        |
| [Arbeits Warteschlangen](work-queues.md)                                                       | Arbeits Warteschlangen stellen eine effiziente Möglichkeit dar, asynchrone Vorgänge in einem anderen Thread auszuführen.          |
| [Schreiben einer asynchronen Methode](writing-an-asynchronous-method.md)                 | Vorgehensweise beim Implementieren von asynchronen Methoden in Media Foundation.                                          |
| [Benutzerdefinierte asynchrone Ergebnis Objekte](custom-asynchronous-result-objects.md)         | Bereitstellen einer benutzerdefinierten Implementierung der [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle.   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Imfasynccallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**Imfasynkresult-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



