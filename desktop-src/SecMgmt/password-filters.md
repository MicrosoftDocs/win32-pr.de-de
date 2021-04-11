---
description: Kenn Wortfilter
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Kenn Wortfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218178"
---
# <a name="password-filters"></a>Kenn Wortfilter

Kenn Wortfilter bieten Ihnen die Möglichkeit, Kenn Wort Richtlinien und Änderungs Benachrichtigungen zu implementieren.

Wenn ein Kennwort Change Request erfolgt, ruft die [*Lokale Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) die auf dem System registrierten Kenn Wortfilter auf. Jeder Kenn Wortfilter wird zweimal aufgerufen: zuerst zum Überprüfen des neuen Kennworts und dann, nachdem alle Filter das neue Kennwort überprüft haben, um die Filter zu benachrichtigen, dass die Änderung vorgenommen wurde. Die folgende Abbildung veranschaulicht diesen Prozess.

![Kennwort Change Request](images/pswdfilte.png)

Benachrichtigung über Kenn Wort Änderung wird zum Synchronisieren von Kenn Wort Änderungen an fremd Konto Datenbanken verwendet.

Kenn Wortfilter werden verwendet, um die Kenn Wort Richtlinie zu erzwingen. Filter überprüfen neue Kenn Wörter und geben an, ob das neue Kennwort der implementierten Kenn Wort Richtlinie entspricht.

Eine Übersicht über die Verwendung von Kenn Wort Filtern finden Sie unter Verwenden von Kenn [Wort Filtern](using-password-filters.md).

Eine Liste der Kenn Wortfilter Funktionen finden Sie unter Kenn [Wortfilter Funktionen](management-functions.md).

Die folgenden Themen enthalten weitere Informationen zu Kenn Wort filtern:

-   [Überlegungen zur Kenn Wort Filter Programmierung](password-filter-programming-considerations.md)
-   [Starke Kenn Wort Erzwingung und Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
