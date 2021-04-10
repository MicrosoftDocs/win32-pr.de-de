---
description: Zum Erstellen eines WMI-Klassen Anbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ classproviderregistration registrieren.
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: Registrieren eines Klassen Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15893e654f96f8c4e476219389a1f8f2c464a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959331"
---
# <a name="registering-a-class-provider"></a>Registrieren eines Klassen Anbieters

Zum Erstellen eines WMI-Klassen Anbieters müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ classproviderregistration**](--classproviderregistration.md)registrieren. Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben. Wenn Ihr Anbieter die meisten Daten im WMI-Repository speichert und diese Daten nur bei der WMI-Initialisierung aktualisiert werden, registrieren Sie Ihre Klasse als Push-Klassen Anbieter. Wenn die von Ihnen bereitgestellten Daten häufig geändert werden und dynamisch durch Ihren Code bei jeder WMI-Anforderung abgerufen werden, registrieren Sie den Anbieter als Pull-Klassen Anbieter.

Im folgenden Verfahren wird beschrieben, wie ein Push-Klassen Anbieter registriert wird.

**So registrieren Sie einen Push-Klassen Anbieter**

-   Legen Sie die **interaktiontype** -Eigenschaft der [**\_ \_ classproviderregistration**](--classproviderregistration.md) -Instanz auf 1 fest.

    Das Erstellen einer Instanz von [**\_ \_ classproviderregistration**](--classproviderregistration.md) ist Teil des Registrierungsprozesses.

Im folgenden Verfahren wird beschrieben, wie Sie einen Pull Class-Anbieter registrieren.

**So registrieren Sie einen Pull-Klassen Anbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.
2.  Erstellen Sie eine Instanz der [**\_ \_ classproviderregistration**](--classproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.

    Innerhalb der [**\_ \_ classproviderregistration**](--classproviderregistration.md) -Instanz:

    1.  Legen Sie die **interaktiontype** -Eigenschaft fest, um anzugeben, ob der Anbieter ein Push-oder Pull-Anbieter ist.
    2.  Markieren Sie die Klasse mit dem [**dynamischen**](standard-wmi-qualifiers.md) und den [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider) Qualifizierern.

        Der [**dynamische**](standard-wmi-qualifiers.md) Qualifizierer signalisiert, dass WMI einen Anbieter zum Abrufen der Klassen Instanzen verwenden soll. Der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) gibt den Namen des Anbieters an, der von WMI verwendet werden soll.

    3.  Definieren Sie die Eigenschaften " **resultsetqueries**", " **referencedsetqueries**" und " **unsupportedqueries** ".

        Diese Abfrage Eigenschaften beschreiben ausführliche Informationen zur unterstützten Klasse.

Neben der Beschreibung der verschiedenen unterstützten Methoden einer Klasse verfügt auch die [**\_ \_ classproviderregistration**](--classproviderregistration.md) -Klasse über drei Eigenschaften, die eine Reihe von Abfragen beschreiben. Bei der gemeinsamen Verwendung beschreiben diese drei Eigenschaften den gesamten vom Klassen Anbieter bereitgestellten Klassen Bereich. Jede Abfrage Eigenschaft enthält eine WQL SELECT-Anweisung, die als "Schema Abfrage" bezeichnet wird, um die Typen der unterstützten Klassen anzugeben. Schema Abfragen geben einen speziellen Klassennamen mit dem Namen Meta \_ Class an. In der folgenden Tabelle sind die Abfrage Eigenschaften aufgeführt.



| Eigenschaft                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resultsetqueries**     | Enthält Informationen über das Resultset, das der Anbieter bereitstellt. WMI verwendet die Informationen, um zu bestimmen, ob der Anbieter aufgerufen werden soll, um eine Abfrage von einer Anwendung zu erfüllen. Diese Eigenschaft beschreibt entweder den Satz aller Klassen, die der Anbieter bereitstellen kann, oder eine übergeordnete Gruppe der verfügbaren Klassen, aber nie eine Teilmenge. WMI erfordert, dass ein Anbieter mindestens eine Abfrage in dieser Eigenschaft angibt.<br/> Im folgenden Beispiel wird gezeigt, wie **resultsetqueries** festgelegt wird, wenn ein Anbieter eine Association-Klasse bereitstellt, die auf die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse verweist.<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> Im folgenden Beispiel wird gezeigt, wie eine allgemeine Abfrage angegeben wird, wenn ein Anbieter Klassen bereitstellt, die auf andere unbekannte Klassen verweisen.<br/> `SELECT * FROM meta_class`<br/> Im folgenden Beispiel wird gezeigt, wie **resultsetqueries** festgelegt wird, wenn ein Anbieter nur Unterklassen bereitstellt, aber nicht die übergeordnete Klasse einer bestimmten Klasse.<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> Im folgenden Beispiel wird gezeigt, wie die spezielle \_ \_ Eigenschaft dieser Eigenschaft verwendet und **resultsetqueries** festgelegt wird, wenn ein Anbieter alle Klassen und Unterklassen bereitstellt.<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **Referencedsetqueries** | Bestimmt, ob der Anbieter in Schema Abfragen umgangen werden soll, in denen Zuordnungen und Verweise angefordert werden. Anbieter, die Zuordnungs Klassen bereitstellen können, müssen mindestens eine Abfrage in Ihre **referencedsetqueries** -Eigenschaft einschließen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Nicht supportedqueries**   | Enthält Informationen über das Resultset, das ein Klassen Anbieter nicht bereitstellt. WMI verwendet diese Eigenschaft, um von dem Satz von Klassen, die von **resultsetqueries** impliziert werden, zu subtrahieren. Ein Klassen Anbieter kann z. b. in der **resultsetqueries** -Unterstützung für alle von MyClass abgeleiteten Klassen angeben und in **unsupportedqueries** eine fehlende Unterstützung für eine bestimmte abgeleitete Klasse angeben.<br/> Weitere Informationen, die ein Anbieter über seine Abfrage Verarbeitungsfunktionen registrieren kann, desto schneller. Das Eingeben einer oder mehrerer Abfragen in der **unsupportedqueries** -Eigenschaft ist eine Möglichkeit, spezifisch zu sein. Dies ist besonders wichtig, wenn ein Anbieter von einer Klasse abhängig ist, die er nicht bereitstellt. Wenn eine Anforderung für eine Klasse erfolgt, die in einer Abfrage in der **unsupportedqueries** -Eigenschaft aufgelistet ist, kann WMI die Klasse selbst bereitstellen oder einen alternativen Anbieter aufrufen, um Sie bereitzustellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Da WMI die-oder-Klausel nicht unterstützt, müssen Sie für jede Klasse eine separate Abfrage erstellen.

Die folgenden Abfragen werden in **resultsetqueries** angegeben, wenn ein Klassen Anbieter MyClass1, MyClass2 und MyClass3 bereitstellt.


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



Nur Administratoren können einen Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und [**\_ \_ classproviderregistration**](--classproviderregistration.md)erstellen.

 

