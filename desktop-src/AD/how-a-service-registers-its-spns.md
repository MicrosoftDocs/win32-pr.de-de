---
title: Registrieren von SPNs durch einen Dienst
description: Bevor ein Client einen SPN zum Authentifizieren einer Instanz eines Diensts verwenden kann, muss der SPN für das Benutzer- oder Computerkonto registriert werden, das von der Dienstinstanz für die Anmeldung verwendet wird.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- So registriert ein Dienst seine SPNs AD
- Dienstprinzipalname AD , wie ein Dienst seine SPNs registriert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ebf33ed0f28dff3acffdcdc96a880c21ec532ff677801dd52ac1801f44c80e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188583"
---
# <a name="how-a-service-registers-its-spns"></a>Registrieren von SPNs durch einen Dienst

Bevor ein Client einen SPN zum Authentifizieren einer Instanz eines Diensts verwenden kann, muss der SPN für das Benutzer- oder Computerkonto registriert werden, das von der Dienstinstanz für die Anmeldung verwendet wird. In der Regel erfolgt die SPN-Registrierung durch ein Dienstinstallationsprogramm, das mit Domänenadministratorrechten ausgeführt wird.

Das Dienstinstallationsprogramm, das eine Dienstinstanz auf einem Hostcomputer installiert, führt in der Regel das folgende Verfahren aus.

**So registrieren Sie SPNs für eine Dienstinstanz**

1.  Rufen Sie die [**DsGetSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) auf, um einen oder mehrere eindeutige SPNs für die Dienstinstanz zu erstellen. Weitere Informationen finden Sie unter [Namensformate für eindeutige SPNs.](name-formats-for-unique-spns.md)
2.  Rufen Sie die [**DsWriteAccountSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) auf, um die Namen für das Anmeldekonto des Diensts zu registrieren.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registriert SPNs als Eigenschaft eines Benutzer- oder Computerkontoobjekts im Verzeichnis. **Benutzer-** und **Computerobjekte** verfügen über ein **servicePrincipalName-Attribut,** bei dem es sich um ein mehrwertiges Attribut zum Speichern aller SPNs handelt, die einem Benutzer- oder Computerkonto zugeordnet sind. Wenn der Dienst unter einem Benutzerkonto ausgeführt wird, werden die SPNs im **servicePrincipalName-Attribut** dieses Kontos gespeichert. Wenn der Dienst im LocalSystem-Konto ausgeführt wird, werden die SPNs im **servicePrincipalName-Attribut** des Kontos des Hostcomputers des Diensts gespeichert. Der **DsWriteAccountSpn-Aufrufer** muss den Distinguished Name des Kontoobjekts angeben, unter dem die SPNs gespeichert werden.

Um sicherzustellen, dass registrierte SPNs sicher sind, kann das **servicePrincipalName-Attribut** nicht direkt geschrieben werden. sie kann nur durch Aufrufen von [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)geschrieben werden. Der Aufrufer muss über Schreibzugriff auf das **servicePrincipalName-Attribut** des Zielkontos verfügen. In der Regel wird schreibzugriff standardmäßig nur Domänenadministratoren gewährt. Es gibt jedoch einen Sonderfall, in dem das System einem Dienst, der unter dem LocalSystem-Konto ausgeführt wird, erlaubt, seine eigenen SPNs auf dem Computerkonto des Diensthosts zu registrieren. In diesem Fall muss der geschriebene SPN das Format <service class> / <host> " " und " &lt; Host " &gt; den DNS-Namen des lokalen Computers aufweisen.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) kann auch SPNs aus einem Konto entfernen. Ein Vorgangsparameter gibt an, ob die SPNs dem Konto hinzugefügt, aus dem Konto entfernt oder verwendet werden sollen, um alle aktuellen SPNs für das Konto vollständig zu ersetzen. Wenn eine Dienstinstanz deinstalliert wird, entfernen Sie alle für diese Instanz registrierten SPNs.

Weitere Informationen und ein Codebeispiel zum Registrieren oder Aufheben der Registrierung der SPNs eines Diensts finden Sie unter [Registrieren der SPNs für einen Dienst.](registering-the-spns-for-a-service.md)

Hostbasierte Dienste, die das einfache SPN-Format "" <service class> / <host> verwenden, haben die Möglichkeit, die [**DsServerRegisterSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) zu verwenden, die SPNs für eine Dienstinstanz erstellt und registriert. **DsServerRegisterSpn** ist eine Hilfsfunktion, die [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) und [**DsWriteAccountSpn aufruft.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)

Weitere Informationen finden Sie unter [Dienstanmeldungskonten.](service-logon-accounts.md)

 

 




