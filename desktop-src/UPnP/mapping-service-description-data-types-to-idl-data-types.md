---
title: Zuordnen von Dienstbeschreibungsdatentypen zu IDL-Datentypen
description: Die folgende Tabelle zeigt die Zuordnung der in einer Dienstbeschreibung angegebenen XML-Datentypen zu den entsprechenden in IDL verwendeten Datentypen.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a34a5ec9ee092091dc00c7cc420b4474a38d8cba0d41c2691943c7dcd5b35e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347630"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a>Zuordnen von Dienstbeschreibungsdatentypen zu IDL-Datentypen

Die folgende Tabelle zeigt die Zuordnung der in einer Dienstbeschreibung angegebenen XML-Datentypen zu den entsprechenden in IDL verwendeten Datentypen.



| XML-Datentyp | IDL-Datentyp  |
|---------------|----------------|
| bin.base64    | SAFEARRAY      |
| bin.hex       | SAFEARRAY      |
| boolean       | VARIANT \_ BOOL  |
| char          | wchar \_ t       |
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
| UUID          | BSTR           |



 

 

 




