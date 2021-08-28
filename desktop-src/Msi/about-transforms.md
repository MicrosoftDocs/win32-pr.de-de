---
description: Eine Transformation ist eine Auflistung von Änderungen, die auf eine Installation angewendet werden. Durch Anwenden einer Transformation auf ein Basisinstallationspaket kann das Installationsprogramm Daten in der Installationsdatenbank hinzufügen oder ersetzen. Das Installationsprogramm kann Transformationen nur während einer Installation anwenden.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: Informationen zu Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635430fb5e75b658880d5c5670219cae950502421c2b188af0381fd60ad3d48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013268"
---
# <a name="about-transforms"></a>Informationen zu Transformationen

Eine Transformation ist eine Auflistung von Änderungen, die auf eine Installation angewendet werden. Durch Anwenden einer Transformation auf ein Basisinstallationspaket kann das Installationsprogramm Daten in der Installationsdatenbank hinzufügen oder ersetzen. Das Installationsprogramm kann Transformationen nur während einer Installation anwenden.

Das Installationsprogramm registriert eine Liste der Transformationen, die für das Produkt während der Installation erforderlich sind. Das Installationsprogramm muss diese Transformationen beim Konfigurieren oder Installieren des Produkts auf das Installationspaket des Produkts anwenden. Wenn eine aufgelistete Transformation nicht verfügbar ist und die Resilienz der Transformationsquelle nicht wiederhergestellt werden kann, schlägt die Installation fehl.

Eine Transformation kann Informationen ändern, die sich in einer beliebigen persistenten Tabelle in der [Installer-Datenbank befindet.](installer-database.md) Eine Transformation kann auch persistente Tabellen in der Installer-Datenbank hinzufügen oder entfernen. Transformationen können keinen Teil eines Installationspakets ändern, der sich nicht [](summary-information-stream.md)in einer Datenbanktabelle befindet, wie z. B. Informationen im Zusammenfassungsinformationsstream, Informationen in Unterstorages oder Dateien in eingebetteten Schränken.

Transformationen verfügen über einen Zusammenfassungsinformationsstream, der Validierungsbedingungen und Fehlerbedingungen enthalten kann. Die Transformationsvalidierungs- und Fehlerbedingungen können den Zusammenfassungsinformationen mithilfe der [**MsiCreateTransformSummaryInfo-Funktion hinzugefügt**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) werden. Die Überprüfungsbedingungen steuern, ob das Installationsprogramm die Transformation auf eine bestimmte Installationsdatenbank anwenden kann. Die Überprüfung der Transformation kann von den Werten der Eigenschaften [**UpgradeCode,**](upgradecode.md) [**ProductCode,**](productcode.md) [**ProductVersion**](productversion.md) und [**ProductLanguage**](productlanguage.md) abhängig sein, die in der Transformation und in der Installationsdatenbank angegeben sind. Die Transformationsfehlerbedingungen steuern, welche Fehler unterdrückt werden, wenn die Transformation angewendet wird. Die in der Transformation enthaltenen Fehlerbedingungen werden durch die Fehlerbedingungen überschrieben, die mithilfe der [**Methoden MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) und [**ApplyTransform angegeben**](database-applytransform.md) werden.

> [!Note]  
> Typische Anpassungstransformationen haben keine Validierungsbedingungen oder überprüfen anhand des [**ProductCode.**](productcode.md) Die in Patchpaketen [gespeicherten Transformationen verfügen](patch-packages.md) in der Regel über strenge Überprüfungsbedingungen, um sicherzustellen, dass die richtige Transformation auf das Patchziel angewendet wird.

 

Es gibt drei Arten von Windows Installer-Transformationen:

-   [Eingebettete Transformationen](embedded-transforms.md)
-   [Gesicherte Transformationen](secured-transforms.md)
-   [Ungesicherte Transformationen](unsecured-transforms.md)

 

 



