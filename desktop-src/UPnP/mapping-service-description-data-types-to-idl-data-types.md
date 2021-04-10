---
title: Zuordnung von Dienst Beschreibungs Datentypen zu IDL-Datentypen
description: Die folgende Tabelle zeigt die Zuordnung der in einer Dienst Beschreibung angegebenen XML-Datentypen zu den entsprechenden Datentypen, die in IDL verwendet werden.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037425"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a>Zuordnung von Dienst Beschreibungs Datentypen zu IDL-Datentypen

Die folgende Tabelle zeigt die Zuordnung der in einer Dienst Beschreibung angegebenen XML-Datentypen zu den entsprechenden Datentypen, die in IDL verwendet werden.



| XML-Datentyp | IDL-Datentyp  |
|---------------|----------------|
| bin.base64    | SAFEARRAY      |
| bin.hex       | SAFEARRAY      |
| boolean       | Variant \_ bool  |
| char          | WCHAR \_ t       |
| date          | DATE           |
| dateTime      | DATE           |
| dateTime.tz   | DATE           |
| fixed.14.4    | CY             |
| float         | float          |
| i1            | char           |
| i2            | short          |
| i4            | long           |
| INT           | long           |
| number        | BSTR           |
| r4            | float          |
| r8            | double         |
| Zeichenfolge        | BSTR           |
| time          | DATE           |
| time.tz       | DATE           |
| ui1           | unsigned char  |
| ui2           | unsigned short |
| ui4           | unsigned long  |
| uri           | BSTR           |
| uuid          | BSTR           |



 

 

 




