---
description: Das Policy-Objekt wird verwendet, um den Zugriff auf die lokale Sicherheits Autorität (LSA) zu steuern, und enthält Informationen, die für das gesamte System gelten oder Standardwerte für das System festlegen.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Policy-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcceec080d51f9c432ab2d63b8eeb26b3211cd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862303"
---
# <a name="policy-object"></a>Policy-Objekt

Das **Policy** -Objekt wird verwendet, um den Zugriff auf die [*Lokale Sicherheits Autorität*](/windows/desktop/SecGloss/l-gly) (LSA) zu steuern, und enthält Informationen, die für das gesamte System gelten oder Standardwerte für das System festlegen. Jedes System verfügt nur über ein **Richtlinien** Objekt. Dieses **Richtlinien** Objekt wird vom LSA erstellt, wenn das System gestartet wird, und Anwendungen können es nicht erstellen oder zerstören.

Zu den in einem **Richtlinien** Objekt gespeicherten Informationen gehören:

-   Standardmäßiges System Arbeitsspeicher-Kontingent. Sofern nicht anders angegeben, wird jedem Benutzer, der sich am System anmeldet, dieses Speicher Kontingent zugewiesen. Besondere Arbeitsspeicher Kontingente können Einzelpersonen oder Gruppenmitgliedern oder lokalen Gruppen über ein [**Konto**](account-object.md) Objekt zugewiesen werden.
-   System weite Sicherheits Überprüfungsanforderungen.
-   Der Name und die SID der Konto Domäne dieses Systems.
-   Informationen zur primären Domäne dieses Systems. Diese Informationen umfassen den Namen und die SID der primären Domäne, den Namen des Kontos innerhalb der primären Domäne, das für Authentifizierungsanforderungen verwendet werden soll, die Namen-und sid-Übersetzungen und das Abrufen der Namen von Domänen Controllern innerhalb der Domäne. Diese Namen sind möglicherweise veraltet und sollten nur als Hinweis verwendet werden. Die Reihenfolge dieser Liste wird als signifikant angesehen und wird beibehalten. Dies ermöglicht beispielsweise, dass der Vorname in der Liste den letzten bekannten primären Domänen Controller darstellt.
-   Informationen dazu, ob die LSA die Master Kopie der Richtlinien Informationen oder eines Replikats enthält. Es wird nur ein Teil der Richtlinien Informationen repliziert. der Rest wird pro System festgelegt.

Die Felder " **accountdomain** " und " **primarydomain** " des Objekts " **Policy** " werden je nach Art der System-und Vertrauens Stellungen für verschiedene Zwecke verwendet:

-   Auf einem System, das nicht über eine primäre Domäne verfügt, enthält das Feld **accountdomain** den Namen und die SID der lokalen Konto Domäne des Systems, die mit dem Computernamen identisch ist. Das Feld **primarydomain** enthält den Namen der Arbeitsgruppe, in der dieser Computer Mitglied ist. Die Objekte der [**Treuhänder Domäne**](trusteddomain-object.md) werden mit einer Ausnahme ignoriert – es darf kein " **Treuhänder** "-Objekt mit dem gleichen Namen wie die Arbeitsgruppe vorhanden sein, da es so angezeigt wird, als ob es sich um die primäre Domäne des Computers handelt.
-   Auf einem System mit einer primären Domäne identifiziert das Feld **accountdomain** den Namen und die SID der lokalen Konto Domäne wie zuvor. Das Feld **primarydomain** enthält jedoch den Namen und die SID der primären Domäne für das System. Außerdem sollte ein " [**treuddomain**](trusteddomain-object.md) "-Objekt mit dem Namen und der SID im Feld " **primarydomain** " angegeben werden. Dieses Objekt " **Treuhänder Domäne** " enthält die Konto-und Server Informationen, die erforderlich sind, um einen sicheren Kanal zu einem Domänen Controller in der primären Domäne einzurichten. Alle anderen Objekte der **Treuhänder Domäne** werden ignoriert.
-   Auf Domänen Controllern identifiziert das Feld **accountdomain** die lokale Konto Domäne für das System. der Kontoname ist jedoch vom Benutzer zugewiesen, anstelle eines bekannten namens. Da die primäre Domäne mit der Konto Domäne identisch ist, muss das Feld **primarydomain** denselben Wert wie das Feld **accountdomain** enthalten. Außerdem wird erwartet, dass alle [**trustddomain**](trusteddomain-object.md) -Objekte gültig sind und Vertrauens Stellungen mit anderen Domänen darstellen. Wenn das System keine anderen Domänen als vertrauenswürdig einstuft, sollten keine vertrauenswürdigen **Domänen** Objekte vorhanden sein.

 

 
