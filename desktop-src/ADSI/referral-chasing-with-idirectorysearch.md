---
title: Empfehlungssuche mit IDirectorySearch
description: Eine Empfehlung ist der Mechanismus, mit dem ein Verzeichnisserver einen Client an einen anderen Server weiter leitet, wenn er nicht genügend Daten über das von einer Abfrage angeforderte Objekt enthält.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Empfehlungssuche mit IDirectorySearch ADSI
- ADSI, Search, IDirectorySearch, Other Search Options, Referral Chasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7fcc74103c5c09816976e9ff91c17ecca8578fcbf596b731df890a350e922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690689"
---
# <a name="referral-chasing-with-idirectorysearch"></a>Empfehlungssuche mit IDirectorySearch

Eine Empfehlung ist der Mechanismus, mit dem ein Verzeichnisserver einen Client an einen anderen Server weiter leitet, wenn er nicht genügend Daten über das von einer Abfrage angeforderte Objekt enthält.

Bei einer Suche auf einer Ebene oder unterstruktur werden Empfehlungen nur für bekannte, unmittelbar untergeordnete Domänen-, Schema- oder Konfigurationscontainer zurückgegeben. das heißt, untergeordnete Domänen, die direkte Nachfolger sind. Weitere Informationen finden Sie unter [Suchbereich](/windows/desktop/AD/search-scope).

In einem Verzeichnis sind nicht alle Daten auf einem einzelnen Server verfügbar, sondern über mehrere verschiedene Server im Netzwerk verteilt. Wenn die Server die Daten gemeinsam verwenden, die andere Server bereitstellen können, können sie Empfehlungen an einen Client senden, wenn eine angeforderte Abfrage auf dem Ursprungsserver nicht aufgelöst werden kann. Wenn ein Client z. B. Server A zur Abfrage eines Benutzerobjekts (U) bittet, kann A vorschlagen, dass der Client die Suche auf Server B fortsetzen soll, wenn sich U nicht auf A befindet, sondern sich auf B befindet. Der Client hat die Wahl, die Empfehlung zu verfolgen oder nicht. Empfehlungen geben an, dass der Client keine vorherigen Kenntnisse über die Funktionen der einzelnen Server besitzen muss, aber der Client muss den Typ der Empfehlungen angeben, die ein Server ausführen soll.

Um die Empfehlungssuche zu aktivieren oder zu deaktivieren, legen Sie eine **SUCHoption ADS \_ SEARCHPREF \_ CHEAT \_ REFERRALS** mit einem **ADSTYPE \_ INTEGER-Wert** fest, der einen der [**ADS ADS ADS \_ \_ REFERRALS \_ ENUM-Enumerationswerte**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält, der an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird.

Das folgende Codebeispiel zeigt, wie Sie Empfehlungsverweise aktivieren.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Weitere Informationen zu Empfehlungen in Active Directory finden Sie unter [Empfehlungen.](/windows/desktop/AD/referrals)

 

 