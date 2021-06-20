---
title: Aufzählen von Gruppen, die viele Elemente enthalten
description: Erfahren Sie mehr über das Aufzählen Azure Active Directory Gruppen, die viele Elemente enthalten, indem Sie den inkrementellen Abruf von Daten (Bereichsabruf) verwenden.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Auflisten von Gruppen, die viele Active Directory-Mitglieder enthalten
- gruppen Active Directory , Auflisten von Gruppen mit vielen Mitgliedern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cab63b809fdbd2666f39a09d32f601346da00e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405153"
---
# <a name="enumerating-groups-that-contain-many-members"></a>Aufzählen von Gruppen, die viele Elemente enthalten

Die Mitglieder einer Gruppe werden in einem Mehrwertattribut namens **Member** gespeichert. Das  Memberattribut kann eine große Anzahl von Werten enthalten. Das Auflisten von Membern kann ineffizient sein, wenn die Anzahl der Werte in einem mehrwertigen Attribut groß wird. Der Server begrenzt auch die maximale Anzahl von Werten, die in einer einzelnen Abfrage abgerufen werden können. Dies bedeutet, dass, wenn eine Gruppe möglicherweise mehr Mitglieder hat, als vom Server bereitgestellt werden können, die einzige Möglichkeit zum Aufzählen aller Elemente der inkrementelle Abruf von Daten ist, die als *Bereichsabruf* bezeichnet wird.

Der Bereichsabruf umfasst das Anfordern einer begrenzten Anzahl von Attributwerten in einer einzelnen Abfrage. Die Anzahl der angeforderten Werte muss kleiner oder gleich der maximalen Anzahl von Werten sein, die vom Server unterstützt werden. Um zu reduzieren, wie oft die Abfrage den Server kontaktieren muss, sollte die Anzahl der angeforderten Werte so nahe wie möglich an diesem Maximum liegen. Damit eine Anwendung ordnungsgemäß mit allen Servern funktioniert, sollte eine maximale Anzahl von 1.000 verwendet werden.

Die Version des Servers, der die angeforderten Daten liefert, bestimmt die maximale Anzahl von Werten, die in einer einzelnen Abfrage abgerufen werden können. In der folgenden Tabelle sind die Serverversion und die maximale Anzahl von Werten aufgeführt, die in einer einzelnen Abfrage abgerufen werden können.



| Version des Serverbetriebssystems | Abgerufene Höchstwerte |
|---------------------------------|--------------------------|
| Windows 2000                    | 1000                     |
| Windows Server 2003             | 1500                     |



 

Weitere Informationen zum Abrufen von Bereichen von Attributwerten mit ADSI finden Sie unter Abrufen von [Attributbereichen.](/windows/desktop/ADSI/attribute-range-retrieval)

Weitere Informationen zum Abrufen von Bereichen von Attributwerten mit [System.DirectoryServices](/dotnet/api/system.directoryservices)finden Sie unter [Auflisten von Membern in einer großen Gruppe.](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx)

 

 