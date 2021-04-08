---
title: Wie ein Dienst seine SPNs verfasst hat
description: 'Ein Dienst kann zwei Funktionen verwenden, um seine SPNs zu verfassen: Es handelt sich um eine allgemeine Funktion zum Verfassen von SPNs, und DsServerRegisterSpn ist eine spezialisierte Funktion zum Verfassen und registrieren einfacher SPNs für einen Host basierten Dienst.'
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- Dienst Prinzipal Name AD, wie ein Dienst zusammensetzt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855428"
---
# <a name="how-a-service-composes-its-spns"></a>Wie ein Dienst seine SPNs verfasst hat

Ein Dienst kann seine SPNs mithilfe von zwei Funktionen zusammensetzen: [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) ist eine allgemeine Funktion zum Verfassen von SPNs, und [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) ist eine spezialisierte Funktion zum Erstellen und registrieren einfacher SPNs für einen Host basierten Dienst.

Ein Dienst Installationsprogramm verwendet in der Regel die [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) -Funktion zum Verfassen von SPNs, die dann mithilfe der [**dswrite-accountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) -Funktion für das Anmelde Konto des Diensts registriert werden. Der **dsgetspn** kann die folgenden Funktionen ausführen.

-   Erstellen Sie einen einfachen SPN mit dem <service class> / <host> Format "" für einen Host basierten Dienst.
-   Erstellen Sie einen komplexen Dienst Prinzipal Namen, der die &lt; Komponente "Dienst Name" enthält, die &gt; von replizierungsdiensten verwendet wird, oder die &lt; Komponente "Port &gt; ", die mehrere Instanzen eines Diensts auf einem einzelnen Host unterscheidet.
-   Erstellen Sie einen einzelnen SPN, wobei die " &lt; Host &gt; "-Komponente entweder auf den Namen eines angegebenen Hosts oder auf den Namen des lokalen Computers standardmäßig festgelegt ist.
-   Erstellen Sie ein Array von SPNs für mehrere Dienst Instanzen, die auf mehreren Hosts in der Gesamtstruktur ausgeführt werden. Jeder SPN gibt den Namen des Hosts für eine Dienst Instanz an.
-   Erstellen Sie ein Array von SPNs für mehrere Dienst Instanzen, die auf demselben Host ausgeführt werden. Jeder SPN gibt den Namen des Hosts und eine Portnummer für eine Dienst Instanz an.

Das von [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) zurückgegebene Array von Namen muss durch Aufrufen der [**dsfreespnarray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) -Funktion freigegeben werden.

Beachten Sie, dass die Funktionen [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**dswrite teaccountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)und [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) nicht überprüfen, ob die SPNs eindeutig sind. Da die gegenseitige Authentifizierung fehlschlägt, wenn ein Client einen nicht eindeutigen SPN anzeigt, überprüfen Sie die Eindeutigkeit, bevor Sie einen SPN registrieren. Zu diesem Zweck Durchsuchen Sie den globalen Katalog (GC) nach **servicePrincipalName** -Attributen, die dem SPN entsprechen. Weitere Informationen zum Durchsuchen des GC finden Sie unter durch [Suchen des globalen Katalogs](searching-global-catalog-contents.md).

 

 




