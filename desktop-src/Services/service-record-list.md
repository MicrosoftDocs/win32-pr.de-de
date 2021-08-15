---
description: Wenn jeder Diensteintrag aus der Datenbank der installierten Dienste gelesen wird, erstellt der SCM einen Dienstdatensatz für den Dienst.
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: Dienstdatensatzliste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef0bdebed5e302b1dc59bea6494fd812ec506e7e6d2531634b2a6686b86bc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888854"
---
# <a name="service-record-list"></a>Dienstdatensatzliste

Wenn jeder Diensteintrag aus der Datenbank der installierten Dienste gelesen wird, erstellt der SCM einen Dienstdatensatz für den Dienst. Ein Dienstdatensatz enthält Folgendes:

-   Dienstname
-   Starttyp (auto-start oder demand-start)
-   Dienststatus (siehe SERVICE [**\_ STATUS-Struktur)**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) <dl> type  
    Aktueller Status  
    Zulässige Steuerungscodes  
    Exitcode  
    Wartehinweis  
    </dl>
-   Pointer to dependency list

Der Benutzername und das Kennwort eines Kontos werden zum Zeitpunkt der Installation des Diensts angegeben. Der SCM speichert den Benutzernamen in der Registrierung und das Kennwort in einem sicheren Teil der lokalen Sicherheitsstelle (Local Security Authority, LSA). Der Systemadministrator kann Konten mit Kennwörtern erstellen, die nie ablaufen. Alternativ kann der Systemadministrator Konten mit abgelaufenen Kennwörtern erstellen und die Konten verwalten, indem er die Kennwörter in regelmäßigen Abständen ändert.

Der SCM speichert zwei Kopien des Kennworts eines Benutzerkontos, ein aktuelles Kennwort und ein Sicherungskennwort. Das kennwort, das bei der ersten Installation des Diensts angegeben wurde, wird als aktuelles Kennwort gespeichert, und das Sicherungskennwort wird nicht initialisiert. Wenn der SCM versucht, den Dienst im Sicherheitskontext des Benutzerkontos ausführen zu können, verwendet er das aktuelle Kennwort. Wenn das aktuelle Kennwort erfolgreich verwendet wird, wird es auch als Sicherungskennwort gespeichert. Wenn das Kennwort mit der [**ChangeServiceConfig-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) oder dem Systemsteuerungs-Hilfsprogramm Dienste geändert wird, wird das neue Kennwort als aktuelles Kennwort und das vorherige Kennwort als Sicherungskennwort gespeichert. Wenn der SCM versucht, den Dienst zu starten, und das aktuelle Kennwort fehlschlägt, verwendet es das Sicherungskennwort. Wenn das Sicherungskennwort erfolgreich verwendet wird, wird es als aktuelles Kennwort gespeichert.

Der SCM aktualisiert den Dienststatus, wenn er von einem Dienst mithilfe der [**SetServiceStatus-Funktion Statusbenachrichtigungen gesendet**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) wird. Der SCM behält den Status eines Treiberdiensts bei, indem er das E/A-System abfragt, anstatt Statusbenachrichtigungen zu empfangen, wie es bei einem Dienst der Dert ist.

Ein Dienst kann zusätzliche Typinformationen registrieren, indem er die [**SetServiceBits-Funktion**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) aufruft. Die [**Funktionen NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) und [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) erhalten die unterstützten Diensttypen.

 

 
