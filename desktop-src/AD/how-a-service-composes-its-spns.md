---
title: So erstellt ein Dienst seine SPNs
description: Ein Dienst kann zwei Funktionen verwenden, um seine SPNs zu erstellen. DsGetSpn ist eine allgemeine Funktion zum Zusammenstellen von SPNs, und DsServerRegisterSpn ist eine spezielle Funktion zum Erstellen und Registrieren einfacher SPNs für einen hostbasierten Dienst.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- Dienstprinzipalname AD , wie ein Dienst erstellt wird
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd4c0ac9c871c76e9e8771a688d203898674e477426ebd788ee34fe894011a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188644"
---
# <a name="how-a-service-composes-its-spns"></a>So erstellt ein Dienst seine SPNs

Ein Dienst kann zwei Funktionen verwenden, um seine SPNs zu erstellen: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) ist eine allgemeine Funktion zum Zusammenstellen von SPNs, und [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) ist eine spezielle Funktion zum Erstellen und Registrieren einfacher SPNs für einen hostbasierten Dienst.

Ein Dienstinstallationsprogramm verwendet in der Regel die [**DsGetSpn-Funktion,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) um SPNs zu erstellen, die dann mithilfe der [**DsWriteAccountSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) für das Anmeldekonto des Diensts registriert werden. **DsGetSpn** kann die folgenden Funktionen ausführen.

-   Erstellen Sie einen einfachen SPN mit dem <service class> / <host> Format "" für einen hostbasierten Dienst.
-   Erstellen Sie einen komplexen SPN, der die &lt; Komponente "Dienstname" enthält, die von &gt; replizierbaren Diensten verwendet wird, oder die &lt; &gt; "port"-Komponente, die mehrere Instanzen eines Diensts auf einem einzelnen Host unterscheidet.
-   Erstellen Sie einen einzelnen SPN, wobei die &lt; &gt; Komponente "host" entweder auf den Namen eines angegebenen Hosts oder standardmäßig auf den Namen des lokalen Computers festgelegt ist.
-   Erstellen Sie ein Array von SPNs für mehrere Dienstinstanzen, die auf mehreren Hosts in der gesamtstruktur ausgeführt werden. Jeder SPN gibt den Namen des Hosts für eine Dienstinstanz an.
-   Erstellen Sie ein Array von SPNs für mehrere Dienstinstanzen, die auf demselben Host ausgeführt werden. Jeder SPN gibt den Namen des Hosts und eine Portnummer für eine Dienstinstanz an.

Das von [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) zurückgegebene Array von Namen muss durch Aufrufen der [**DsFreeSpnArray-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) freigegeben werden.

Beachten Sie, dass die Funktionen [**DsGetSpn,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)und [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) nicht überprüfen, ob SPNs eindeutig sind. Da bei der gegenseitigen Authentifizierung ein Fehler auftritt, wenn ein Client einen nicht eindeutigen SPN vorlegt, überprüfen Sie die Eindeutigkeit, bevor Sie einen SPN registrieren. Durchsuchen Sie hierzu den globalen Katalog (GC) nach **servicePrincipalName-Attributen,** die Ihrem SPN entsprechen. Weitere Informationen zum Durchsuchen der GC finden Sie unter [Durchsuchen des globalen Katalogs.](searching-global-catalog-contents.md)

 

 




