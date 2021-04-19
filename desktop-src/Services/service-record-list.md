---
description: Wenn jeder Dienst Eintrag aus der Datenbank der installierten Dienste gelesen wird, erstellt der SCM einen Dienst Daten Satz für den Dienst.
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: Dienst Daten Satz Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1143625de977c7e5c488c5cc56620adc3a5454db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347771"
---
# <a name="service-record-list"></a>Dienst Daten Satz Liste

Wenn jeder Dienst Eintrag aus der Datenbank der installierten Dienste gelesen wird, erstellt der SCM einen Dienst Daten Satz für den Dienst. Ein Dienst Daten Satz umfasst Folgendes:

-   Dienstname
-   Starttyp (Auto-Start oder Demand-Start)
-   Dienststatus (siehe die [**Dienst \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Struktur) <dl> type  
    Aktueller Status  
    Akzeptable Kontrollcodes  
    Exitcode  
    Wait-Hinweis  
    </dl>
-   Pointer to dependency list

Der Benutzername und das Kennwort eines Kontos werden zu dem Zeitpunkt angegeben, zu dem der Dienst installiert ist. Der SCM speichert den Benutzernamen in der Registrierung und das Kennwort in einem sicheren Teil der lokalen Sicherheits Autorität (Local Security Authority, LSA). Der Systemadministrator kann Konten mit Kenn Wörtern erstellen, die nie ablaufen. Alternativ dazu kann der Systemadministrator Konten mit Kenn Wörtern erstellen, die die Konten ablaufen und verwalten, indem die Kenn Wörter regelmäßig geändert werden.

Der SCM speichert zwei Kopien des Kennworts eines Benutzerkontos, ein aktuelles Kennwort und ein Sicherungs Kennwort. Das Kennwort, das beim erstmaligen Installieren des Dienstanbieter angegeben wird, wird als Aktuelles Kennwort gespeichert, und das Sicherungs Kennwort ist nicht initialisiert. Wenn der SCM versucht, den Dienst im Sicherheitskontext des Benutzerkontos auszuführen, wird das aktuelle Kennwort verwendet. Wenn das aktuelle Kennwort erfolgreich verwendet wird, wird es auch als Sicherungs Kennwort gespeichert. Wenn das Kennwort mit der [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) -Funktion oder dem Dienstprogramm für die Systemsteuerung geändert wird, wird das neue Kennwort als Aktuelles Kennwort gespeichert, und das vorherige Kennwort wird als Sicherungs Kennwort gespeichert. Wenn der SCM versucht, den Dienst zu starten, und das aktuelle Kennwort fehlschlägt, wird das Sicherungs Kennwort verwendet. Wenn das Sicherungs Kennwort erfolgreich verwendet wird, wird es als Aktuelles Kennwort gespeichert.

Der SCM aktualisiert den Dienststatus, wenn ein Dienst IT-Status Benachrichtigungen mithilfe der Funktion [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) sendet. Der SCM verwaltet den Status eines Treiber Dienstanbieter, indem er das e/a-System abfragt, anstatt Status Benachrichtigungen zu erhalten, wie er von einem Dienst erfolgt.

Ein Dienst kann zusätzliche Typinformationen registrieren, indem er die [**setservicebits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) -Funktion aufruft. Die [**NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) -und [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) -Funktionen erhalten die unterstützten Dienst Typen.

 

 
