---
description: Windows Das Installationsprogramm kann die Softwareinstallation mithilfe der Werte von Variablen konfigurieren, die in einem Installationspaket oder vom Benutzer definiert sind.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Informationen zu Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a7bdd5a70721520c4d2afb975aabaca312975dc3bf4b7d94215112f69a0a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382077"
---
# <a name="about-properties"></a>Informationen zu Eigenschaften

Windows Das Installationsprogramm kann die Softwareinstallation mithilfe der Werte von Variablen konfigurieren, die in einem Installationspaket oder vom Benutzer definiert sind.

Windows Das Installationsprogramm verwendet während einer Installation drei Kategorien von globalen Variablen:

-   Private Eigenschaften: Das Installationsprogramm verwendet intern private Eigenschaften, und ihre Werte müssen in der Installationsdatenbank erstellt oder auf Werte festgelegt werden, die von der Betriebsumgebung bestimmt werden.
-   Öffentliche Eigenschaften: Öffentliche Eigenschaften können in der Datenbank erstellt und von einem Benutzer oder Systemadministrator über die Befehlszeile, durch Anwenden einer Transformation oder durch Interaktion mit einer erstellten Benutzeroberfläche geändert werden.
-   Eingeschränkte öffentliche Eigenschaften: Aus Sicherheitsgründen kann der Autor eines Installationspakets die öffentlichen Eigenschaften einschränken, die ein Benutzer ändern kann.

Nicht alle Eigenschaften müssen in jedem Paket definiert werden. Es gibt einen kleinen Satz erforderlicher Eigenschaften, die in jedem Paket definiert werden müssen. Das Installationsprogramm legt die Werte von Eigenschaften in einer bestimmten Rangfolge fest.

[Private Eigenschaften](private-properties.md)

[Öffentliche Eigenschaften](public-properties.md)

[Eingeschränkte öffentliche Eigenschaften](restricted-public-properties.md)

[Erforderliche Eigenschaften](required-properties.md)

[Rangfolge der Eigenschaften](order-of-property-precedence.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Eigenschaftenverweis](property-reference.md)
</dt> </dl>

 

 



