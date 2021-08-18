---
description: Die VBScript-WiLstPrd.vbs wird in den sdk-Komponenten Windows für Windows Installer-Entwickler bereitgestellt. Das Beispielskript stellt eine Verbindung mit einem Installer-Objekt und listet registrierte Produkte und Produktinformationen auf.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Auflisten von Produkten, Eigenschaften, Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa090deef877757277b64cef02ecf42df61405fdc9238935bfffba756434f316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013148"
---
# <a name="list-products-properties-features-and-components"></a>Auflisten von Produkten, Eigenschaften, Features und Komponenten

Die VBScript-WiLstPrd.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Das Beispielskript stellt eine Verbindung mit einem [**Installer-Objekt**](installer-object.md) und listet registrierte Produkte und Produktinformationen auf.

Dieses Beispiel veranschaulicht die Verwendung von:

-   [**ProductInfo-Eigenschaft**](installer-productinfo.md)
-   [**ProductState-Eigenschaft (Installer-Objekt)**](installer-productstate-property.md)
-   [**Products-Eigenschaft**](installer-products.md)
-   [**Features (Eigenschaft)**](installer-features.md)
-   [**FeatureParent-Eigenschaft**](installer-featureparent.md)
-   [**FeatureState-Eigenschaft**](installer-featurestate.md)
-   [**Components-Eigenschaft**](installer-components.md)
-   [**ComponentClients(Eigenschaft)**](installer-componentclients.md)
-   [**ComponentPath-Eigenschaft**](installer-componentpath.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md)
-   [**RegistryValue-Methode**](installer-registryvalue.md) des [ **Installer-Objekts**](installer-object.md)

Sie benötigen die CScript.exe oder WScript.exe von Windows Script Host, um dieses Beispiel verwenden zu können. Um dieses CScript.exe ausführen zu können, geben Sie an der Eingabeaufforderung eine Befehlszeile mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ Pfad zur Datei \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiLstPrd.vbs \[ \] \[ Produktname-Optionen\]**

Geben Sie den Produktnamen ohne Unterscheidung nach Groß-/Kleinschreibung oder die Produkt-ID-GUID des installierten oder angekündigten Produkts an. Wenn keine Produkte oder Optionen angegeben sind, listet das Installationsprogramm alle auf dem System installierten oder angekündigten Produkte auf.

Beachten Sie, dass es sich bei diesen Optionen nicht um Schalter handelt. Daher sollten Sie ihnen keinen Schrägstrich (/) in der Befehlszeile voran stellen. Die folgenden Optionen können kombiniert werden, indem die Buchstaben verkettet werden. Beispiel: "pc", um sowohl die Eigenschaften der Produkte als auch die installierten Komponenten auflisten zu können.



| Option               | Beschreibung                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| keine Optionen angegeben | Listen Sie die Eigenschaften der Produkte auf.                                                                                                        |
| p                    | Listen Sie die Eigenschaften der Produkte auf.                                                                                                        |
| f                    | Auflisten der Produktfeatures, Deren Elemente und Installationszustände                                                                 |
| c                    | Listet die installierten Komponenten der Produkte auf.                                                                                              |
| d                    | Listen Sie den Wert **unter HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion \\ SharedDlls** für die Schlüsseldateien der Produktkomponente auf. |



 

Weitere Informationen finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) für zusätzliche Skriptbeispiele. Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



