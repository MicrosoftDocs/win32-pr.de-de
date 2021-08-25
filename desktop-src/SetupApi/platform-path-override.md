---
description: Plattformpfadüberschreibung
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Plattformpfadüberschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63cc1e6ba4b1cb53c26e380eeab95a96091d5159e8356d8f7067529a6b589d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992620"
---
# <a name="platform-path-override"></a>Plattformpfadüberschreibung

Die [**SetupSetPlatformPathOverride-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) wird verwendet, um eine Plattformpfadüberschreibung für einen Zielcomputer beim Arbeiten mit INF-Dateien von einem anderen Computer einzurichten. Daher kann sie auf eine andere Plattform verweisen als die, auf der sie derzeit ausgeführt wird. Für den Umgang mit Medienquellen kann er sich auf Plattformen beziehen, die nicht mehr unterstützt werden, z. B. Alpha, MIPS und PPC. Die Außerkraftsetzung des Plattformpfads wird entfernt, wenn kein Wert angegeben ist.

Nachdem eine Plattformpfadüberschreibung durch einen Aufruf von [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea)festgelegt wurde, überprüft jede Setupfunktion, die Dateikopiervorgänge in die Warteschlange einreiht, die letzte Komponente des Quellpfads. Wenn die endgültige Komponente dem Namen der Plattform des Benutzers entspricht, ersetzt die Setupfunktion sie durch die überschreibende Zeichenfolge, die von **SetupSetPlatformPathOverride festgelegt wurde.**

Wenn Sie beispielsweise Druckertreiber auf einem MIPS-Server installieren, sollten Sie Treiber für alle unterstützten Plattformen installieren. Wenn Sie die Dateien in die Warteschlange einsenden, werden die in den MIPS-abhängigen Abschnitten der INF-Datei angegebenen Dateien mit Quellpfaden wie \\ \\ Stammquellen-Mips \\ \\ installiert. Um die Dateien für eine zweite Plattform zu installieren, müssen Sie [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) mit *Override* aufrufen, das die Ersatzplattform angibt. Wenn der durch  Außerkraftsetzung angegebene Speicherort den Zeichenfolgenwert "alpha" enthält, würden Dateikopiervorgänge, die an die Warteschlange mit einem Quellpfad mit Stammquellen-Mips gesendet werden, ihren Quellpfad in Stammquellen-Alpha \\ \\ \\ \\ \\ \\ \\ \\ ändern. Sie würden diesen Vorgang für jede plattform von Interesse wiederholen.

 

 



