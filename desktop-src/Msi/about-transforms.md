---
description: Eine Transformation ist eine Sammlung von Änderungen, die auf eine Installation angewendet werden. Durch Anwenden einer Transformation auf ein Basis Installationspaket kann das Installationsprogramm Daten in der Installations Datenbank hinzufügen oder ersetzen. Das Installationsprogramm kann während einer Installation nur Transformationen anwenden.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: Informationen zu Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbae9f21ec71209116f3c8eadffca20381cfe71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215731"
---
# <a name="about-transforms"></a>Informationen zu Transformationen

Eine Transformation ist eine Sammlung von Änderungen, die auf eine Installation angewendet werden. Durch Anwenden einer Transformation auf ein Basis Installationspaket kann das Installationsprogramm Daten in der Installations Datenbank hinzufügen oder ersetzen. Das Installationsprogramm kann während einer Installation nur Transformationen anwenden.

Der Installer registriert eine Liste von Transformationen, die während der Installation von dem Produkt benötigt werden. Beim Konfigurieren oder Installieren des Produkts muss das Installationsprogramm diese Transformationen auf das Installationspaket des Produkts anwenden. Wenn eine aufgeführte Transformation nicht verfügbar ist und die Resilienz der Transformations Quelle nicht wieder hergestellt werden kann, tritt bei der Installation ein Fehler auf.

Eine Transformation kann Informationen ändern, die sich in einer persistenten Tabelle in der [Installer-Datenbank](installer-database.md)befinden. Eine Transformation kann auch persistente Tabellen in der Installerdatenbank hinzufügen oder entfernen. Transformationen können keinen Teil eines Installationspakets ändern, der nicht in einer Datenbanktabelle enthalten ist, z. b. Informationen im [Zusammenfassungs Datenstrom](summary-information-stream.md), Informationen in substorages oder Dateien in eingebetteten Schränken.

Transformationen verfügen über einen Zusammenfassungs Informationsdaten Strom, der Validierungs Bedingungen und Fehlerbedingungen enthalten kann. Die Transformations Validierung und Fehlerbedingungen können den Zusammenfassungs Informationen mithilfe der [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) -Funktion hinzugefügt werden. Mit den Validierungs Bedingungen wird gesteuert, ob das Installationsprogramm die Transformation auf eine angegebene Installations Datenbank anwenden kann. Die Überprüfung der Transformation kann auf die Werte der Eigenschaften " [**UpgradeCode**](upgradecode.md)", " [**ProductCode**](productcode.md)", " [**ProductVersion**](productversion.md) " und " [**productlanguage**](productlanguage.md) ", die in der Transformation festgelegt sind, und die in der Installations Datenbank angegebenen Eigenschaften Die Transformations Fehlerbedingungen steuern, welche Fehler beim Anwenden der Transformation unterdrückt werden. Die in der Transformation enthaltenen Fehlerbedingungen werden durch die mithilfe der Methoden [**msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) und [**applytransform**](database-applytransform.md) angegebenen Fehlerbedingungen überschrieben.

> [!Note]  
> Typische Anpassungs Transformationen verfügen über keine Validierungs Bedingungen oder können nicht mit [**ProductCode**](productcode.md)überprüft werden. Die in [patchpaketen](patch-packages.md) gespeicherten Transformationen verfügen im Allgemeinen über strikte Validierungs Bedingungen, um sicherzustellen, dass die richtige Transformation auf das patchziel angewendet wird.

 

Es gibt drei Arten von Windows Installer Transformationen:

-   [Eingebettete Transformationen](embedded-transforms.md)
-   [Gesicherte Transformationen](secured-transforms.md)
-   [Unsichere Transformationen](unsecured-transforms.md)

 

 



