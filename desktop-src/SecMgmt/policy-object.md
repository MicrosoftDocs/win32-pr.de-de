---
description: Das Richtlinienobjekt wird verwendet, um den Zugriff auf die Datenbank der lokalen Sicherheitsautorität (Local Security Authority, LSA) zu steuern, und enthält Informationen, die für das gesamte System gelten oder Standardwerte für das System festlegen.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Richtlinienobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49e3dd7a33fd83107f9338783e3b8bdcc68eee7d8c4f927f67a7df1c0262c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005062"
---
# <a name="policy-object"></a>Richtlinienobjekt

Das **Richtlinienobjekt** wird verwendet, um den Zugriff auf die Datenbank der [*lokalen Sicherheitsautorität (Local Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) zu steuern, und enthält Informationen, die für das gesamte System gelten oder Standardwerte für das System festlegen. Jedes System verfügt nur über ein **Policy-Objekt.** Dieses **Richtlinienobjekt** wird vom LSA erstellt, wenn das System gestartet wird, und Anwendungen können es nicht erstellen oder zerstören.

Die in einem **Policy-Objekt** gespeicherten Informationen umfassen Folgendes:

-   Standardspeicherkontingent des Systems. Sofern nicht anders angegeben, wird jedem Benutzer, der sich beim System anmeldet, dieses Speicherkontingent zugewiesen. Spezielle Arbeitsspeicherkontingente können Einzelpersonen oder Mitgliedern von Gruppen oder lokalen Gruppen über ein [**Kontoobjekt**](account-object.md) zugewiesen werden.
-   Systemweite Sicherheitsüberwachungsanforderungen.
-   Der Name und die SID der Kontodomäne dieses Systems.
-   Informationen zur primären Domäne dieses Systems. Diese Informationen umfassen den Namen und die SID der primären Domäne, den Namen des Kontos in der primären Domäne, das für Authentifizierungsanforderungen verwendet werden soll, Namens- und SID-Übersetzungen sowie das Abrufen der Namen von Domänencontrollern innerhalb der Domäne. Diese Namen sind möglicherweise veraltet und sollten nur als Hinweis betrachtet werden. Es wird davon ausgegangen, dass die Reihenfolge dieser Liste signifikant ist und beibehalten wird. Dadurch kann z. B. der Vorname in der Liste den letzten bekannten primären Domänencontroller darstellen.
-   Informationen darüber, ob das LSA die Masterkopie der Richtlinieninformationen oder eines Replikats enthält. Nur ein Teil der Richtlinieninformationen wird repliziert. der Rest wird auf Systembasis eingerichtet.

Die Felder **AccountDomain** und **PrimaryDomain** des **Richtlinienobjekts** werden je nach Typ der System- und Vertrauensstellungen für unterschiedliche Zwecke verwendet:

-   Auf einem System ohne primäre Domäne enthält das Feld **AccountDomain** den Namen und die SID der lokalen Kontodomäne des Systems, die mit dem Computernamen identisch sind. Das Feld **PrimaryDomain** enthält den Namen der Arbeitsgruppe, der dieser Computer angehört. [**TrustedDomain-Objekte**](trusteddomain-object.md) werden mit einer Ausnahme ignoriert. Es kann kein **TrustedDomain-Objekt** mit dem gleichen Namen wie die Arbeitsgruppe vorhanden sein, da es so ausgeht, als wäre es die primäre Domäne des Computers.
-   Auf einem System, das über eine primäre Domäne verfügt, identifiziert das Feld **AccountDomain** den Namen und die SID der lokalen Kontodomäne wie zuvor. Das Feld **PrimaryDomain** enthält jedoch den Namen und die SID der primären Domäne für das System. Darüber hinaus sollte ein [**TrustedDomain-Objekt**](trusteddomain-object.md) mit dem Namen und der SID vorhanden sein, die im Feld **PrimaryDomain** angegeben sind. Dieses **TrustedDomain-Objekt** enthält die Konto- und Serverinformationen, die zum Einrichten eines sicheren Kanals zu einem Domänencontroller in der primären Domäne erforderlich sind. Alle anderen **TrustedDomain-Objekte** werden ignoriert.
-   Auf Domänencontrollern identifiziert das Feld **AccountDomain** die lokale Kontodomäne für das System. Der Kontoname ist jedoch vom Benutzer zugewiesen, anstatt ein bekannter Name zu sein. Da die primäre Domäne mit der Kontodomäne identisch ist, muss das Feld **PrimaryDomain** den gleichen Wert wie das Feld **AccountDomain** enthalten. Darüber hinaus wird erwartet, dass alle [**TrustedDomain-Objekte**](trusteddomain-object.md) gültig sind und Vertrauensstellungen mit anderen Domänen darstellen. Wenn das System anderen Domänen nicht vertraut, sollten keine **TrustedDomain-Objekte** vorhanden sein.

 

 
