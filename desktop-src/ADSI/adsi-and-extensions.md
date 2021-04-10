---
title: Integration von Erweiterungen durch ADSI
description: Richtlinien, die beschreiben, wie ADSI mit Erweiterungen interagiert.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI
- ADSI und Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039603"
---
# <a name="how-adsi-integrates-extensions"></a>Integration von Erweiterungen durch ADSI

In den folgenden Richtlinien wird beschrieben, wie ADSI mit Erweiterungen interagiert:

-   Etwas wird an ein ADSI-Verzeichnis Objekt gebunden. Beispiel: "LDAP://CN = JeffSmith, OU = Sales, DC = fabrikam, DC = com".
-   ADSI identifiziert, dass das Objekt in der **User** -Klasse vorhanden ist.
-   ADSI führt eine Suche in der Registrierung durch und identifiziert die Erweiterungs-CLSIDs für den **Benutzer**. Beachten Sie, dass ADSI diese Daten zwischenspeichert.
-   Die **QueryInterface** -Methode wird für IID \_ imyextension aufgerufen. ADSI durchsucht die Schnittstellen, die dem **User** -Objekt zugeordnet sind, beginnend mit seinen eigenen Schnittstellen und untersucht dann Erweiterungs Schnittstellen.
-   Wenn eine Entsprechung gefunden wird, erstellt ADSI eine Instanz der Komponente, die IID \_ imyextension unterstützt, und ruft **QueryInterface** für die Erweiterung auf. Die resultierende Schnittstelle wird zurückgegeben.
-   Der Benutzer verwendet diese Schnittstelle, um die Schnittstellen Methoden aufzurufen.
-   Als Nächstes ruft der Client **QueryInterface** für IID \_ iyourextension auf, die sich in einer anderen Komponente befindet. Diese Komponente delegiert diesen **QueryInterface** -Aufrufe an die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Aggregators, bei der es sich um ADSI selbst handelt.
-   Erneut durchsucht ADSI die Schnittstellen und erstellt die Komponenteninstanz.

 

 