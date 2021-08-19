---
title: ADSI-Eigenschaften und -Attribute
description: Attribute werden manchmal als Eigenschaften bezeichnet. Dies kann zu Verwirrung führen. In dieser Dokumentation werden die folgenden Definitionen für Eigenschaften und Attribute verwendet.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- ADSI-Eigenschaften und -Attribute ADSI
- 'ADSI ADSI : Verwenden, Zugreifen auf und Bearbeiten von Daten, Eigenschaften und Attributen'
- AdsI-Eigenschaften
- Attribute ADSI
- ADSI-Eigenschaften, definiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b05637cada9a62cee129e9645385233b4700cbf2762b9446ba9a871d1897d440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082794"
---
# <a name="adsi-properties-and-attributes"></a>ADSI-Eigenschaften und -Attribute

Attribute werden manchmal als Eigenschaften bezeichnet. Dies kann zu Verwirrung führen. In dieser Dokumentation werden die folgenden Definitionen für Eigenschaften und Attribute verwendet.

Eigenschaften sind benannte Werte, die einem Programmierobjekt zugeordnet sind. Beispielsweise macht die [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) Eigenschaften wie [**Class und**](iads-property-methods.md) **Name verfügbar.**

Attribute sind die Daten, die Objekten in einem Verzeichnisdienst zugeordnet sind. Beispielsweise verfügt ein Benutzerobjekt über ein Attribut namens **cn,** das eine Zeichenfolge enthält, die den allgemeinen oder relativen Distinguished Name des Objekts ist. Auf Attribute kann über ADSI-Schnittstellenmethoden wie [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs.Put zugegriffen werden.**](/windows/desktop/api/Iads/nf-iads-iads-put)

Weitere Informationen zu ADSI-Eigenschaften und -Attributen finden Sie unter:

-   [Der ADSI-Attributcache](the-adsi-attribute-cache.md)
-   [Einzelne oder mehrere Wertattribute](single-vs--multiple-value-attributes.md)
-   [Active Directory-Betriebsattribute](active-directory-operational-attributes.md)

 

 




