---
description: Um einen WMI-Klassenanbieter zu erstellen, müssen Sie die Win32Provider-Instanz registrieren, die Ihren Anbieter mithilfe einer Instanz \_ \_ von \_ \_ ClassProviderRegistration darstellt.
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: Registrieren eines Klassenanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16a28b489f2cfd01163d6b32c9a70c0d8a193a542197795d6d2b40de0e1baef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316482"
---
# <a name="registering-a-class-provider"></a>Registrieren eines Klassenanbieters

Um einen WMI-Klassenanbieter zu erstellen, müssen Sie die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) registrieren, die Ihren Anbieter darstellt, indem Sie eine Instanz von [**\_ \_ ClassProviderRegistration verwenden.**](--classproviderregistration.md) Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Beim folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters beschrieben.](registering-a-provider.md) Wenn Ihr Anbieter die meisten Daten im WMI-Repository speichert und diese Daten nur bei der WMI-Initialisierung aktualisiert werden, registrieren Sie Ihre Klasse als Pushklassenanbieter. Wenn sich die daten, die Sie bereitstellen, häufig ändern und dynamisch von Ihrem Code bei jeder Anforderung von WMI abgerufen werden, registrieren Sie Ihren Anbieter als Pullklassenanbieter.

Im folgenden Verfahren wird beschrieben, wie Sie einen Pushklassenanbieter registrieren.

**So registrieren Sie einen Pushklassenanbieter**

-   Legen Sie **die InteractionType-Eigenschaft** der [**\_ \_ ClassProviderRegistration-Instanz**](--classproviderregistration.md) auf 1 fest.

    Das Erstellen einer Instanz von [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) ist Teil des Registrierungsprozesses.

Im folgenden Verfahren wird beschrieben, wie Sie einen Pullklassenanbieter registrieren.

**So registrieren Sie einen Pullklassenanbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) die den Anbieter beschreibt.
2.  Erstellen Sie eine Instanz der [**\_ \_ ClassProviderRegistration-Klasse,**](--classproviderregistration.md) die den Funktionssatz des Anbieters beschreibt.

    Innerhalb der [**\_ \_ ClassProviderRegistration-Instanz:**](--classproviderregistration.md)

    1.  Legen Sie die **InteractionType-Eigenschaft** fest, um anzugeben, ob der Anbieter ein Push- oder Pullanbieter ist.
    2.  Kennzeichnen Sie die Klasse mit den [**Qualifizierern Dynamic**](standard-wmi-qualifiers.md) und [**Provider.**](/windows/desktop/api/Provider/nl-provider-provider)

        Der [**Dynamische Qualifizierer**](standard-wmi-qualifiers.md) signalisiert, dass WMI einen Anbieter verwenden soll, um die Klasseninstanzen abzurufen. Der [](/windows/desktop/api/Provider/nl-provider-provider) Anbieterqualifizierer gibt den Namen des Anbieters an, den WMI verwenden soll.

    3.  Definieren Sie **die Eigenschaften ResultSetQueries,** **ReferencedSetQueries** und **UnsupportedQueries.**

        Diese Abfrageeigenschaften beschreiben ausführliche Informationen zur unterstützten Klasse.

Zusätzlich zur Beschreibung der verschiedenen unterstützten Methoden einer Klasse verfügt die [**\_ \_ ClassProviderRegistration-Klasse**](--classproviderregistration.md) auch über drei Eigenschaften, die eine Reihe von Abfragen beschreiben. Bei der gemeinsamen Verwendung beschreiben diese drei Eigenschaften den gesamten Bereich von Klassen, die vom Klassenanbieter bereitgestellt werden. Jede Abfrageeigenschaft enthält eine WQL-SELECT-Anweisung, die als "Schemaabfrage" bezeichnet wird, um die Typen der unterstützten Klassen anzugeben. Schemaabfragen geben einen speziellen Klassennamen namens meta \_ class an. In der folgenden Tabelle sind die Abfrageeigenschaften aufgeführt.



| Eigenschaft                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ResultSetQueries**     | Enthält Informationen über das vom Anbieter zur Verfügung stellende Resultset. WMI verwendet die Informationen, um zu bestimmen, ob der Anbieter aufgerufen werden soll, um eine Abfrage aus einer Anwendung zu erfüllen. Diese Eigenschaft beschreibt entweder den Satz aller Klassen, die der Anbieter bereitstellen kann, oder eine Obermenge der verfügbaren Klassen, aber nie eine Teilmenge. WMI erfordert, dass ein Anbieter mindestens eine Abfrage in dieser Eigenschaft anfordert.<br/> Das folgende Beispiel zeigt, wie **ResultSetQueries** festgelegt wird, wenn ein Anbieter eine Zuordnungsklasse an die [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) verweist.<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> Das folgende Beispiel zeigt, wie eine allgemeine Abfrage angegeben wird, wenn ein Anbieter Klassen an die Hand gibt, die auf andere unbekannte Klassen verweisen.<br/> `SELECT * FROM meta_class`<br/> Im folgenden Beispiel wird gezeigt, wie **ResultSetQueries** festgelegt wird, wenn ein Anbieter nur Unterklassen, aber nicht die übergeordnete Klasse einer bestimmten Klasse liefert.<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> Im folgenden Beispiel wird gezeigt, wie die spezielle diese Eigenschaft verwendet und \_ \_ **ResultSetQueries** festgelegt wird, wenn ein Anbieter alle Klassen und Unterklassen liefert.<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **ReferencedSetQueries** | Bestimmt, ob der Anbieter in Schemaabfragen umgangen werden soll, bei denen Zuordnungen und Verweise angefordert werden. Anbieter, die Zuordnungsklassen liefern können, müssen mindestens eine Abfrage in ihrer **ReferencedSetQueries-Eigenschaft** enthalten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **UnsupportedQueries**   | Enthält Informationen über das Von einem Klassenanbieter nicht zur Verfügung stellende Resultset. WMI verwendet diese Eigenschaft, um von dem Satz von Klassen zu subtrahieren, die von **ResultSetQueries impliziert werden.** Beispielsweise kann ein Klassenanbieter in **ResultSetQueries-Unterstützung** für alle von MyClass abgeleiteten Klassen angeben und in **UnsupportedQueries** eine fehlende Unterstützung für eine bestimmte abgeleitete Klasse angeben.<br/> Je mehr Informationen ein Anbieter über seine Abfrageverarbeitungsfunktionen registrieren kann, desto schneller wird er ausgeführt. Die Eingabe einer oder mehrere Abfragen in die **UnsupportedQueries-Eigenschaft** ist eine Möglichkeit, spezifisch zu sein. Dies ist besonders wichtig, wenn ein Anbieter auf einer Klasse basiert, die er nicht zur Verfügung stellt. Wenn eine Anforderung für eine Klasse erfolgt, die in einer Abfrage in der **UnsupportedQueries-Eigenschaft** aufgeführt ist, kann WMI die Klasse selbst oder einen alternativen Anbieter aufrufen, um sie zu liefern.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Da WMI die OR-Klausel nicht unterstützt, müssen Sie für jede Klasse eine separate Abfrage erstellen.

Die folgenden Abfragen werden in **ResultSetQueries angegeben,** wenn ein Klassenanbieter MyClass1, MyClass2 und MyClass3 anfing.


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



Nur Administratoren können einen Anbieter registrieren oder löschen, indem sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und [**\_ \_ ClassProviderRegistration erstellen.**](--classproviderregistration.md)

 

