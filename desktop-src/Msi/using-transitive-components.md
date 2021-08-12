---
description: Eine typische Verwendung für transitive Komponenten ist die Vorbereitung eines Produkts für die Neuinstallation während eines Systemupgrades.
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: Verwenden transitiver Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ad6906b3e5d29ba6c0e3f8e279f4a1df2d5578f931219b6962062efaabd375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622888"
---
# <a name="using-transitive-components"></a>Verwenden transitiver Komponenten

Eine typische Verwendung für transitive Komponenten ist die Vorbereitung eines Produkts für die Neuinstallation während eines Systemupgrades. Der Autor des Installationspakets gibt die Komponenten an, die während eines Systemupgrades ausgetauscht werden müssen, da sie das transitive Attribut aufweisen. Wenn der Benutzer das System später aktualisiert, muss das Produkt neu installiert werden. Nach dieser Neuinstallation entfernt das Installationsprogramm die früheren Komponenten und installiert die späteren Komponenten, ohne das gesamte Produkt installieren zu müssen.

**So schließen Sie zwei transitive Komponenten in das Installationspaket ein**

1.  Schließen Sie beide transitiven Komponenten in das Installationspaket ein.
2.  Erstellen Sie beide transitiven Komponenten in der [Komponententabelle](component-table.md) genauso wie reguläre Komponenten. Jede transitive Komponente muss über eine eigene eindeutige GUID verfügen, die in der ComponentId-Spalte angegeben ist.
3.  Schließen Sie das **Bit msidbComponentAttributesTransitive** für jede transitive Komponente in die Attributes -Spalte der Component-Tabelle ein. Wenn dieses Bit festgelegt ist, wertet das Installationsprogramm bei einer Neuinstallation den Wert der Anweisung in der Spalte Bedingung erneut aus.

    Wenn der Wert zuvor False war und in True geändert wurde, installiert das Installationsprogramm die Komponente.

    Wenn der Wert zuvor True war und in False geändert wurde, entfernt das Installationsprogramm die Komponente, auch wenn die Komponente über andere Produkte als Clients verfügt.

    > [!Note]  
    > Sofern das transitive Bit nicht festgelegt ist, bleibt die Komponente nach der Installation aktiviert, auch wenn die bedingte Anweisung bei einer nachfolgenden Wartungsinstallation des Produkts als False ausgewertet wird. Die Bedingungen dürfen nur auf Computerzuständen basieren. Verwenden Sie nicht mit Bedingungen, die auf Benutzerzuständen oder Eigenschaften basieren, die in der Befehlszeile festgelegt sind, da dies dazu führen kann, dass das Installationsprogramm bei jeder Verwendung durch einen anderen Benutzer eine Neuinstallation des Produkts erfordert.

     

4.  Geben Sie ergänzende bedingte Ausdrücke in die Felder Bedingung der Control-Tabelle ein, sodass die Bedingung für die erste transitive Komponente in False geändert wird, die Bedingung für die zweite transitive Komponente in True geändert wird. Dies führt dazu, dass die erste Komponente entfernt und die zweite Komponente nach der Neuinstallation der Anwendung installiert wird.

Eine Neuinstallation des Produkts ist erforderlich, um die transitiven Komponenten zu wechseln. Paketautoren müssen benutzern daher eine Methode zum erneuten Installieren des Produkts und zum Festlegen der Modi der [**REINSTALLMODE-Eigenschaft**](reinstallmode.md) bereitstellen. Es gibt im Grunde drei Möglichkeiten, die Neuinstallation auszulösen:

-   Führen Sie die Neuinstallation über die Benutzeroberfläche aus, und konfigurieren Sie sie, indem Sie ein Paket erstellen, das die [*vollständige Benutzeroberfläche verwendet.*](f-gly.md)
-   Führen Sie die Neuinstallation über die Befehlszeile mithilfe von **msiexec /f** aus, und wählen Sie die Modi in der Liste für die [Befehlszeilenoption](command-line-options.md) **/f** aus.
-   Lassen Sie die Anwendung [**MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) oder [**MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)aufrufen.

Das Bit sollte nur mit Bedingungen verwendet werden, die auf Computerzuständen basieren. Verwenden Sie nicht mit Bedingungen, die auf Benutzerzuständen oder Eigenschaften basieren, die in der Befehlszeile festgelegt sind, da dies dazu führen kann, dass das Installationsprogramm bei jeder Verwendung durch einen anderen Benutzer eine Neuinstallation des Produkts erfordert.

> [!Note]
> Sofern das Transitive Bit in der Spalte Attribute nicht für eine Komponente festgelegt ist, bleibt die Komponente nach der Installation aktiviert, auch wenn die bedingungsbedingte Anweisung in der Spalte Bedingung bei einer nachfolgenden Wartungsinstallation des Produkts als False ausgewertet wird.
> 
> Wenn eine Anwendung transitive Komponenten enthält, erfordert Windows Installer in den meisten Fällen die Quelle der Anwendung, um die Anwendung zu reparieren oder zu aktualisieren. In diesen Fällen funktioniert die von einem Originalgerätehersteller gelieferte CD-ROM für die Systemwiederherstellung nicht, und es muss eine tatsächliche Installationsquelle für die Anwendung bereitgestellt werden.

 

 

 



