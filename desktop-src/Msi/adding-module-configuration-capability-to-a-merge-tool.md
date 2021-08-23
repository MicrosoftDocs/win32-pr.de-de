---
description: Windows Installerentwickler können Tools erstellen, mit denen Endbenutzer konfigurierbare Mergemodule verwenden können.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Hinzufügen der Modulkonfigurationsfunktion zu einem Mergetool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb20645d4a66b09ffa95e34f04e9057bd0a8c57e645be652d8ea8cd595ddd6cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252100"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>Hinzufügen der Modulkonfigurationsfunktion zu einem Mergetool

Damit Endbenutzer konfigurierbare Mergemodule verwenden können, können Sie Merge- und Konfigurationstools für folgende Zwecke erstellen:

-   Mergetools sollten die Funktionen in Mergemod.dll Version 2.0 aufrufen, um das Modul zusammenzuführen. Frühere Versionen von Mergemod.dll können nicht zum Konfigurieren von Mergemodulen verwendet werden.
-   Clientkonfigurationsanwendungen sollten mit dem Mergemodulbenutzer interagieren, um die Benutzerauswahl für konfigurierbare Elemente zu erfassen.
-   Mergetools sollten Konfigurationsinformationen, die im Mergemodul erstellt wurden, für die Clientanwendung verfügbar machen, damit der Client diese Informationen zum Abfragen des Benutzers verwenden kann.
-   Wenn ein Mergetool während einer Zusammenführung auf ein konfigurierbares Element trifft, sollte es das Clientkonfigurationstool aufrufen, um vom Benutzer abgerufene Anpassungsinformationen zu erhalten. Das Mergetool sollte die angegebenen Änderungen am Mergemodul vornehmen.
-   Konfigurationsanwendungen sollten es dem Benutzer ermöglichen, Optionen für konfigurierbare Elemente bereitzustellen, aber alle möglichen Optionen müssen dem Benutzer nicht angezeigt werden. Das Mergetool kann Standardwerte für konfigurierbare Elemente verwenden, die der Benutzer nicht auswählt.
-   Wenn ein Benutzer keine Anpassungsinformationen bereitstellt, sollten Mergetools die standardkonfigurationswerte verwenden, die im Mergemodul angegeben sind.
-   Nachdem ein Benutzer dem Konfigurationstool bestimmte Auswahlmöglichkeiten erteilt hat, ruft das Mergetool Mergemod.dll auf, um die Zusammenführung durchzuführen.

 

 



