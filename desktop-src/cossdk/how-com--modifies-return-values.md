---
description: Ändern von Rückgabewerten durch COM+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Ändern von Rückgabewerten durch COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ba2b8a9761c7bb669982b47d94b7d522298fa6d557d197d24ea4cb5e56a0df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813821"
---
# <a name="how-com-modifies-return-values"></a>Ändern von Rückgabewerten durch COM+

COM+ ändert nie den Rückgabewert eines **HRESULT, das** auf einen Fehler hinweist, z. B. E \_ UNEXPECTED oder E \_ FAIL. Wenn ein Objekt mit COM+-Funktionalität jedoch einen **HRESULT-Wert** zurückgibt, der den Erfolg angibt (z. B. S \_ OK, S \_ FALSE oder NOERROR), konvertiert COM+ das **HRESULT** manchmal in einen COM+-Fehlercode, bevor es an den Aufrufer zurückgegeben wird.

Wenn eine Anwendung beispielsweise \_ S OK zurückgibt, nachdem [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)aufgerufen wurde, wird das **HRESULT** in CONTEXT \_ E ABORTED konvertiert, wenn das Objekt der Stamm einer Transaktion ist, für die kein Commit ausgeführt werden \_ kann.

Wenn COM+ einen **HRESULT-Wert** konvertiert, werden alle Ausgabeparameter der Methode gelöscht. Zurückgegebene Verweise werden freigegeben, und die Werte der zurückgegebenen Objektzeiger werden auf **NULL** festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerisolation und Failfast-Richtlinie](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Suchen der Fehlerquelle](finding-the-source-of-an-error.md)
</dt> <dt>

[Interpretieren von Fehlercodes](interpreting-error-codes.md)
</dt> <dt>

[Strategien zur Behandlung von Fehlern in COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Problembehandlung](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



