---
title: Verweis Verfolgung mit idirector ysearch
description: Ein Verweis ist der Mechanismus, der von einem Verzeichnisserver verwendet wird, um einen Client an einen anderen Server weiterzuleiten, wenn er keine ausreichenden Daten über das von einer Abfrage angeforderte Objekt enthält.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Verweis Verfolgung mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Verweis Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949113"
---
# <a name="referral-chasing-with-idirectorysearch"></a>Verweis Verfolgung mit idirector ysearch

Ein Verweis ist der Mechanismus, der von einem Verzeichnisserver verwendet wird, um einen Client an einen anderen Server weiterzuleiten, wenn er keine ausreichenden Daten über das von einer Abfrage angeforderte Objekt enthält.

Bei einer Suche in einer Ebene oder einer Unterstruktur werden Verweise nur für bekannte, unmittelbar untergeordnete Domänen-, Schema-oder Konfigurations Container zurückgegeben. Dies sind untergeordnete Domänen, die direkte Nachfolger sind. Weitere Informationen finden Sie unter [Suchbereich](/windows/desktop/AD/search-scope).

In einem Verzeichnis sind nicht alle Daten auf einem einzelnen Server verfügbar, sondern auf mehrere verschiedene Server über das Netzwerk verteilt. Wenn die Server die Daten gemeinsam nutzen, die andere Server bereitstellen können, können Sie Verweise auf einen Client bereitstellen, wenn eine angeforderte Abfrage nicht auf dem ursprünglichen Server aufgelöst werden kann. Wenn ein Client z. b. Server a auffordert, ein Benutzerobjekt (u) abzufragen, kann eine die Suche auf Server B fortsetzen, wenn sich U nicht in einer befindet, aber als auf B festgelegt ist. Der Client hat die Möglichkeit, den Verweis nachzuverfolgen. Verweise geben an, dass der Client über vorherige Kenntnisse der Funktion der einzelnen Server verfügen muss, aber der Client muss den Typ der Verweise angeben, die ein Server ausführen sollte.

Legen Sie zum Aktivieren oder Deaktivieren der Verweis Verfolgung eine Suchoption für **ADS \_ searchpref \_ Chase \_ Referrals** mit einem **\_ ganzzahligen adstype** -Wert fest, der einen der ADS-enumerationsenumerationswerte für Enumerationswerte im ADS-enumerationsarray enthält, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode weitergegeben wird. [**\_ \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) [**\_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)

Im folgenden Codebeispiel wird gezeigt, wie Sie Chase-Verweise aktivieren.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Weitere Informationen zu verweisen in Active Directory finden Sie unter [Verweise](/windows/desktop/AD/referrals).

 

 