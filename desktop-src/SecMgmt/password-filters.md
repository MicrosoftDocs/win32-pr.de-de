---
description: Kennwortfilter
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Kennwortfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5771fce0e8cbb2826bcf79344e2813587db6dcedc831d7e879b42ab74698b9a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894001"
---
# <a name="password-filters"></a>Kennwortfilter

Kennwortfilter bieten Ihnen die Möglichkeit, Kennwortrichtlinien und Änderungsbenachrichtigungen zu implementieren.

Wenn eine Kennwortänderungsanforderung erfolgt, ruft die lokale Sicherheitsstelle [*(Local Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) die im System registrierten Kennwortfilter auf. Jeder Kennwortfilter wird zweimal aufgerufen: zuerst, um das neue Kennwort zu überprüfen, und dann, nachdem alle Filter das neue Kennwort überprüft haben, um die Filter darüber zu benachrichtigen, dass die Änderung vorgenommen wurde. Die folgende Abbildung veranschaulicht diesen Prozess.

![Kennwortänderungsanforderung](images/pswdfilte.png)

Kennwortänderungsbenachrichtigungen werden verwendet, um Kennwortänderungen mit Fremdkontodatenbanken zu synchronisieren.

Kennwortfilter werden verwendet, um Kennwortrichtlinien zu erzwingen. Filter überprüfen neue Kennwörter und geben an, ob das neue Kennwort der implementierten Kennwortrichtlinie entspricht.

Eine Übersicht über die Verwendung von Kennwortfiltern finden Sie unter [Verwenden von Kennwortfiltern.](using-password-filters.md)

Eine Liste der Kennwortfilterfunktionen finden Sie unter [Kennwortfilterfunktionen](management-functions.md).

Die folgenden Themen enthalten weitere Informationen zu Kennwortfiltern:

-   [Überlegungen zur Programmierung von Kennwortfiltern](password-filter-programming-considerations.md)
-   [Erzwingung und Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
