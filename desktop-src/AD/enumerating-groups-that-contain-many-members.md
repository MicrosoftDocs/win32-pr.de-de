---
title: Auflisten von Gruppen, die viele Member enthalten
description: Die Mitglieder einer Gruppe werden in einem mehrwertigen Attribut mit dem Namen "Member" gespeichert.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Auflisten von Gruppen, die viele Member enthalten Active Directory
- Gruppen Active Directory, Auflisten von Gruppen mit vielen Membern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2d9a5c9abc6e77ac72672379789d1028f92c3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101454"
---
# <a name="enumerating-groups-that-contain-many-members"></a>Auflisten von Gruppen, die viele Member enthalten

Die Mitglieder einer Gruppe werden in einem mehrwertigen Attribut mit dem Namen " **Member**" gespeichert. Das **Member** -Attribut kann eine große Anzahl von Werten enthalten. Das Auflisten von Membern kann ineffizient sein, wenn die Anzahl von Werten in einem mehrwertigen Attribut groß wird. Der Server schränkt außerdem die maximale Anzahl der Werte ein, die in einer einzelnen Abfrage abgerufen werden können. Dies bedeutet, dass eine Gruppe, die möglicherweise mehr Mitglieder hat, als vom Server bereitgestellt werden kann, nur das inkrementelle Abrufen von Daten verwendet, die als *Bereichs Abruf* bezeichnet werden.

Der Bereichs Abruf umfasst das Anfordern einer begrenzten Anzahl von Attributwerten in einer einzelnen Abfrage. Die Anzahl der angeforderten Werte muss kleiner oder gleich der maximalen Anzahl von Werten sein, die vom Server unterstützt werden. Um die Häufigkeit zu verringern, mit der die Abfrage den Server kontaktieren muss, sollte die Anzahl der angeforderten Werte so nah wie möglich auf diesen Höchstwert liegen. Damit eine Anwendung ordnungsgemäß mit allen Servern funktioniert, sollte eine maximale Anzahl von 1000 verwendet werden.

Die Version des Servers, der die angeforderten Daten bereitstellt, bestimmt die maximale Anzahl von Werten, die in einer einzelnen Abfrage abgerufen werden können. In der folgenden Tabelle werden die Server Version und die maximale Anzahl von Werten aufgelistet, die in einer einzelnen Abfrage abgerufen werden können.



| Server-Betriebssystemversion | Maximal abgerufene Werte |
|---------------------------------|--------------------------|
| Windows 2000                    | 1000                     |
| Windows Server 2003             | 1500                     |



 

Weitere Informationen zum Abrufen von Bereichen mit Attributwerten mit ADSI finden Sie unter [Attribut Bereichs Abruf](/windows/desktop/ADSI/attribute-range-retrieval).

Weitere Informationen zum Abrufen von Bereichen mit Attributwerten mit [System. DirectoryServices](/dotnet/api/system.directoryservices)finden Sie unter Auflisten von Membern [in einer großen Gruppe](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).

 

 