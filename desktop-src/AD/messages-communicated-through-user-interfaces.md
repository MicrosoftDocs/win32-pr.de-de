---
title: Über Benutzeroberflächen kommunizierte Nachrichten
description: In diesem Thema werden Meldungen aufgeführt, die ein Verzeichnisdienst über eine Benutzeroberfläche senden kann.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Über Benutzeroberflächen kommunizierte Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20b2706ae9f03109064c459ce494fb38da3f4579ca8f5b03ade970fcb0391f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186572"
---
# <a name="messages-communicated-through-user-interfaces"></a>Über Benutzeroberflächen kommunizierte Nachrichten

In diesem Thema werden Meldungen aufgeführt, die ein Verzeichnisdienst über eine Benutzeroberfläche senden kann.

## <a name="common-query-page-messages"></a>Allgemeine Meldungen zu Abfrageseiten

Die folgenden Meldungen werden in der [**CQPageProc-Rückruffunktion**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) an eine Seite für eine Verzeichnisdienstabfrageformularerweiterung gesendet:

-   [**CQPM \_ CLEARFORM**](cqpm-clearform.md)
-   [**CQPM \_ ENABLE**](cqpm-enable.md)
-   [**CQPM \_ GETPARAMETERS**](cqpm-getparameters.md)
-   [**CQPM \_ HANDLERSPECIFIC**](cqpm-handlerspecific.md)
-   [**CQPM-HILFE \_**](cqpm-help.md)
-   [**CQPM \_ INITIALIZE**](cqpm-initialize.md)
-   [**CQPM \_ PERSIST**](cqpm-persist.md)
-   [**CQPM-RELEASE \_**](cqpm-release.md)
-   [**CQPM \_ SETDEFAULTPARAMETERS**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Sonstige Meldungen

Die folgende Tabelle enthält Meldungen, die ein Verzeichnisdienst senden kann.



| `Message`                  | Wert                     | BESCHREIBUNG                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPROP \_ ATTRCHANGED \_ MSG | "DsPropAttrChanged"       | Eine Meldung, die zum Synchronisieren von Eigenschaftenseiten und der Verzeichnisdienst-Verwaltungstools gesendet wird, deklariert in Dsclient.h.                                                                                                                       |
| DSQPM \_ GETCLASSLIST      | CQPM \_ HANDLERSPECIFIC+0   | Eine An die Formularseiten gesendete Seitennachricht zum Abrufen einer Liste von Klassen für die Abfrage, die vom Feldauswahl- und Eigenschaftenbereich zum Erstellen der Liste der Anzeigeklassen verwendet wird. wParam = flags und lParam = LPLPDSQUERYCLASSLIST, deklariert in Dsquery.h. |
| DSQPM \_ HELPTOPICS        | (CQPM \_ HANDLERSPECIFIC+1) | Eine Seitennachricht, die an die Formularseiten gesendet wird, um die Anforderung "Hilfethemen" zu behandeln. wParam = 0, lParam = hWndParent, deklariert in Dsquery.h.                                                                                                         |



 

 

 




