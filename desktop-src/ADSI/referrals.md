---
title: Empfehlungen (ADSI)
description: Empfehlungen treten auf, wenn der Server, den Sie abfragen, diese Daten nicht enthält, sie aber finden kann.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- Empfehlungen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5fb6ad299c2f47efa9723857b53cf7eee5350589757153eaaae869b2c37e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444020"
---
# <a name="referrals-adsi"></a>Empfehlungen (ADSI)

Empfehlungen treten auf, wenn der Server, den Sie abfragen, diese Daten nicht enthält, sie aber finden kann. Der Zielserver gibt das Ergebnisset zurück, das sowohl die tatsächlichen Daten als auch eine Empfehlung an einen anderen Server enthalten kann, um die zusätzlichen Daten abzurufen. Durch Aktivieren der *Empfehlungsausführung* verwendet der zugrunde liegende ADSI-Clientcode diese Verweisdaten, um zu versuchen, das Zielobjekt von dem in den Verweisdaten beschriebenen Server abzurufen. Beachten Sie, dass die Deaktivierung der Verweisausweitung zu einem kleineren Ergebnisergebnis führen kann, während die Aktivierung der Verweisausweitung dazu führen kann, dass eine Abfrage viele Server umfasst. Die empfohlene Lösung ist nach Möglichkeit die Verwendung des globalen Katalogs.

Weitere Informationen zu Empfehlungen und Zur Referenzierung in Active Directory finden Sie unter [Empfehlungen](/windows/desktop/AD/referrals).

Wenn ein Client beispielsweise Server A (A) anweisen soll, ein Benutzerobjekt (U) abfragen zu lassen, kann A vorschlagen, dass der Client die Suche auf Server B (B) fortsetzen soll, wenn sich U nicht auf A befindet, aber bekannt ist, dass er sich auf B befindet. Der Client hat die Wahl, die Empfehlung zu erhalten oder nicht. Suchempfehlungen machen es für den Client nicht erforderlich, dass die Funktionen der einzelnen Server erweitert werden. Der Client muss jedoch den Typ der Empfehlungen angeben, die ein Server ausführen soll.

Active Directory bietet Suchempfehlungsdienste. Ein Client kann eine der folgenden Arten von Empfehlungssuchen auswählen:

-   Nie: Der Server sollte keine Empfehlung an einen Client generieren, obwohl er erkennt, dass die angeforderten Daten von einem anderen Server gespeichert werden.
-   Extern: Der Server sollte Empfehlungen generieren, wenn die Anforderung auf einem anderen Server einer anderen Verzeichnisstruktur aufgelöst werden kann. Beispielsweise fragt ein Client "OU=Sales,DC=Fabrikam,DC=COM" auf dem Server "fab01" in der Domäne "Fabrikam.com" ab. Das Objekt gehört jedoch nicht zu "fab01", aber es ist bekannt, dass es sich auf dem Server "arc01" in der Domäne "Fabrikam.com" befindet. Daher bezieht "fab01" den Client auf "arc01".
-   Untergeordneter Server: Der Server sollte Empfehlungen generieren, wenn die Anforderung auf einem Server aufgelöst werden kann, dessen Name einen zusammenhängenden Pfad vom Ursprungsserver bildet. Der Suchbereich muss auf der Unterstrukturebene sein.

    Beispielsweise enthält Server A Objekte in "DC=Sales,DC=Fabrikam,DC=Com". Server B enthält Objekte in "DC=Seattle,DC=Sales,DC=Fabrikam,DC=Com". Beachten Sie, dass der Name von Server B einen zusammenhängenden Pfad von Server A bildet. Wenn ein Client server A kontaktiert, eine Unterstruktursuche nach "DC=Sales,DC=Fabrikam,DC=Com" angibt und die Empfehlung als untergeordneten Typ angibt, tritt das folgende Ereignis auf:

    -   Server A gibt alle Objekte zurück, die ihm innerhalb seines Bereichs bekannt sind.
    -   Server A informiert den Client darüber, dass Objekte in "DC=Seattle,DC=Sales,DC=Fabrikam,DC=COM" auf Server B zu finden sind.

    Der Client kann server B kontaktieren. Wenn dies der Fall ist, tritt das folgende Ereignis auf:

    -   Server B antwortet mit den angeforderten Objekten.
    -   Wenn Server B andere Server im zusammenhängenden Namenspfad erkennt und der Prozess fortgesetzt wird.

-   Immer: Der Server generiert Empfehlungen, wenn die Suche basierend auf dem externen Typ oder dem untergeordneten Typ aufgelöst werden kann.

> [!Note]  
> In Active Directory enthält der globale Katalog alle Objekte in einem bestimmten Unternehmen. Das Durchsuchen eines globalen Katalogservers führt zu einer besseren Leistung als das Übertragen von Empfehlungen von einem Server zu einem anderen.

 

In den meisten Fällen ist die Weiterleitung von Empfehlungen für den Aufrufer transparent. Wenn die Empfehlung an ein Objekt in einer anderen Domäne oder Gesamtstruktur erfolgt, versucht die zugrunde liegende LDAP-API, die aktuellen Anmeldeinformationen zu verwenden, um eine Bindung an das Ziel der Empfehlung zu erstellen. Wenn dies erfolgreich ist, ist die Empfehlungserkung transparent. Wenn dies nicht erfolgreich ist, werden die Empfehlung und ein Empfehlungsfehlercode zurückgegeben.

Weitere Informationen zur Verwendung der Optionen für die Empfehlungssuche mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Empfehlungssuche mit IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Suchen mit ActiveX Datenobjekten](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 