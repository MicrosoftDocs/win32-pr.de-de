---
description: Jeder Sprachbezeichner besteht aus einem Bezeichner der primären Sprache, der die Sprache angibt, und einem Untersprachbezeichner, der das Land bzw. die Region angibt.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Sprachbezeichnerkonstatoren und Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67321097d93c5f4224a86a66528f98dacce18312003062665ccc30c1377de70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948747"
---
# <a name="language-identifier-constants-and-strings"></a>Sprachbezeichnerkonstatoren und Zeichenfolgen

> [!IMPORTANT]
> Sprachbezeichnerkonst constants sind veraltet, und ihre Verwendung wird abgeraten. Die Verwendung von Locale Names anstelle von Locale Identifiers ist immer vorzuziehen.

Eine [Beschreibung der Sprachbezeichner](language-identifiers.md) finden Sie unter Sprachbezeichner.

Ein primärer oder untergeordneter Bezeichner kann benutzerdefiniert oder vordefiniert sein. Informationen zu den vordefinierten Bezeichnern der primären Sprache mit ihren gültigen Untergeordneten Sprachbezeichnern finden Sie unter [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f)( Referenz zu .

> [!Note]  
> Wenn es keinen Bezeichner für die Untersprache gibt, der mit einem Bezeichner der primären Sprache verwendet werden kann, sollte Ihre Anwendung **SUBLANG \_ DEFAULT verwenden.** Es sollte **SUBLANG \_ NEUTRAL für** Ressourcen verwenden, die für alle Untersprachen einer primären Sprache identisch sind.

Ein benutzerdefinierter Primärsprachbezeichner verfügt über einen Wert im Bereich, 0x0200 zu 0x03ff. Alle anderen Werte sind für die Verwendung durch das Betriebssystem reserviert.

Ein benutzerdefinierter Untersprachebezeichner verfügt über einen Wert im Bereich, 0x20 zu 0x3f. Alle anderen Werte sind für die Verwendung durch das Betriebssystem reserviert.
