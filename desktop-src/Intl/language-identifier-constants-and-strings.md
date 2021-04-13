---
description: Jeder sprach Bezeichner besteht aus einer primär Sprachen-ID, die die Sprache angibt, und einer unter Sprachen-ID, die das Land bzw. die Region angibt.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Sprach Bezeichner-Konstanten und Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346039"
---
# <a name="language-identifier-constants-and-strings"></a>Sprach Bezeichner-Konstanten und Zeichen folgen

> [!IMPORTANT]
> Sprach Bezeichner-Konstanten sind veraltet, und ihre Verwendung ist nicht empfehlenswert. Die Verwendung von Gebiets Schema Namen anstelle von Gebiets Schema bezeichnermerkmalen ist immer vorzuziehen.

Eine Beschreibung von Sprach [Bezeichnern](language-identifiers.md) finden Sie unter Sprach-ID.

Ein primärer oder unter Sprachen Bezeichner kann Benutzer definiert oder vordefiniert sein. Informationen zu den vordefinierten primär Sprachen Bezeichnern mit Ihren gültigen unter Sprachen Bezeichnern finden Sie unter [[MS-LCID]: Referenz zur Windows-Sprach Code-ID (LCID)](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).

> [!Note]  
> Wenn keine unter Sprachen-ID vorhanden ist, die mit einer primär Sprachen-ID verwendet werden kann, sollte die Anwendung den **\_ Standardwert von sublang** verwenden. Es sollte für Ressourcen, die für alle unter Sprachen einer Primärsprache identisch sind, die **Unterklasse \_** "lang" verwenden.

Ein benutzerdefinierter primärer sprach Bezeichner weist einen Wert im Bereich von 0x0200 bis 0x03ff auf. Alle anderen Werte sind für die Verwendung durch das Betriebssystem reserviert.

Ein benutzerdefinierter unter Sprachen Bezeichner weist einen Wert im Bereich von 0x20 bis 0x3f auf. Alle anderen Werte sind für die Verwendung durch das Betriebssystem reserviert.
