---
title: ADSI-Eigenschaften und-Attribute
description: Attribute werden manchmal auch als Eigenschaften bezeichnet. Dies kann Verwirrung verursachen. In dieser Dokumentation werden die folgenden Definitionen für Eigenschaften und Attribute verwendet.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- ADSI-Eigenschaften und-Attribute ADSI
- ADSI ADSI, verwenden, zugreifen auf und Bearbeiten von Daten, Eigenschaften und Attributen
- Eigenschaften ADSI
- Attribute ADSI
- Eigenschaften ADSI, definiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338564"
---
# <a name="adsi-properties-and-attributes"></a>ADSI-Eigenschaften und-Attribute

Attribute werden manchmal auch als Eigenschaften bezeichnet. Dies kann Verwirrung verursachen. In dieser Dokumentation werden die folgenden Definitionen für Eigenschaften und Attribute verwendet.

Eigenschaften sind benannte Werte, die einem Programmier Objekt zugeordnet sind. Beispielsweise macht die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle Eigenschaften wie z. b. [**Klasse**](iads-property-methods.md) und **Name** verfügbar.

Attribute sind die Daten, die Objekten in einem Verzeichnisdienst zugeordnet sind. Beispielsweise verfügt ein Benutzerobjekt über ein Attribut namens **CN** , das eine Zeichenfolge mit dem allgemeinen oder relativen Distinguished Name des Objekts enthält. Auf Attribute kann über Methoden der ADSI-Schnittstelle wie [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put)zugegriffen werden.

Weitere Informationen zu Eigenschaften und Attributen von ADSI finden Sie unter:

-   [Der ADSI-Attribut Cache](the-adsi-attribute-cache.md)
-   [Einzelne Attribute und Attribute mit mehreren Werten](single-vs--multiple-value-attributes.md)
-   [Active Directory von Betriebs Attributen](active-directory-operational-attributes.md)

 

 




