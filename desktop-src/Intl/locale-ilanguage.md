---
description: Gebiets Schema- \_ iLanguage
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346266"
---
# <a name="locale_ilanguage"></a>Gebiets Schema- \_ iLanguage

Der [Sprachen Bezeichner](language-identifiers.md) mit einem hexadezimalen Wert. Beispielsweise hat Englisch (USA) den Wert 0409, der 0x0409 hexadezimal angibt und 1033 Decimal entspricht. Die maximal zulässige Anzahl von Zeichen für diese Zeichenfolge ist fünf, einschließlich eines abschließenden NULL-Zeichens.

**Windows Vista und höher:** Die Verwendung dieser Konstante kann bewirken, dass [**getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) einen ungültigen Gebiets Schema Bezeichner zurückgibt. Die Anwendung sollte beim Aufrufen dieser Funktion die [ \_ sname](locale-sname.md) -Konstante für das Gebiets Schema verwenden.

 

 



