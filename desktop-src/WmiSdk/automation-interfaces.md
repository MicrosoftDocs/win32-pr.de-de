---
description: Stellt die Schnittstellen der Skript-API für WMI für C/C++-Programmierer anstelle der com-API-Versionen zur Verfügung.
ms.assetid: 18f6cc70-9df1-4d43-a2e0-af03e2f9e2c5
ms.tgt_platform: multiple
title: Automatisierungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652e9a1fb35a66bddb9f0aebe543770e89e6e2ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350045"
---
# <a name="automation-interfaces"></a>Automatisierungs Schnittstellen

Die Automation-API stellt die Schnittstellen der Skript-API für WMI für C/C++-Programmierer anstelle der com-API-Versionen zur Verfügung.

In der folgenden Tabelle sind WMI-Objekte und deren Verwendung in der Automation-API aufgelistet. Die Querverweise sind mit der Schnittstellendokumentation für die Skript-API für WMI-Entsprechungen verknüpft.



| Automatisierungs Objekt                                 | BESCHREIBUNG                                                                                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**Iswbemeventsource**](swbemeventsource.md)     | Ruft Ereignisse in Verbindung mit [**ISWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md)ab.   |
| [**Iswbemlasterror**](swbemlasterror.md)         | Stellt erweiterte Fehlerinformationen bereit, wenn ein Fehler auftritt.                                                                   |
| [**Iswbemlocator**](swbemlocator.md)             | Ruft einen Verweis auf ein [**iswbemservices**](swbemservices.md) -Objekt ab, das auf WMI auf einem bestimmten Host Computer zugreifen kann. |
| [**Iswbemmethod**](swbemmethod.md)               | Enthält eine einzelne Methoden Definition.                                                                                        |
| [**Iswbemmethodset**](swbemmethodset.md)         | Ruft den Zugriff auf eine Auflistung von [**iswbemmethod**](swbemmethod.md) -Objekten ab.                                                 |
| [**Iswbemnamedvalue**](swbemnamedvalue.md)       | Enthält einen einzelnen benannten Wert.                                                                                              |
| [**Iswbemnamedvalueset**](swbemnamedvalueset.md) | Ruft den Zugriff auf eine Auflistung von [**iswbemnamedvalue**](swbemnamedvalue.md) -Objekten ab.                                         |
| [**Iswbemubjekt**](swbemobject.md)               | Enthält und manipuliert eine einzelne Common Information Model (CIM)-Objektklasse oder-Instanz.                                  |
| [**Iswbemubjectpath**](swbemobjectpath.md)       | Generiert und überprüft einen Objekt Pfad.                                                                                     |
| [**Iswbemubjectset**](swbemobjectset.md)         | Ruft den Zugriff auf eine Auflistung von [**iswbemubject**](swbemobject.md) -Objekten ab.                                                 |
| [**Iswbemprivilege**](swbemprivilege.md)         | Legt eine Berechtigung fest oder löscht sie.                                                                                                 |
| [**Iswbemprivilegeset**](swbemprivilegeset.md)   | Ruft den Zugriff auf eine Auflistung von [**iswbemprivilege**](swbemprivilege.md) -Objekten ab.                                           |
| [**Iswbemproperty**](swbemproperty.md)           | Wird verwendet, um eine einzelne CIM-Eigenschaft zu enthalten.                                                                                      |
| [**Iswbempropertyset**](swbempropertyset.md)     | Abrufen des Zugriffs auf eine Sammlung von [**iswbemproperty**](swbemproperty.md) -Objekten.                                              |
| [**Iswbemqualifizierer**](swbemqualifier.md)         | Enthält einen einzelnen Klassen Qualifizierer.                                                                                          |
| [**Iswbemqualifierset**](swbemqualifierset.md)   | Ruft den Zugriff auf eine Auflistung von [**iswbemqualifier**](swbemqualifier.md) -Objekten ab.                                           |
| [**Iswbemsecurity**](swbemsecurity.md)           | Verwaltet Sicherheitseinstellungen wie Component Object Model (com)-Berechtigung, AuthenticationLevel und Identitätswechsel Ebene.      |
| [**Iswbemservices**](swbemservices.md)           | Erstellt, aktualisiert und ruft Instanzen oder Klassen ab.                                                                       |
| [**Iswbemsink**](swbemsink.md)                   | Empfängt die Ergebnisse der asynchronen Vorgänge von Client Anwendungen und Ereignis Benachrichtigungen.                                 |



 

 

 



