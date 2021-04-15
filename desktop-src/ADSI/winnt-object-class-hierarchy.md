---
title: WinNT-Objektklassen Hierarchie
description: Die Objektklassen Hierarchie von Winnt beginnt beim Namespace-Objekt.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- WinNT-Dienstanbieter ADSI, Objektklassen Hierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515452"
---
# <a name="winnt-object-class-hierarchy"></a>WinNT-Objektklassen Hierarchie

Die Objektklassen Hierarchie von Winnt beginnt beim Namespace-Objekt.



| Objektklasse                   | BESCHREIBUNG                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Namespace<br/>           | Objekt Container der obersten Ebene.<br/>                                            |
| Domain<br/>              | Die Windows NT-Domäne.<br/>                                                 |
| Benutzer<br/>                | Benutzerkonto.<br/>                                                          |
| Gruppieren<br/>               | Gruppenkonto zum Verwalten von Zugriffsrechten.<br/>                              |
| Usergroupcollection<br/> | Eine Gruppe von Benutzergruppen, die [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)implementieren.<br/>  |
| GroupCollection<br/>     | Ein Satz anderer Gruppen, die [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)implementieren.<br/> |
| Computer<br/>            | Windows NT 4,0-Server oder-Arbeitsstation.<br/>                                  |
| PrintJob<br/>            | Druckauftrag in der Druck Warteschlange.<br/>                                          |
| Printjobscollection<br/> | Ein Satz von Druckaufträgen.<br/>                                                   |
| PrintQueue<br/>          | Druck Warteschlange auf einem Druckerspooler.<br/>                                      |
| Dienst<br/>             | Anwendung, die als Dienst ausgeführt wird.<br/>                                      |
| File Service<br/>         | Dienste, die auf das Dateisystem zugreifen<br/>                                        |
| FileShare<br/>           | Der Dateifreigabe Punkt.<br/>                                                      |
| Resource<br/>            | Eine Ressource im Dienst.<br/>                                             |
| Sitzung<br/>             | Eine aktive Datei Dienst Verbindung.<br/>                                     |
| Benutzer<br/>                | Lokales Benutzerkonto.<br/>                                                    |
| Gruppieren<br/>               | Lokale Gruppe.<br/>                                                           |
| UserCollection<br/>      | Sammlung lokaler Benutzer.<br/>                                             |
| GroupCollection<br/>     | Sammlung lokaler Gruppen.<br/>                                            |
| Schema<br/>              | WinNT-Schema Container.<br/>                                                |
| Klasse<br/>               | Schema Klassendefinition.<br/>                                               |
| Eigenschaft<br/>            | Schema Attribut Definition.<br/>                                           |
| Syntax<br/>              | Syntax einer Eigenschaft.<br/>                                                  |



 

 

 





