---
description: Die VBScript-Datei WiLstPrd.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Das Beispielskript stellt eine Verbindung mit einem Installerobjekt her und listet registrierte Produkte und Produktinformationen auf.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Auflisten von Produkten, Eigenschaften, Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347189"
---
# <a name="list-products-properties-features-and-components"></a>Auflisten von Produkten, Eigenschaften, Features und Komponenten

Die VBScript-Datei WiLstPrd.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Das Beispielskript stellt eine Verbindung mit einem [**Installerobjekt**](installer-object.md) her und listet registrierte Produkte und Produktinformationen auf.

In diesem Beispiel wird die Verwendung von veranschaulicht:

-   [**ProductInfo-Eigenschaft**](installer-productinfo.md)
-   [**Productstate-Eigenschaft (Installer-Objekt)**](installer-productstate-property.md)
-   [**Products-Eigenschaft**](installer-products.md)
-   [**Features-Eigenschaft**](installer-features.md)
-   [**Featureparent (Eigenschaft)**](installer-featureparent.md)
-   [**Featurestate (Eigenschaft)**](installer-featurestate.md)
-   [**Komponenten Eigenschaft**](installer-components.md)
-   [**Componentclients (Eigenschaft)**](installer-componentclients.md)
-   [**Componentpath (Eigenschaft)**](installer-componentpath.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md)
-   [**REGISTRYVALUE-Methode**](installer-registryvalue.md) des [ **Installer-Objekts**](installer-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ Pfad zur Datei \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiLstPrd.vbs Optionen für den \[ Produktnamen \] \[\]**

Geben Sie den Produktnamen für die Groß-/Kleinschreibung oder die Produkt-ID-GUID des installierten oder angekündigten Produkts an. Wenn kein Produkt oder keine Optionen angegeben werden, listet das Installationsprogramm alle Produkte auf, die auf dem System installiert oder angekündigt wurden.

Beachten Sie, dass es sich bei diesen Optionen nicht um Switches handelt, sodass Sie keinen Schrägstrich (/) in der Befehlszeile voranstellen sollten. Die folgenden Optionen können durch Verkettung der Buchstaben kombiniert werden. Beispiel: "PC" zum Auflisten der Eigenschaften und der installierten Komponenten der Produkte.



| Option               | BESCHREIBUNG                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| keine Optionen angegeben. | Listet die Eigenschaften der Produkte auf.                                                                                                        |
| p                    | Listet die Eigenschaften der Produkte auf.                                                                                                        |
| f                    | Auflisten der Features der Produkte, der übergeordneten Funktionen und der Installations Zustände                                                                 |
| c                    | Listet die installierten Komponenten der Produkte auf.                                                                                              |
| d                    | Listen Sie den Wert unter " **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDLLs** " für die Schlüsseldateien der Komponente "Products" auf. |



 

Weitere Informationen finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md) für weitere Skript Beispiele. Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



