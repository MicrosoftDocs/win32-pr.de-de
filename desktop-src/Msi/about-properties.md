---
description: Windows Installer können die Software Installation konfigurieren, indem Sie die Werte der Variablen verwenden, die in einem Installationspaket oder vom Benutzer definiert sind.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Informationen zu Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215734"
---
# <a name="about-properties"></a>Informationen zu Eigenschaften

Windows Installer können die Software Installation konfigurieren, indem Sie die Werte der Variablen verwenden, die in einem Installationspaket oder vom Benutzer definiert sind.

Windows Installer verwendet während einer Installation drei Kategorien globaler Variablen:

-   Private Eigenschaften: das Installationsprogramm verwendet intern private Eigenschaften, und ihre Werte müssen in der Installations Datenbank erstellt oder auf von der Betriebsumgebung festgelegte Werte festgelegt werden.
-   Öffentliche Eigenschaften: öffentliche Eigenschaften können in der Datenbank erstellt und durch einen Benutzer-oder Systemadministrator in der Befehlszeile geändert werden, durch Anwenden einer Transformation oder durch Interaktion mit einer erstellten Benutzeroberfläche.
-   Eingeschränkte öffentliche Eigenschaften: aus Sicherheitsgründen kann der Autor eines Installationspakets die öffentlichen Eigenschaften einschränken, die ein Benutzer ändern kann.

Nicht alle Eigenschaften müssen in jedem Paket definiert werden. es gibt einen kleinen Satz von erforderlichen Eigenschaften, die in jedem Paket definiert werden müssen. Der Installer legt die Werte von Eigenschaften in einer bestimmten Rangfolge fest.

[Private Eigenschaften](private-properties.md)

[Öffentliche Eigenschaften](public-properties.md)

[Eingeschränkte öffentliche Eigenschaften](restricted-public-properties.md)

[Erforderliche Eigenschaften](required-properties.md)

[Reihenfolge der Eigenschafts Rangfolge](order-of-property-precedence.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Eigenschafts Verweis](property-reference.md)
</dt> </dl>

 

 



