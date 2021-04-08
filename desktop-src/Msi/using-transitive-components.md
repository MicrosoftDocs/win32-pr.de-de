---
description: Eine typische Verwendung für transitiv Komponenten ist die Vorbereitung eines Produkts, das während eines System Upgrades neu installiert wird.
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: Verwenden transitiv Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35982aafd486a62ce8560e507b8b6caf88e32591
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961260"
---
# <a name="using-transitive-components"></a>Verwenden transitiv Komponenten

Eine typische Verwendung für transitiv Komponenten ist die Vorbereitung eines Produkts, das während eines System Upgrades neu installiert wird. Der Autor des Installationspakets gibt die Komponenten an, die während eines System Upgrades mit dem transitiven Attribut ausgetauscht werden müssen. Wenn der Benutzer zu einem späteren Zeitpunkt ein Upgrade des Systems durchführt, muss das Produkt neu installiert werden. Bei dieser erneuten Installation entfernt das Installationsprogramm die früheren Komponenten und installiert die späteren Komponenten, ohne dass das gesamte Produkt installiert werden muss.

**So schließen Sie zwei transitiv Komponenten in das Installationspaket ein**

1.  Schließen Sie sowohl transitiv Komponenten in das Installationspaket ein.
2.  Erstellen Sie sowohl transitiv Komponenten in der [Komponenten Tabelle](component-table.md) als auch reguläre Komponenten. Jede transitiv Komponente muss über eine eigene eindeutige GUID verfügen, die in der ComponentID-Spalte angegeben ist.
3.  Fügen Sie für jede transitiv Komponente das **msidbcomponentattributestransitive** -Bit in die Attribute-Spalte der Component-Tabelle ein. Wenn dieses Bit festgelegt ist, wertet das Installationsprogramm den Wert der Anweisung in der Spalte Bedingung bei einer erneuten Installation erneut aus.

    Wenn der Wert zuvor false war und in true geändert wurde, installiert der Installer die Komponente.

    Wenn der Wert zuvor true war und in false geändert wurde, entfernt das Installationsprogramm die Komponente, auch wenn die Komponente andere Produkte als Clients hat.

    > [!Note]  
    > Wenn das transitiv Bit nicht festgelegt ist, bleibt die Komponente nach der Installation auch dann aktiviert, wenn die bedingte Anweisung bei einer nachfolgenden Wartungs Installation des Produkts zu false ausgewertet wird. Die Bedingungen müssen nur auf Computer Zuständen basieren. Verwenden Sie nicht mit Bedingungen auf der Grundlage von Benutzer Zuständen oder Eigenschaften, die in der Befehlszeile festgelegt sind, da dies dazu führen kann, dass das Installationsprogramm bei jeder Verwendung durch einen anderen Benutzer eine Neuinstallation des Produkts erfordert.

     

4.  Geben Sie ergänzende bedingte Ausdrücke in die Bedingungs Felder der Steuerelement Tabelle ein, sodass die Bedingung für die erste transitiv Komponente in "false" geändert wird, wenn die Bedingung für die erste transitiv Komponente in "false" geändert wird. Dies führt zum Entfernen der ersten Komponente und der Installation der zweiten Komponente bei der erneuten Installation der Anwendung.

Zum Wechseln der transitiven Komponenten ist eine Neuinstallation des Produkts erforderlich. Paket Autoren müssen daher Benutzern eine Methode zur Neuinstallation des Produkts und zum Festlegen der Modi der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft bereitstellen. Es gibt im Wesentlichen drei Möglichkeiten, die Neuinstallation zu initiieren:

-   Führen Sie aus, und konfigurieren Sie die Neuinstallation über die Benutzeroberfläche, indem Sie ein Paket erstellen, das die [*gesamte*](f-gly.md)Benutzeroberfläche verwendet.
-   Führen Sie die Neuinstallation über die Befehlszeile mithilfe von **msiexec/f** aus, und wählen Sie die Modi in der Liste für die [Befehlszeilenoption](command-line-options.md) **/f** aus.
-   Installieren Sie die Anwendung [**msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) oder [**msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

Das Bit sollte nur mit Bedingungen verwendet werden, die auf Computer Zuständen basieren. Verwenden Sie nicht mit Bedingungen auf der Grundlage von Benutzer Zuständen oder Eigenschaften, die in der Befehlszeile festgelegt sind, da dies dazu führen kann, dass das Installationsprogramm bei jeder Verwendung durch einen anderen Benutzer eine Neuinstallation des Produkts erfordert.

> [!Note]
> Wenn das transitive Bit in der Spalte Attribute für eine Komponente nicht festgelegt ist, bleibt die Komponente nach der Installation auch dann aktiviert, wenn die bedingte Anweisung in der Spalte Bedingung bei einer nachfolgenden Wartung des Produkts zu false ausgewertet wird.
> 
> Wenn eine Anwendung transitiv Komponenten umfasst, erfordert Windows Installer in den meisten Fällen, dass die Anwendung von der Anwendungs Quelle repariert oder aktualisiert wird. In diesen Fällen funktioniert die von einem Originalgerätehersteller gelieferte CD-ROM zur Systemwiederherstellung nicht, und es muss eine tatsächliche Installationsquelle für die Anwendung bereitgestellt werden.

 

 

 



