---
description: Asynchrone Rückrufmethoden
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Asynchrone Rückrufmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e59fec2423d6bc1b02a3f5ce05855419596bc92ea54062303ebd1315d087e489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606710"
---
# <a name="asynchronous-callback-methods"></a>Asynchrone Rückrufmethoden

Media Foundation bietet eine konsistente Möglichkeit, asynchrone Methoden mithilfe einer Rückrufschnittstelle zu implementieren.

In diesem Abschnitt wird beschrieben, wie die Rückrufschnittstelle implementiert wird und wie asynchrone Methoden geschrieben werden, die diese Schnittstelle verwenden. Sie enthält die folgenden Themen.



| Thema                                                                                | Beschreibung                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Aufrufen asynchroner Methoden](calling-asynchronous-methods.md)                     | Aufrufen asynchroner Methoden in Media Foundation.                                               |
| [Implementieren des asynchronen Rückrufs](implementing-the-asynchronous-callback.md) | Implementieren der Rückrufmethode in [**derASYNCCallback-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) |
| [Unterstützen mehrerer Rückrufe](supporting-multiple-callbacks.md)                   | Unterstützung mehrerer Rückrufe innerhalb derselben C++-Klasse.                                        |
| [Arbeitswarteschlangen](work-queues.md)                                                       | Arbeitswarteschlangen bieten eine effiziente Möglichkeit, asynchrone Vorgänge für einen anderen Thread durchzuführen.          |
| [Schreiben einer asynchronen Methode](writing-an-asynchronous-method.md)                 | Implementieren von asynchronen Methoden in Media Foundation.                                          |
| [Benutzerdefinierte asynchrone Ergebnisobjekte](custom-asynchronous-result-objects.md)         | Bereitstellen einer benutzerdefinierten Implementierung [**derASYNCAsyncResult-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASYNCAsyncCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**ASYNCAsyncResult-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



