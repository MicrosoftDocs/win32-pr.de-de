---
description: In der Referenz zur Skript-API für WMI werden alle Skript Objekte beschrieben, die eine bestimmte Syntax verwenden. Eine Erläuterung dieser Syntax finden Sie unter Dokument Konventionen für die Skript-API.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: API-Skript Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30d3269b137686472f54cdb8cf53720b4aad978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215330"
---
# <a name="scripting-api-objects"></a>API-Skript Objekte

In der Referenz zur Skript-API für WMI werden alle Skript Objekte beschrieben, die eine bestimmte Syntax verwenden. Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

In der folgenden Tabelle sind WMI-Skript Objekte und deren Verwendung aufgelistet.



| Object                                               | BESCHREIBUNG                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Swap-DateTime**](swbemdatetime.md)               | Erstellt und analysiert CIM- [DateTime](date-and-time-format.md) -Werte.                                                                                                                                                                                 |
| [**"Errbemeventsource"**](swbemeventsource.md)         | Ruft Ereignisse in Verbindung mit [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md)ab.                                                                                                                               |
| [**Austausch Fehler**](swbemlasterror.md)             | Stellt erweiterte Fehlerinformationen bereit, wenn ein Fehler auftritt.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Ruft ein Objekt vom Typ " [**Swap Services**](swbemservices.md) " ab, das auf einem bestimmten Host Computer Zugriff auf WMI erhalten kann.                                                                                                                                     |
| [**Swap-Methode**](swbemmethod.md)                   | Enthält eine einzelne WMI-Methoden Definition.                                                                                                                                                                                                               |
| [**Swap-methodset**](swbemmethodset.md)             | Ruft eine Auflistung von " [**taubemmethod**](swbemmethod.md) "-Objekten ab.                                                                                                                                                                                       |
| [**"Swap NamedValue"**](swbemnamedvalue.md)           | Enthält einen einzelnen benannten Wert.                                                                                                                                                                                                                         |
| [**Austausch Elementname**](swbemnamedvalueset.md)     | Ruft den Zugriff auf eine Auflistung von " [**taubemnamedvalue**](swbemnamedvalue.md) "-Objekten ab.                                                                                                                                                                     |
| [**Austausch Objekt**](swbemobject.md)                   | Enthält und manipuliert eine einzelne WMI-Objektklasse oder-Instanz.                                                                                                                                                                                        |
| [**Austauschen von "errbemubjectex"**](swbemobjectex.md)               | Erweitert die Funktionalität von [**Swap-Objekte**](swbemobject.md). Dieses Objekt fügt die [**Aktualisierungs**](swbemrefresher-refresh.md) Methode für die Objekte " [**Swap**](swbemrefresher.md) Update" hinzu.                                                           |
| [**Errbemubjectpath**](swbemobjectpath.md)           | Generiert und überprüft einen Objekt Pfad.                                                                                                                                                                                                                |
| [**Austauschen von "errbemubjectset"**](swbemobjectset.md)             | Ruft den Zugriff auf eine Auflistung von [**Swap**](swbemobject.md) -Objekten ab.                                                                                                                                                                             |
| [**Austausch Berechtigung**](swbemprivilege.md)             | Legt eine Berechtigung fest oder löscht sie.                                                                                                                                                                                                                            |
| [**Swap-Privileg**](swbemprivilegeset.md)       | Ruft den Zugriff auf eine Auflistung von [**Swap Privilege**](swbemprivilege.md) -Objekten ab.                                                                                                                                                                       |
| [**Swap Property**](swbemproperty.md)               | Enthält eine einzelne WMI-Eigenschaft.                                                                                                                                                                                                                        |
| [**Swap PropertySet**](swbempropertyset.md)         | Ruft den Zugriff auf eine Auflistung von [**Swap Property**](swbemproperty.md) -Objekten ab.                                                                                                                                                                         |
| [**Austausch Qualifizierer**](swbemqualifier.md)             | Enthält einen einzelnen Eigenschaften Qualifizierer.                                                                                                                                                                                                                  |
| [**Swap-qualifierset**](swbemqualifierset.md)       | Ruft den Zugriff auf eine Auflistung von " [**taubemqualifier**](swbemqualifier.md) "-Objekten ab.                                                                                                                                                                       |
| [**Swap-Aktualisierungs Programm**](swbemrefresher.md)             | Sammelt und aktualisiert Objekt Eigenschaftswerte in einem Vorgang.                                                                                                                                                                                          |
| [**Swap-aktuableitem**](swbemrefreshableitem.md) | Stellt ein einzelnes Aktualisier bares Element in einem " [**Swap**](swbemrefresher.md) "-Objekt dar, z. b. eine-Eigenschaft.                                                                                                                                     |
| [**Austausch Sicherheit**](swbemsecurity.md)               | Verwaltet Sicherheitseinstellungen wie z. b. Component Object Model (com)- [**Berechtigungen**](swbemsecurity-privileges.md), [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)und Identitätswechsel [**Ebene**](swbemsecurity-impersonationlevel.md).   |
| [**SWbemServices**](swbemservices.md)               | Erstellt, aktualisiert und ruft Instanzen oder Klassen ab.                                                                                                                                                                                                  |
| [**Swap Service Ex**](swbemservicesex.md)           | Erweitert die Funktionalität von [**Swap Services**](swbemservices.md). Dieses Objekt fügt die [**Put**](swbemservicesex-put.md) -Methode und die [**putasync**](swbemservicesex-putasync.md) -Methode hinzu, um zuzulassen, dass eine Klasse oder eine Instanz in mehreren Namespaces gespeichert wird. |
| [**Swap-Senke**](swbemsink.md)                       | Empfängt die Ergebnisse von asynchronen Vorgängen und Ereignis Benachrichtigungen, die von Client Anwendungen verwendet werden.                                                                                                                                        |



 

 

 



