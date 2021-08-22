---
title: Aufzählen von Gruppen, die viele Mitglieder enthalten
description: Erfahren Sie mehr über das Aufzählen Azure Active Directory Gruppen, die viele Mitglieder enthalten, indem Sie den inkrementellen Abruf von Daten (Bereichsabruf) verwenden.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Aufzählen von Gruppen, die viele Mitglieder enthalten Active Directory
- gruppen Active Directory , Aufzählen von Gruppen mit vielen Mitgliedern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550ec2f4a77938b26e2273d468d3f9740d637249501aa2396fef3744cd105060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695138"
---
# <a name="enumerating-groups-that-contain-many-members"></a>Aufzählen von Gruppen, die viele Mitglieder enthalten

Die Mitglieder einer Gruppe werden in einem Mehrwertattribut namens Member **gespeichert.** Das  Memberattribut kann eine große Anzahl von Werten enthalten. Das Aufzählen von Membern kann ineffizient sein, wenn die Anzahl der Werte in einem mehrwertigen Attribut groß wird. Der Server schränkt auch die maximale Anzahl von Werten ein, die in einer einzelnen Abfrage abgerufen werden können. Dies bedeutet, dass die einzige Möglichkeit zum Aufzählen aller Elemente die Verwendung des inkrementellen Abrufs von Daten ist, wenn eine Gruppe über mehr Mitglieder als vom Server bereitgestellt werden kann. Dies wird als Bereichsabruf *bezeichnet.*

Der Bereichsabruf umfasst das Anfordern einer begrenzten Anzahl von Attributwerten in einer einzelnen Abfrage. Die Anzahl der angeforderten Werte muss kleiner oder gleich der maximalen Anzahl von Werten sein, die vom Server unterstützt werden. Um zu verringern, wie oft die Abfrage den Server kontaktieren muss, sollte die Anzahl der angeforderten Werte so nah wie möglich an diesem Höchstwert liegen. Damit eine Anwendung ordnungsgemäß mit allen Servern funktioniert, sollte eine maximale Anzahl von 1.000 verwendet werden.

Die Version des Servers, der die angeforderten Daten liefert, bestimmt die maximale Anzahl von Werten, die in einer einzelnen Abfrage abgerufen werden können. In der folgenden Tabelle sind die Serverversion und die maximale Anzahl von Werten aufgeführt, die in einer einzelnen Abfrage abgerufen werden können.



| Serverbetriebssystemversion | Abgerufene Höchstwerte |
|---------------------------------|--------------------------|
| Windows 2000                    | 1000                     |
| Windows Server 2003             | 1500                     |



 

Weitere Informationen zum Abrufen von Bereichen von Attributwerten mit ADSI finden Sie unter [Abrufen von Attributbereichen.](/windows/desktop/ADSI/attribute-range-retrieval)

Weitere Informationen zum Abrufen von Bereichen von Attributwerten mit [System.DirectoryServices finden](/dotnet/api/system.directoryservices)Sie unter [Aufzählen von Membern in einer großen Gruppe.](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx)

 

 