---
description: Platt Form Pfad Überschreibung
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Platt Form Pfad Überschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9a6ae6795b444c44db91d90ecd93efd19ea9dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357092"
---
# <a name="platform-path-override"></a>Platt Form Pfad Überschreibung

Mit der [**setupsetplatformpathoverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) -Funktion wird beim Arbeiten mit INF-Dateien von einem anderen Computer eine Platt Form Pfad-außer Kraft setzung für einen Zielcomputer festgelegt. Daher kann Sie auf eine andere Plattform verweisen als auf die, auf der Sie derzeit ausgeführt wird. Für den Umgang mit Medienquellen kann es auf Plattformen verweisen, die nicht mehr unterstützt werden, wie z. b. Alpha, MIPS und PPC. Wenn kein Wert angegeben wird, wird der Platt Form Pfad außer Kraft gesetzt.

Nachdem eine Platt Form Pfad Außerkraftsetzung durch einen aufzurufenden [**setupsetplatformpathoverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea)-Befehl festgelegt wurde, wird die endgültige Komponente des Quell Pfads von jeder Setup Funktion untersucht, die Datei Kopiervorgänge in Warteschlangen Wenn die endgültige Komponente mit dem Namen der Plattform des Benutzers übereinstimmt, wird Sie von der Setup Funktion durch die von **setupsetplatformpathoverride** festgelegte Überschreibungs Zeichenfolge ersetzt.

Wenn Sie z. b. Druckertreiber auf einem MIPS-Server installieren, können Sie Treiber für alle unterstützten Plattformen installieren. Wenn Sie die Dateien in die Warteschlange stellen, werden die Dateien, die in den MIPS-abhängigen Abschnitten der INF-Datei angegeben sind, mit Quell Pfaden installiert \\ \\ \\ \\ Um die Dateien für eine zweite Plattform zu installieren, müssen Sie [**setupsetplatformpathoverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) mit *außer Kraft* Setzung aufrufen, die die Ersatz Plattform angibt. Wenn der durch *override* festgestellte Speicherort den Zeichen folgen Wert "Alpha" enthält, wird der Quellpfad von Datei Kopier Vorgängen, die mit einem Quellpfad der Stamm Quelle MIPS an die Warteschlange gesendet werden, \\ \\ \\ \\ in \\ \\ root \\ Source \\ Alpha geändert. Sie würden diesen Vorgang für jede gewünschte Plattform wiederholen.

 

 



