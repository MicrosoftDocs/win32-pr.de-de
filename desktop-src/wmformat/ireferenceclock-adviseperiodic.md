---
title: IReferenceClock AdvisePeriodic-Methode
description: Diese Methode ist nicht implementiert.
ms.assetid: b34ef914-992e-4ce2-943b-8bc36687a88a
keywords:
- AdvisePeriodic-Methodenfenster Medienformat
- AdvisePeriodic-Methode windows Media Format , IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle windows Media Format , AdvisePeriodic-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.AdvisePeriodic
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2502109f3e28fedc411e69888725360632966e052c44555b25a72978f9cbbe63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701668"
---
# <a name="ireferenceclockadviseperiodic-method"></a>IReferenceClock::AdvisePeriodic-Methode

Diese Methode ist nicht implementiert.

In anderen Implementierungen der **IReferenceClock-Schnittstelle,** z. B. in der DirectShow®-Komponente von Microsoft® DirectX®, wird die **AdvisePeriodic-Methode** verwendet, um eine regelmäßige Empfehlungsanforderung zu erstellen, die das angegebene Ereignisobjekt jedes Mal signalisieren würde, wenn das angegebene Zeitintervall verstrichen ist. Dieses SDK implementiert nicht die Funktionalität dieser Methode, und alle Aufrufe an diese Methode führen zu einem Rückgabewert von E \_ NOTIMPL.

## <a name="syntax"></a>Syntax


```C++
 AdvisePeriodic();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IReferenceClock-Schnittstelle**](ireferenceclock.md)
</dt> </dl>

 

 




