---
description: Identifizieren gültiger DVD-Vorgänge
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identifizieren gültiger DVD-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392769"
---
# <a name="identifying-valid-dvd-operations"></a>Identifizieren gültiger DVD-Vorgänge

Verschiedene Faktoren bestimmen, ob ein angegebener DVD-Vorgang durchgeführt werden kann:

-   Die aktuelle Domäne. Einige Befehle sind nur in bestimmten Domänen gültig. Wenn sich die Domäne ändert, sendet der Navigator ein EC- \_ DVD- \_ Domänen \_ Änderungs Ereignis. Sie können auch [**IDvdInfo2:: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) aufrufen, um die aktuelle Domäne abzurufen.
-   UOPs-Flags. Dies sind Flags, die auf die Festplatte geschrieben werden und angeben, welche Vorgänge zulässig sind. Wenn sich die Flags ändern, sendet der Navigator ein \_ gültiges UOPs-Änderungs Ereignis für eine EC-DVD \_ \_ \_ mit den neuen Flags. Sie können auch [**IDvdInfo2:: getcurrentuops**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) aufrufen, um die aktuellen UOPs-Flags zu erhalten.
-   DVD-Inhalt. Einige Befehle sind möglicherweise auf Grundlage des Inhalts der DVD nicht relevant. Beispielsweise kann die [**IDvdControl2:: selectangle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) -Methode gemäß der aktuellen Domäne und den UOPs-Flags zulässig sein, aber das Video hat möglicherweise nur einen Winkel. In diesem Fall ist der **selectangle** -Befehl zulässig, ist jedoch keine sinnvolle Option.

Wenn Sie zweifelhaft sind, gestatten Sie eine Aktion. Im schlimmsten Fall tritt bei der [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Methode ein Fehler auf, und Sie können dem Benutzer Feedback geben. Das Feedback sollte relativ unaufdringlich sein. Beispielsweise können Sie ein kleines rotes X blinken, um den Benutzer zu benachrichtigen. Der DVD-Navigator gibt VFW \_ e \_ DVD \_ invaliddomain zurück, wenn die Domäne einen Vorgang untersagt, und VFW \_ e \_ DVD-Vorgang wird verhindert, \_ \_ Wenn die UOPs-Flags einen Vorgang verbieten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



