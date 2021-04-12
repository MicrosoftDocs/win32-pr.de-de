---
title: Auswählen der Suchtechnologie
description: Dieses Thema enthält eine Liste der Technologien, die für die Suche nach Active Directory verwendet werden.
ms.assetid: c9e887e3-7de4-4461-bc32-03db71c3e272
ms.tgt_platform: multiple
keywords:
- Technologien in Active Directory suchen Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6edba5c87ed438bc0047e0381d7e366cd6cc865
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472668"
---
# <a name="choosing-the-search-technology"></a>Auswählen der Suchtechnologie

Die in der folgenden Tabelle aufgeführten Technologien können verwendet werden, um in Active Directory Domain Services zu suchen.



| Technologie                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1)<br/> | Die [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1) -Klasse wird vom [System. DirectoryServices](/dotnet/api/system.directoryservices?view=dotnet-plat-ext-3.1) -Namespace bereitgestellt, um das Suchen in Active Directory Domain Services mit .NET Framework zu ermöglichen. Weitere Informationen finden Sie unter durch [Suchen des Verzeichnisses](/previous-versions/ms180879(v=vs.90)).<br/>                                                                                                                                  |
| [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)<br/>                       | ADSI bietet die [**idirectoriysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstelle zum Abfragen eines Active Directory Servers sowie anderer Verzeichnisdienste wie NDS mithilfe von LDAP. **IDirectorySearch** ist eine COM-Schnittstelle, die zahlreiche typisierte Daten zurückgibt, wie z. b. ganze Zahlen, Oktett-Zeichen folgen, Zeichen folgen, Sicherheits Beschreibungen, UTC-Zeit, große ganze Zahl oder boolesche Werte. Weitere Informationen zur Verwendung von **idirector ysearch** finden Sie unter [Suchen mit der idirector ysearch-Schnittstelle](/windows/desktop/ADSI/searching-with-idirectorysearch).<br/> |
| OLE DB<br/>                                                              | OLE DB ist ein Satz von COM-Schnittstellen, die Anwendungen einen einheitlichen Zugriff auf Daten bereitstellen, die in verschiedenen Datenquellen gespeichert sind, unabhängig von Speicherort oder Typ. ADSI bietet auch einen OLE DB Anbieter für ADSI, mit dem Anwendungen OLE DB auf Active Directory Domain Services zugreifen können. Der ADSI OLE DB-Anbieter verwendet die [**idirector ysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstellen, um Abfragen an Active Directory Domain Services zu senden und die Ergebnisse zu erfassen.<br/>                                     |
| ADO und andere OLE DB basierte Datenzugriffs Technologien<br/>                 | Der ADSI-OLE DB-Anbieter ermöglicht die Suche nach Datenzugriffs Technologien, die auf OLE DB, z. b. ADO, basieren, in Active Directory Domain Services zu suchen.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| LDAP-API<br/>                                                            | Windows 2000-Domänen Controller sind Verzeichnisserver, die mit LDAP Version 3 kompatibel sind. Die LDAP-API ist eine Funktionsbibliothek im C-Stil. Anwendungen können die LDAP-API verwenden, um in Active Directory Domain Services zu suchen.<br/>                                                                                                                                                                                                                                                                              |



 

Beachten Sie bei der Auswahl einer Technologie Folgendes:

-   Für Microsoft Visual Basic und Visual Basic Scripting Edition (VBScript) wird ADO empfohlen.
-   Für C/C++ können Sie eine beliebige Technologie auswählen.
-   Wenn Ihre Anwendung häufig ADSI verwendet, ist es möglicherweise einfacher, [**idirector ysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)zu verwenden. Wenn Sie [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) verwenden, um Objekte in Active Directory Domain Services zu verwalten, verwenden Sie **IDirectorySearch** , um die Verarbeitung der von der Suche zurückgegebenen Eigenschaften zu vereinfachen. **IDirectorySearch** verwendet die gleichen [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) -Strukturen wie **IDirectoryObject** , um Eigenschaften darzustellen. Außerdem wird **idirector ysearch** für fast alle ADSI COM-Objekte verfügbar gemacht. Wenn Sie einen Zeiger auf ein ADSI-COM-Objekt haben, können Sie **QueryInterface** zum Abrufen eines **IDirectorySearch** -Zeigers verwenden, mit dem Sie eine Suche starten können, beginnend bei dem Verzeichnis Objekt, das durch das ADSI COM-Objekt dargestellt wird.
-   Wenn Ihre Anwendung bereits OLE DB-, ADO-oder LDAP-API verwendet, können Sie diese Technologien weiterhin verwenden, um innerhalb Active Directory Domain Services zu suchen.
-   Wenn Ihre Anwendung Daten aus einem Active Directory-Domäne-Dienst und einer SQL Server 7-Datenbank verknüpfen muss, verwenden Sie OLE DB. Wenn Sie OLE DB verwenden, kann Ihre Anwendung verteilte Abfragen ausführen, die auf Active Directory Domain Services und Tabellen und Rowsets aus einer oder mehreren Microsoft SQL Server 7-Datenbanken verweisen.

 

