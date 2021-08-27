---
description: '\_GEBIETSSCHEMA-ILANGUAGE'
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3159fe26ce1af7291c5990a07297e7513144b5187b55c00086bf46e452ef188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106650"
---
# <a name="locale_ilanguage"></a>\_GEBIETSSCHEMA-ILANGUAGE

[Sprachbezeichner](language-identifiers.md) mit einem Hexadezimalwert. Beispielsweise weist Englisch (USA) den Wert 0409 auf, der 0x0409 hexadezimalen Wert angibt und 1033 dezimal entspricht. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, beträgt fünf, einschließlich eines abschließenden NULL-Zeichens.

**Windows Vista und höher:** Die Verwendung dieser Konstante kann dazu führen, dass [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) einen ungültigen Gebietsschemabezeichner zurückgibt. Ihre Anwendung sollte beim Aufrufen dieser Funktion die [ \_ LOCALE-SNAME-Konstante](locale-sname.md) verwenden.

 

 



