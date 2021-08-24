---
description: Eine Sammlung ist ein Standardautomatisierungskonzept, das eine einheitliche Schnittstelle für eine Gruppe von Objekten bereitstellt, über die Sie Iterationen ausführen können.
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
ms.openlocfilehash: da563830b742b47a138c106b21efe197108bbdddf7ad7f86b90984a04431aa0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860513"
---
# <a name="accessing-a-wmi-collection"></a>Zugreifen auf eine WMI-Sammlung

Eine Sammlung ist ein Standardautomatisierungskonzept, das eine einheitliche Schnittstelle für eine Gruppe von Objekten bereitstellt, über die Sie Iterationen ausführen können. Die Skripterstellungs-API für WMI macht eine Reihe von Schnittstellen verfügbar, die dem Sammlungsparadigma entsprechen. Verwenden Sie in jedem Fall die **Item-Methode,** um die Elemente mithilfe einer Zeichenfolge zu identifizieren, die den Wert enthält.

Die [**Auflistungen SWbemPropertySet,**](swbempropertyset.md) [**SWbemQualifierSet**](swbemqualifierset.md)und [**SWbemMethodSet**](swbemmethodset.md) werden hauptsächlich zum Ändern des Schemas verwendet. Ein [**SWbemObjectSet-Objekt**](swbemobjectset.md) enthält WMI-Objekte, z. B. eine [**Win32 \_ LogicalDisk-Instanz,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) die über Aufrufe wie [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) oder [**SWbemObject.Associators \_**](swbemobject-associators-.md)abgerufen wurden. Das [**SWbemRefresher-Objekt**](swbemrefresher.md) kann nur Instanzen von WMI-Klassen enthalten. Das [**SWbemNamedValueSet-Objekt**](swbemnamedvalueset.md) kann WMI-Objekte oder andere Datentypen enthalten, die ein Anbieter für den Methodenaufruf benötigt.

> [!Note]  
> Die folgenden Themen wurden hauptsächlich für VBScript geschrieben. C# verwendet die [IEnumerable-Standardschnittstelle](/dotnet/api/system.collections.ienumerable) zum Sortieren und Aufzählen von Objekten. Im Gegensatz dazu verwendet PowerShell in der Regel eine implizite Objektauflistung, wenn ein Rückgabewert mehr als ein Ergebnis enthält.

 

In der folgenden Tabelle sind die Auflistungen in der Skripterstellungs-API für WMI sowie die Elemente und Parameter für jede Sammlung aufgeführt.



| Sammlung                                       | Element                                              | Item()-Parameter                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**SWbemObjectSet**](swbemobjectset.md)         | [**Swbemobject**](swbemobject.md)                   | Objektpfad                                                              |
| [**SWbemPropertySet**](swbempropertyset.md)     | [**SWbemProperty**](swbemproperty.md)               | Eigenschaftenname                                                            |
| [**SWbemQualifierSet**](swbemqualifierset.md)   | [**SWbemQualifier**](swbemqualifier.md)             | Qualifizierername                                                           |
| [**SWbemMethodSet**](swbemmethodset.md)         | [**SWbemMethod**](swbemmethod.md)                   | Methodenname                                                              |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | [**SWbemNamedValue**](swbemnamedvalue.md)           | Wertname                                                               |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)   | [**SWbemPrivilege**](swbemprivilege.md)             | Berechtigungsname                                                           |
| [**SWbemRefresher**](swbemrefresher.md)         | [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Index des Elements im [**SWbemRefresher-Objekt**](swbemrefresher.md) |



 

Weitere Informationen und Beispiele zum Hinzufügen und Entfernen von Elementen aus einer Sammlung finden Sie unter [Entfernen eines einzelnen Elements aus einer Sammlung](removing-a-single-item-from-a-collection.md) und Entfernen mehrerer Elemente aus einer [Sammlung.](removing-multiple-items-from-a-collection.md) Weitere Informationen zum Arbeiten mit Klassen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)

 

 
