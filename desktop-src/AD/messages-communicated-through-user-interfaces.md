---
title: Über Benutzeroberflächen übermittelte Nachrichten
description: In diesem Thema werden die Nachrichten aufgelistet, die von einem Verzeichnisdienst von einer Benutzeroberfläche gesendet werden können.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Über Benutzeroberflächen übermittelte Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036356"
---
# <a name="messages-communicated-through-user-interfaces"></a>Über Benutzeroberflächen übermittelte Nachrichten

In diesem Thema werden die Nachrichten aufgelistet, die von einem Verzeichnisdienst von einer Benutzeroberfläche gesendet werden können.

## <a name="common-query-page-messages"></a>Allgemeine Meldungen der Abfrage Seite

Die folgenden Meldungen werden an eine Seite der Verzeichnisdienst-Abfrageformular Erweiterung in der [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion gesendet:

-   [**cqpm- \_ ClearForm**](cqpm-clearform.md)
-   [**cqpm \_ aktivieren**](cqpm-enable.md)
-   [**cqpm \_ GetParameters**](cqpm-getparameters.md)
-   [**cqpm \_ handlerspecific**](cqpm-handlerspecific.md)
-   [**cqpm- \_ Hilfe**](cqpm-help.md)
-   [**cqpm \_ initialisieren**](cqpm-initialize.md)
-   [**cqpm \_ persistent speichern**](cqpm-persist.md)
-   [**cqpm- \_ Version**](cqpm-release.md)
-   [**cqpm \_ setdefaultparameters**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Verschiedene Nachrichten

In der folgenden Tabelle werden die Nachrichten aufgelistet, die ein Verzeichnisdienst senden kann.



| `Message`                  | Wert                     | BESCHREIBUNG                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dsprop \_ attrchanged-Meldung \_ | "Dspropattrchanged"       | Eine Meldung, die zum Synchronisieren von Eigenschaften Seiten und der Verzeichnisdienst-Verwaltungs Tools gesendet wurde, die in "DSClient. h" deklariert sind.                                                                                                                       |
| dsqpm \_ getclasslist      | Cqpm \_ handlerspecific + 0   | Eine Seiten Nachricht, die an die Formular Seiten zum Abrufen einer Liste von Klassen für die Abfrage gesendet wird, die von der Feldauswahl und der Eigenschaften Quelle verwendet werden, um die Liste der Anzeige Klassen zu erstellen. wParam = Flags und lParam = lplpdsqueryclasslist, deklariert in "dsquery. h". |
| Hilfe Themen zu dsqpm \_        | (Cqpm \_ Handlerspecific + 1) | Eine Seiten Nachricht, die an die Formular Seiten zur Bearbeitung der "Hilfe Themen"-Anforderung gesendet wird. wParam = 0, LPARAM = hwndParent, deklariert in "dsquery. h".                                                                                                         |



 

 

 




