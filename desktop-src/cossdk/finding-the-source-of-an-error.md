---
description: Ermitteln der Fehlerquelle
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Ermitteln der Fehlerquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041503"
---
# <a name="finding-the-source-of-an-error"></a>Ermitteln der Fehlerquelle

Mithilfe von com+ und anderen Tools können Sie die Quelle diagnostizieren und eine Beschreibung der Anwendungsfehler abrufen. Wenn Sie feststellen, dass der Anwendungsfehler durch com+ verursacht wird, können Sie die Fehlermeldung mit der Datei "Winerror. h" oder mithilfe des Microsoft Visual C++ Fehler-Hilfsprogramms interpretieren.

Wenn die Serveranwendung ausfällt oder unerwartetes Verhalten verursacht, müssen Sie zuerst bestimmen, wo der Fehler aufgetreten ist. Das System Ereignisanzeige nachverfolgt Anwendungs-, Sicherheits-und Systemereignisse. Viele "Stille" Fehler werden hier aufgezeichnet. Allerdings werden nicht alle Fehler in der Ereignisanzeige angezeigt.

Zuerst sollten Sie auf das Anwendungsprotokoll in der Ereignisanzeige verweisen, um die Anwendung zu überprüfen, die der Ereignismeldung zugeordnet ist. (Da Sie auch Ereignisprotokolle archivieren können, können Sie einen Ereignis Verlauf des Fehlers nachverfolgen.) Wenn Sie in Ihrem Protokoll auf einen Eintrag doppelklicken, wird eine Seite mit **Ereignis Eigenschaften** aktiviert, die weitere Informationen über das System Ereignis bereitstellt.

Weitere Informationen zum Debuggen einer COM+-Anwendung finden Sie unter [Debuggen von com+-Anwendungen](debugging-com--applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehler Isolation und FailFast-Richtlinie](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Ändern der Rückgabewerte durch com+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretieren von Fehler Codes](interpreting-error-codes.md)
</dt> <dt>

[Strategien für die Behandlung von Fehlern in com+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Problembehandlung](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



