---
description: Ändern der Rückgabewerte durch com+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Ändern der Rückgabewerte durch com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127033"
---
# <a name="how-com-modifies-return-values"></a>Ändern der Rückgabewerte durch com+

Com+ ändert niemals den Rückgabewert eines **HRESULT** , das einen Fehler angibt, wie z \_ . b. e unerwartete oder e \_ Fail. Wenn ein Objekt, das die com+-Funktionalität verwendet, jedoch einen **HRESULT** -Wert zurückgibt, der einen Erfolg angibt (z. b. s \_ OK, s \_ false oder noError), konvertiert com+ manchmal das **HRESULT** in einen com+-Fehlercode, bevor es zum Aufrufer zurückkehrt.

Wenn eine Anwendung z. b. \_ nach dem Aufruf von [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)den Wert OK zurückgibt, wird das **HRESULT** in den \_ abgebrochenen Kontext E konvertiert, wenn das Objekt der Stamm einer Transaktion ist, für die kein Commit ausgeführt werden kann \_ .

Wenn com+ einen **HRESULT** -Wert konvertiert, löscht er alle Ausgabeparameter der Methode. Zurückgegebene Verweise werden freigegeben, und die Werte der zurückgegebenen Objekt Zeiger werden auf **null** festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehler Isolation und FailFast-Richtlinie](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Ermitteln der Fehlerquelle](finding-the-source-of-an-error.md)
</dt> <dt>

[Interpretieren von Fehler Codes](interpreting-error-codes.md)
</dt> <dt>

[Strategien für die Behandlung von Fehlern in com+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Problembehandlung](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



