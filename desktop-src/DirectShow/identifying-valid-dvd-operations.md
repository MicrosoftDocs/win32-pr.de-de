---
description: Identifizieren gültiger DVD-Vorgänge
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identifizieren gültiger DVD-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd1b99a38949ca0ff54d391e9ad5458bbe854a5c4af4140b15deaf4177147aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051980"
---
# <a name="identifying-valid-dvd-operations"></a>Identifizieren gültiger DVD-Vorgänge

Mehrere Faktoren bestimmen, ob Sie einen bestimmten DVD-Vorgang ausführen können:

-   Die aktuelle Domäne. Einige Befehle sind nur in bestimmten Domänen gültig. Wenn sich die Domäne ändert, sendet der Navigator ein EC \_ DVD \_ DOMAIN \_ CHANGE-Ereignis. Sie können auch [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) aufrufen, um die aktuelle Domäne zu erhalten.
-   UOPS-Flags. Dies sind Flags, die auf den Datenträger geschrieben werden und angeben, welche Vorgänge zulässig sind. Wenn sich die Flags ändern, sendet der Navigator ein EC \_ DVD \_ VALID \_ UOPS \_ CHANGE-Ereignis mit den neuen Flags. Sie können auch [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) aufrufen, um die aktuellen UOPS-Flags zu erhalten.
-   DVD-Inhalt. Einige Befehle sind basierend auf dem Inhalt der DVD möglicherweise nicht relevant. Beispielsweise kann die [**IDvdControl2::SelectAngle-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) gemäß der aktuellen Domäne und den UOPS-Flags zulässig sein, aber das Video kann nur einen Winkel haben. In diesem Fall ist der **SelectAngle-Aufruf** zulässig, ist aber keine sinnvolle Option.

Lassen Sie im Zweifelsfall eine Aktion zu. Im schlimmsten Fall kann [**die IDvdControl2-Methode**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) nicht verwendet werden, und Sie können dem Benutzer Feedback geben. Das Feedback sollte relativ unauffällig sein. Beispielsweise können Sie ein kleines rotes X blinken, um den Benutzer zu warnen. Der DVD-Navigator gibt die VFW-E-DVD INVALIDDOMAIN zurück, wenn die Domäne einen Vorgang verhindert, und VFW E DVD OPERATION BEFIEED, wenn die \_ \_ \_ \_ \_ \_ \_ UOPS-Flags einen Vorgang verhindern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



