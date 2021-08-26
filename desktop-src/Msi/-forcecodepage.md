---
description: Die \_ ForceCodepage-Tabelle ist eine spezielle Tabelle, die zum Ändern der Codepage eines Installationspakets verwendet wird. Sie können die Codepage ermitteln oder festlegen, indem Sie eine Textdatei mit dem Namen \_ ForceCodepage.idt exportieren oder importieren.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee252260b0aaee9713c28af5a6d810a3f6a8ed1c1b376b52bd82472cebfd0853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979600"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

Die \_ ForceCodepage-Tabelle ist eine spezielle Tabelle, die zum Ändern der Codepage eines Installationspakets verwendet wird. Sie können die Codepage ermitteln oder festlegen, indem Sie eine [Textdatei](text-archive-files.md) mit dem Namen \_ ForceCodepage.idt exportieren oder importieren.

Das Format der \_ ForceCodepage-Tabelle ist 2 Leere Zeilen gefolgt von einer dritten Zeile, die die numerische Codepage angibt. Beispielsweise würde eine \_ ForceCodepage-Tabellen-IDT-Datei für eine japanische Datenbank wie folgt aussehen. Die numerische Codepage ist in diesem Fall 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Weitere Informationen zur Verwendung von \_ ForceCodepage zum Abrufen oder Festlegen der Codepage einer Datenbank finden Sie in den folgenden Themen.

-   [Codepagebehandlung (Windows Installer)](code-page-handling-windows-installer-.md)
-   [Bestimmen der Codepage einer Installationsdatenbank](determining-an-installation-database-s-code-page.md)
-   [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md)

Die \_ ForceCodepage-Tabelle ist eine spezielle Pseudotabelle, die zum Ändern der Codepage eines Installationspakets verwendet wird. Wenn Sie die \_ ForceCodepage-Tabelle verwenden, wird die Datenbank bedingungslos auf die Codepage festgelegt, ohne dass überprüft wird, ob die derzeit in der Datenbank enthaltenen Daten auf die neue Codepage übersetzt werden können. Es wird immer empfohlen, die Codepage einer Datenbank mit einer sprachneutralen Datenbank zu ändern.

 

 



