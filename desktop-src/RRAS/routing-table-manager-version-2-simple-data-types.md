---
title: Routing Table Manager, Version 2, einfache Datentypen
description: Die RTMv2-API definiert mehrere einfache Datentypen. In der folgenden Tabelle sind diese Datentypen aufgeführt.
ms.assetid: e935518e-b8d8-47fb-b2b2-c9750c2b540e
keywords:
- RRAS für den Routing-und RAS-Dienst, Routing-Tabellen-Manager Version 2, einfache Datentypen
- Routing Table Manager Version 2 RRAS, simple Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dbd7530799c1c7e1702e0384d51b37a77dda0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712089"
---
# <a name="routing-table-manager-version-2-simple-data-types"></a>Routing Table Manager, Version 2, einfache Datentypen

Die RTMv2-API definiert mehrere einfache Datentypen. In der folgenden Tabelle sind diese Datentypen aufgeführt.



| Datentyp                                                                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                      | TypeDef              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| RTM- \_ Sicht- \_ ID, \* PRTM- \_ Ansichts- \_ ID                                                                                                                                                                                                                                                                                             | Identifiziert eine bestimmte Ansicht.                                                                                                                    | INT                  |
| DWORD-RTM- \_ Ansichts \_ Satz, \* PRTM- \_ Ansichts \_ Satz                                                                                                                                                                                                                                                                                     | Identifiziert eine Gruppe von Sichten. wird als Maske ausgedrückt.                                                                                                  | DWORD                |
| RTM- \_ Entitäts \_ handle, \* PRTM- \_ Entitäts \_ handle, RTM \_ dest- \_ handle, \* PRTM \_ dest- \_ handle, RTM-Routen \_ \_ handle, PRTM-Routen Handle \* \_ \_ , RTM- \_ nexthop- \_ handle, \* PRTM- \_ nexthop-handle, RTM-Aufzählungs handle, PRTM-Aufzählungs \_ \_ \_ \* \_ \_ \_ \_ \_ \* \_ \_ \_ \_ \_ \* \_ \_ handle, RTM-Weiterleitungs handle | Handles, die auf RTMv2-Daten zeigen.                                                                                                                  | HANDLE               |
| RTM- \_ Entitäts \_ \_ Methodentyp, \* PRTM- \_ \_ \_ Entitätstyp                                                                                                                                                                                                                                                                     | Identifiziert die von einem registrierten Client exportierten Methoden.                                                                                              | DWORD                |
| RTM- \_ Entitäts \_ Export \_ Methode, \* PRTM- \_ Entitäts \_ Export \_ Methode                                                                                                                                                                                                                                                                 | Gibt den allgemeinen Prototyp für Client Methoden an.                                                                                               | \_Entity- \_ Methode     |
| RTM-Weiterleitungs \_ \_ Änderungs \_ Flags, PRTM-Weiterleitungs \* \_ \_ Änderungs \_ Flags                                                                                                                                                                                                                                                                     | Eingabe-und Ausgabeflags, mit denen der Status angegeben wird, wenn eine Route hinzugefügt oder aktualisiert wird.                                                               | DWORD                |
| RTM \_ nexthop \_ - \_ änderungflags, \* PRTM \_ nexthop- \_ \_ änderungflags                                                                                                                                                                                                                                                                 | Ausgabeflags, mit denen der Zustand angegeben wird, wenn ein nächster Hop hinzugefügt wird.                                                                                 | DWORD                |
| RTM-Übereinstimmungs \_ \_ Flags, \* PRTM- \_ Übereinstimmungs \_                                                                                                                                                                                                                                                                                     | Eingabeflags, mit denen Kriterien angegeben werden, wenn Routen in der Routing Tabelle übereinstimmen.                                                                  | DWORD                |
| RTM- \_ Enum- \_ Flags, \* PRTM- \_ Enum- \_ Flags                                                                                                                                                                                                                                                                                       | Identifiziert Enumerationen.                                                                                                                         | DWORD                |
| RTM- \_ Benachrichtigungs- \_ Flags, \* PRTM- \_ Benachrichtigungs \_ Flags                                                                                                                                                                                                                                                                                   | Ausgabeflags, die verwendet werden, um anzugeben, welcher Benachrichtigungstyp ausgegeben wird. wird wie folgt zusammengesetzt: (Änderungs Typen, die von \| einem Client geändert werden). | DWORD                |
| RTM- \_ Ereignis \_ Rückruf, \* PRTM- \_ Ereignis \_ Rückruf;                                                                                                                                                                                                                                                                              | Gibt den Rückruf an, mit dem Clients benachrichtigt werden, dass eine Änderung im Routen Status oder registrierten Clients aufgetreten ist.                                  | RTM- \_ Ereignis \_ Rückruf |



 

 

 




