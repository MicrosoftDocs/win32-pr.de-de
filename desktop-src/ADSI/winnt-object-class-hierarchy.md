---
title: WinNT-Objektklassenhierarchie
description: Die WinNT-Objektklassenhierarchie beginnt mit dem Namespace-Objekt.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- WinNT-Dienstanbieter ADSI, Objektklassenhierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e893839393ad3b9aaa42557d90f9bf279ab0625e1225ab41f2d1a3c7e7980a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589760"
---
# <a name="winnt-object-class-hierarchy"></a>WinNT-Objektklassenhierarchie

Die WinNT-Objektklassenhierarchie beginnt mit dem Namespace-Objekt.



| Objektklasse                   | BESCHREIBUNG                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Namespace<br/>           | Objektcontainer der obersten Ebene.<br/>                                            |
| Domäne<br/>              | Die Windows NT-Domäne.<br/>                                                 |
| User<br/>                | Benutzerkonto.<br/>                                                          |
| Group<br/>               | Gruppenkonto für die Verwaltung von Zugriffsrechten.<br/>                              |
| UserGroupCollection<br/> | Eine Gruppe von Benutzergruppen, die [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)implementieren.<br/>  |
| Groupcollection<br/>     | Eine Gruppe anderer Gruppen, die [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)implementieren.<br/> |
| Computer<br/>            | Windows NT 4.0-Server oder -Arbeitsstation.<br/>                                  |
| Printjob<br/>            | Druckauftrag in der Druckwarteschlange.<br/>                                          |
| PrintJobsCollection<br/> | Eine Gruppe von Druckaufträgen.<br/>                                                   |
| PrintQueue<br/>          | Druckwarteschlange in einem Druckerspooler.<br/>                                      |
| Service<br/>             | Anwendung, die als Dienst ausgeführt wird.<br/>                                      |
| FileService<br/>         | Dienste, die auf das Dateisystem zugreifen.<br/>                                        |
| FileShare<br/>           | Dateifreigabepunkt.<br/>                                                      |
| Ressource<br/>            | Eine Ressource im Dienst.<br/>                                             |
| Sitzung<br/>             | Eine aktive Dateidienstverbindung.<br/>                                     |
| User<br/>                | Lokales Benutzerkonto.<br/>                                                    |
| Group<br/>               | Lokale Gruppe.<br/>                                                           |
| UserCollection<br/>      | Sammlung lokaler Benutzer.<br/>                                             |
| Groupcollection<br/>     | Sammlung lokaler Gruppen.<br/>                                            |
| Schema<br/>              | WinNT-Schemacontainer.<br/>                                                |
| Klasse<br/>               | Schemaklassendefinition.<br/>                                               |
| Eigenschaft<br/>            | Schemaattributdefinition.<br/>                                           |
| Syntax<br/>              | Syntax einer Eigenschaft.<br/>                                                  |



 

 

 





