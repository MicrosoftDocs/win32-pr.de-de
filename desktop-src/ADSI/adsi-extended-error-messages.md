---
title: Erweiterte ADSI-Fehlermeldungen
description: Dieses Thema enthält eine Liste der Themen, in denen erläutert wird, wie Sie mit den von IADs, IADsContainer, IDirectoryObject und IDirectorySearch zurückgegebenen ADSI-Fehlermeldungen arbeiten.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Erweiterte ADSI-Fehlermeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036329"
---
# <a name="adsi-extended-error-messages"></a>Erweiterte ADSI-Fehlermeldungen

Abgesehen von den **HRESULT** -Werten werden von mehreren ADSI-Systemanbietern (größtenteils LDAP) zusätzliche Fehler Daten für Vorgänge zurückgegeben, die von den folgenden Schnittstellen ausgeführt werden:

-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Ein Teil dieser erweiterten Fehler Daten ist die Zeichenfolge, die vom Server als Teil des Nachrichten Ergebnisses gesendet wird.

Rufen Sie [**adsgetlasterror**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) auf, um solche erweiterten Fehlermeldungen abzurufen. Der erste Parameter dieser Funktion, *lperror*, ist ein **DWORD** -Wert. Bei einem Active Directory Server versucht ADSI, eine LDAP-Fehlermeldung einem entsprechenden Win32-Fehlercode zuzuordnen, und weist den Win32-Fehler Codewert *lperror* zu. Wenn die Zuordnung nicht aufgelöst werden kann, weist ADSI *lperror* **fehlerhafte \_ \_ Daten** zu, wie es bei jedem anderen Verzeichnisserver der Fall ist. In allen Fällen leitet ADSI die Zeichenfolge der Fehlerbeschreibung über *lperrorbuf*, den zweiten Parameter der **adsgetlasterror** -Funktion, vom Server an den Client weiter.

 

 




