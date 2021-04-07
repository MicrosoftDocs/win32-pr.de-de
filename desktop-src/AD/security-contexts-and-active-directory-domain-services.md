---
title: Sicherheits Kontexte und Active Directory Domain Services
description: Wenn eine Anwendung an einen Active Directory-Domäne Controller (DC) gebunden wird, wird dies im Sicherheitskontext eines Sicherheits Prinzipals durchführt, bei dem es sich um einen Benutzer oder eine Entität (z. b. einen Computer oder einen Systemdienst) handeln kann.
ms.assetid: 7ad0acbe-f81b-46d6-be87-3526b0bfbd1b
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, Sicherheits Kontexte
- Sicherheits Kontexte Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337cb05f8158dbb90f231652c42fb10a486aef4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038732"
---
# <a name="security-contexts-and-active-directory-domain-services"></a>Sicherheits Kontexte und Active Directory Domain Services

Wenn eine Anwendung an einen Active Directory-Domäne Controller (DC) gebunden wird, wird dies im Sicherheitskontext eines Sicherheits Prinzipals durchführt, bei dem es sich um einen Benutzer oder eine Entität (z. b. einen Computer oder einen Systemdienst) handeln kann. Der Sicherheitskontext ist das Benutzerkonto, das vom System zum Erzwingen der Sicherheit verwendet wird, wenn ein Thread versucht, auf ein Sicherungs fähiges Objekt zuzugreifen. Diese Daten umfassen die Benutzer Sicherheits-ID (SID), Gruppenmitgliedschaften und Berechtigungen.

Ein Benutzer legt einen Sicherheitskontext fest, indem Anmelde Informationen für die Authentifizierung vorgelegt werden. Wenn die Anmelde Informationen authentifiziert werden, erstellt das System ein Zugriffs Token, das die Gruppenmitgliedschaften und Berechtigungen identifiziert, die dem Benutzerkonto zugeordnet sind. Das System überprüft das Zugriffs Token, wenn Sie versuchen, auf ein Verzeichnis Objekt zuzugreifen. Sie vergleicht die Daten in Ihrem Zugriffs Token mit den Konten und Gruppen, denen der Zugriff durch die Objekt Sicherheits Beschreibung erteilt oder verweigert wird.

Verwenden Sie die folgenden Methoden, um den Sicherheitskontext zu steuern, mit dem Sie eine Bindung an einen Active Directory DC herstellen:

-   Binden Sie mithilfe der **AD \_ Secure \_ Authentication** -Option mit der [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) -Funktion oder der [**iadsopendsobject:: opendsobject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) -Methode, und geben Sie explizit einen Benutzernamen und ein Kennwort an. Diese Anmelde Informationen werden vom System authentifiziert, und es wird ein Zugriffs Token generiert, das für die Dauer der Bindung für die Zugriffs Überprüfung verwendet wird. Weitere Informationen finden Sie unter [Authentifizierung](authentication.md).
-   Binden Sie mithilfe **der \_ sicheren \_ Authentifizierungs Option ADS** , aber ohne Angabe von Anmelde Informationen. Wenn Sie keine Identität eines Benutzers annehmen, verwendet das System den primären Sicherheitskontext Ihrer Anwendung, d. h. den Sicherheitskontext des Benutzers, der die Anwendung gestartet hat. Bei einem Systemdienst handelt es sich hierbei um den Sicherheitskontext des Dienst Kontos oder des Kontos LocalSystem.
-   Nimmt die Identität eines Benutzers an und bindet dann die **\_ sichere \_ Authentifizierung mit ADS** ein, ohne Anmelde Informationen anzugeben. In diesem Fall verwendet das System den Sicherheitskontext des Clients, dessen Identität angenommen wird. Weitere Informationen finden Sie unter [Client](/windows/desktop/SecAuthZ/client-impersonation)Identitätswechsel.
-   Binden Sie mithilfe von [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) oder [**iadsopendsobject:: opendsobject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) mit der Option **ADS \_ No \_ Authentication** . Diese Methode bindet ohne Authentifizierung und führt zu "jeder" als Sicherheitskontext. Diese Option wird nur vom LDAP-Anbieter unterstützt.

Binden Sie, wenn möglich, ohne Angabe von Anmelde Informationen. Das heißt, verwenden Sie den Sicherheitskontext des angemeldeten Benutzers oder des Clients, dessen Identität angenommen wurde. Dadurch können Sie das Zwischenspeichern von Anmelde Informationen vermeiden. Wenn Sie alternative Benutzer Anmelde Informationen verwenden müssen, fordern Sie die Anmelde Informationen an, binden Sie Sie ein, aber nicht zwischenspeichern. Wenn Sie in mehreren Bindungs Vorgängen denselben Sicherheitskontext verwenden möchten, können Sie den Benutzernamen und das Kennwort für den ersten Bindungs Vorgang angeben und dann nur den Benutzernamen angeben, um nachfolgende Bindungen zu erstellen. Weitere Informationen zur Verwendung dieser Technik finden Sie unter [Authentifizierung](authentication.md).

Einige Sicherheits Kontexte sind leistungsfähiger als andere. Beispielsweise hat das LocalSystem-Konto auf einem Domänen Controller vollen Zugriff auf Active Directory Domain Services, wohingegen ein typischer Benutzer nur begrenzten Zugriff auf einige der Objekte im Verzeichnis hat. Im Allgemeinen sollte die Anwendung nicht in einem leistungsfähigen Sicherheitskontext wie "LocalSystem" ausgeführt werden, wenn ein weniger leistungsfähiger Sicherheitskontext für die Ausführung der Vorgänge ausreicht. Dies bedeutet, dass Sie die Anwendung in separate Komponenten aufteilen möchten, die jeweils in einem Sicherheitskontext ausgeführt werden, der für die auszuführenden Vorgänge geeignet ist. Beispielsweise kann das Setup der Anwendung wie folgt aufgeteilt werden:

-   Ausführen von Schema Änderungen und Erweiterungen im Kontext eines Benutzers, der Mitglied der Gruppe "Schema Administratoren" ist.
-   Führen Sie Konfigurations Container Änderungen im Kontext eines Benutzers durch, der Mitglied der Gruppe "Unternehmens Administratoren" ist.
-   Ausführen von Domänen Container Änderungen im Kontext eines Benutzers, der Mitglied der Gruppe "Domänen Administratoren" ist.

 

 