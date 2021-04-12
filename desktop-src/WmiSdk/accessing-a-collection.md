---
description: Eine Sammlung ist ein Standardmäßiges Automatisierungskonzept, das eine einheitliche Schnittstelle für eine Reihe von Objekten bereitstellt, über die Sie Iterationen ausführen können.
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: Zugreifen auf eine WMI-Sammlung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b875f50c1778a03c304f90c019da172be6ef5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217970"
---
# <a name="accessing-a-wmi-collection"></a>Zugreifen auf eine WMI-Sammlung

Eine Sammlung ist ein Standardmäßiges Automatisierungskonzept, das eine einheitliche Schnittstelle für eine Reihe von Objekten bereitstellt, über die Sie Iterationen ausführen können. Die Skript-API für WMI macht eine Reihe von Schnittstellen verfügbar, die dem Sammlungs Paradigma entsprechen. Verwenden Sie in jedem Fall die **Item** -Methode, um die Elemente mithilfe einer Zeichenfolge zu identifizieren, die den Wert enthält.

Die Listungen " [**Swap PropertySet**](swbempropertyset.md)", " [**gobemqualifierset**](swbemqualifierset.md)" und " [**taubemmethodset**](swbemmethodset.md) " werden größtenteils zum Ändern des Schemas verwendet. Ein Objekt vom Typ " [**errbewbjectset**](swbemobjectset.md) " enthält WMI-Objekte (z. b. eine [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Instanz), die durch Aufrufe abgerufen wurden, z. b. "WS- [**Services. InstancesOf**](swbemservices-instancesof.md) " oder " [**errbewbject. ASSOCIATORS \_**](swbemobject-associators-.md)" Das [**taubemaktualisierungs**](swbemrefresher.md) -Objekt kann nur Instanzen von WMI-Klassen enthalten. Das Objekt "WS [**bemnamedvalueset**](swbemnamedvalueset.md) " kann WMI-Objekte oder beliebige andere Datentypen enthalten, die ein Anbieter für den Methoden aufrufbedarf benötigt.

> [!Note]  
> Die folgenden Themen wurden primär für VBScript geschrieben. C# verwendet die standardmäßige [IEnumerable](/dotnet/api/system.collections.ienumerable) -Schnittstelle, um Objekte zu sortieren und aufzuzählen. Im Gegensatz dazu verwendet PowerShell im Allgemeinen eine implizite Objekt Auflistung, wenn ein Rückgabewert mehr als ein Ergebnis enthält.

 

In der folgenden Tabelle werden die Auflistungen in der Skript-API für WMI und die Elemente und Parameter für die einzelnen Sammlungen aufgelistet.



| Sammlung                                       | Element                                              | Item ()-Parameter                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**Austauschen von "errbemubjectset"**](swbemobjectset.md)         | [**Austausch Objekt**](swbemobject.md)                   | Objekt Pfad                                                              |
| [**Swap PropertySet**](swbempropertyset.md)     | [**Swap Property**](swbemproperty.md)               | Eigenschaftenname                                                            |
| [**Swap-qualifierset**](swbemqualifierset.md)   | [**Austausch Qualifizierer**](swbemqualifier.md)             | Qualifizierername                                                           |
| [**Swap-methodset**](swbemmethodset.md)         | [**Swap-Methode**](swbemmethod.md)                   | Methodenname                                                              |
| [**Austausch Elementname**](swbemnamedvalueset.md) | [**"Swap NamedValue"**](swbemnamedvalue.md)           | Wertname                                                               |
| [**Swap-Privileg**](swbemprivilegeset.md)   | [**Austausch Berechtigung**](swbemprivilege.md)             | Berechtigungs Name                                                           |
| [**Swap-Aktualisierungs Programm**](swbemrefresher.md)         | [**Swap-aktuableitem**](swbemrefreshableitem.md) | Index des Elements im Objekt " [**Swap**](swbemrefresher.md) -Aktualisierungs Programm" |



 

Weitere Informationen zu und Beispielen zum Hinzufügen und Entfernen von Elementen aus einer Auflistung finden Sie unter [Entfernen eines einzelnen Elements aus](removing-a-single-item-from-a-collection.md) einer Auflistung und [Entfernen mehrerer Elemente aus einer](removing-multiple-items-from-a-collection.md)Sammlung. Weitere Informationen zum Arbeiten mit Klassen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

 

 
