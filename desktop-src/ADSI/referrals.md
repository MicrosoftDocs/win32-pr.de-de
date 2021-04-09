---
title: Verweise (ADSI)
description: Verweise werden ausgelöst, wenn der Server, den Sie Abfragen, diese Daten nicht enthält, ihn aber finden kann.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- Verweise auf ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79e6b2e8a737f6bb40386effd68f7f31d8d490d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102330"
---
# <a name="referrals-adsi"></a>Verweise (ADSI)

Verweise werden ausgelöst, wenn der Server, den Sie Abfragen, diese Daten nicht enthält, ihn aber finden kann. Der Zielserver gibt das Resultset zurück, das möglicherweise sowohl die eigentlichen Daten als auch einen Verweis auf einen anderen Server enthält, um die zusätzlichen Daten abzurufen. Durch Aktivieren der *Verweis Verfolgung* verwendet der zugrunde liegende ADSI-Client Code diese Verweis Daten, um zu versuchen, das Zielobjekt von dem Server abzurufen, der in den Verweis Daten beschrieben wird. Beachten Sie, dass die Deaktivierung der Verweis Verfolgung möglicherweise zu einem kleineren Resultset führt, während die Aktivierung der Verweis Verfolgung dazu führen kann, dass eine Abfrage viele Server umfasst. Wenn möglich, ist die empfohlene Lösung die Verwendung des globalen Katalogs.

Weitere Informationen zu Verweise und verweiserweiterverfolgung in Active Directory finden Sie unter " [Verweise](/windows/desktop/AD/referrals)".

Wenn ein Client z. b. Server a (a) anweist, ein Benutzerobjekt (u) abzufragen, kann ein den Client die Suche auf Server b (b) fortsetzen, wenn sich U nicht in einem befindet, aber bekanntermaßen auf B fest. Der Client hat die Möglichkeit, den Verweis nachzuverfolgen. Durch Such Verweise wird der Client von der erweiterten Erkennung der Funktionen der einzelnen Server aufgefordert. Der Client muss jedoch den Typ der Verweise angeben, die ein Server erstellen sollte.

Active Directory bietet Search-Referenz Dienste. Ein Client kann einen der folgenden Arten der Verweis Verfolgung auswählen:

-   Nie: der Server sollte keinen Verweis an einen Client generieren, auch wenn er erkennt, dass die angeforderten Daten von einem anderen Server gespeichert werden.
-   Extern: der Server sollte Verweise generieren, wenn die Anforderung auf einem anderen Server einer anderen Verzeichnisstruktur aufgelöst werden kann. Ein Client fragt z. b. "OU = Sales, DC = fabrikam, DC = com" auf dem Server "fab01" in der Domäne "fabrikam.com" ab. Das Objekt gehört jedoch nicht zu "fab01", aber es ist bekanntermaßen auf dem Server "arc01" in der Domäne "fabrikam.com". Daher verweist "fab01" auf den Client auf "arc01".
-   Untergeordnet: der Server sollte Verweise generieren, wenn die Anforderung auf einem Server aufgelöst werden kann, dessen Name einen zusammenhängenden Pfad vom ursprünglichen Server bildet. Der Suchbereich muss sich auf der Unterstruktur Ebene befinden.

    Server A enthält z. b. Objekte in "DC = Sales, DC = fabrikam, DC = com". Server B enthält Objekte in "DC = Seattle, DC = Sales, DC = fabrikam, DC = com". Beachten Sie, dass der Name von Server B einen zusammenhängenden Pfad von Server a bildet. Wenn ein Client eine Verbindung mit Server a herstellt, fordert eine Unterstruktur Suche in "DC = Sales, DC = fabrikam, DC = com" an und gibt den Verweis auf einen untergeordneten Typ an. das folgende Ereignis tritt auf:

    -   Server A gibt alle-Objekte zurück, die innerhalb des Gültigkeits Bereichs bekannt sind.
    -   Server A informiert den Client, dass die Objekte in "DC = Seattle, DC = Sales, DC = fabrikam, DC = com" auf Server B gefunden werden können.

    Der Client kann sich für den Kontakt zu Server B entscheiden. Wenn dies der Fall ist, tritt das folgende Ereignis auf:

    -   Server B antwortet mit den angeforderten Objekten.
    -   Wenn Server B andere Server im zusammenhängenden Benennungs Pfad erkennt und der Prozess fortgesetzt wird.

-   Immer: der Server generiert Verweise, wenn die Suche auf der Grundlage des externen Typs oder des untergeordneten Typs aufgelöst werden kann.

> [!Note]  
> In Active Directory enthält der globale Katalog alle Objekte in einem bestimmten Unternehmen. Durch das Durchsuchen eines globalen Katalog Servers ergibt sich eine bessere Leistung als das Überschreiten von Verweisen von einem Server auf einen anderen.

 

In den meisten Fällen ist die Verweis Verfolgung für den Aufrufer transparent. Wenn der Verweis auf ein Objekt in einer anderen Domäne oder Gesamtstruktur erfolgt, versucht die zugrunde liegende LDAP-API, die aktuellen Anmelde Informationen zum Binden an das Ziel der Referenz zu verwenden. Wenn dies erfolgreich ist, wird die Verweis Verfolgung transparent. Wenn dies nicht erfolgreich ist, werden der Verweis und der Verweis Fehlercode zurückgegeben.

Weitere Informationen zur Verwendung der Optionen für die Verweis Verfolgung mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Verweis Verfolgung mit idirector ysearch](referral-chasing-with-idirectorysearch.md)
-   [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 