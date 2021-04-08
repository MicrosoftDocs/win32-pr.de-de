---
title: Registrieren der SPNs durch einen Dienst
description: Bevor ein Client einen SPN zum Authentifizieren einer Instanz eines Dienstanbieter verwenden kann, muss der SPN für das Benutzer-oder Computer Konto registriert werden, das von der Dienst Instanz für die Anmeldung verwendet wird.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- Registrieren des SPNs AD durch einen Dienst
- Dienst Prinzipal Name AD, wie ein Dienst seine SPNs registriert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74410be3a024fc6accd1d8394e2ba8335be9f550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855427"
---
# <a name="how-a-service-registers-its-spns"></a>Registrieren der SPNs durch einen Dienst

Bevor ein Client einen SPN zum Authentifizieren einer Instanz eines Dienstanbieter verwenden kann, muss der SPN für das Benutzer-oder Computer Konto registriert werden, das von der Dienst Instanz für die Anmeldung verwendet wird. In der Regel wird die SPN-Registrierung von einem Dienst Installationsprogramm ausgeführt, das mit Domänen Administratorrechten ausgeführt wird.

Das Dienst Installationsprogramm, das eine Dienst Instanz auf einem Host Computer installiert, führt normalerweise das folgende Verfahren aus.

**So registrieren Sie SPNs für eine Dienst Instanz**

1.  Rufen Sie die [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) -Funktion auf, um einen oder mehrere eindeutige SPNs für die Dienst Instanz zu erstellen. Weitere Informationen finden Sie unter [namens Formate für eindeutige SPNs](name-formats-for-unique-spns.md).
2.  Wenden Sie die [**dsschreiteaccountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) -Funktion an, um die Namen für das Anmelde Konto des Diensts zu registrieren.

[**Dswrite teaccountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registriert SPNs als Eigenschaft eines Benutzer-oder Computer Konto Objekts im Verzeichnis. **Benutzer** -und **Computer** Objekte verfügen über ein **servicePrincipalName** -Attribut, bei dem es sich um ein mehr wertiges Attribut zum Speichern aller SPNs handelt, die einem Benutzer-oder Computer Konto zugeordnet sind. Wenn der Dienst unter einem Benutzerkonto ausgeführt wird, werden die SPNs im **servicePrincipalName** -Attribut dieses Kontos gespeichert. Wenn der Dienst im Konto "LocalSystem" ausgeführt wird, werden die SPNs im **servicePrincipalName** -Attribut des Kontos auf dem Host Computer des Diensts gespeichert. Der **dswrite-accountspn** -Aufrufer muss den Distinguished Name des Konto Objekts angeben, unter dem die SPNs gespeichert werden.

Um sicherzustellen, dass registrierte SPNs sicher sind, kann das **servicePrincipalName** -Attribut nicht direkt geschrieben werden. Sie kann nur durch Aufrufen von [**dswrite-accountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)geschrieben werden. Der Aufrufer muss über Schreibzugriff auf das **servicePrincipalName** -Attribut des Zielkontos verfügen. In der Regel wird Schreibzugriff standardmäßig nur für Domänen Administratoren erteilt. Es gibt jedoch einen Sonderfall, bei dem ein Dienst, der unter dem Konto "LocalSystem" ausgeführt wird, seine eigenen SPNs auf dem Computer Konto des Dienst Hosts registrieren kann. In diesem Fall muss der SPN, der geschrieben wird, das Format "" aufweisen, <service class> / <host> und " &lt; Host &gt; " muss der DNS-Name des lokalen Computers sein.

[**Dsbeschreib teaccountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) kann auch SPNs von einem Konto entfernen. Ein Vorgangs Parameter gibt an, ob die SPNs dem Konto hinzugefügt, aus dem Konto entfernt oder verwendet werden, um alle aktuellen SPNs für das Konto vollständig zu ersetzen. Wenn eine Dienst Instanz deinstalliert wird, entfernen Sie alle für diese Instanz registrierten SPNs.

Weitere Informationen und ein Codebeispiel, in dem die SPNs eines dienstanders registriert oder aufgehoben werden, finden Sie unter [Registrieren der SPNs für einen Dienst](registering-the-spns-for-a-service.md).

Host basierte Dienste, die das einfache SPN-Format " <service class> / <host> " verwenden, haben die Möglichkeit, die [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) -Funktion zu verwenden, die für eine Dienst Instanz SPNs erstellt und registriert. **DsServerRegisterSpn** ist eine Hilfsfunktion, die [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) und [**dsschreiteaccountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)aufruft.

Weitere Informationen finden Sie unter [Dienst Anmeldekonten](service-logon-accounts.md).

 

 




