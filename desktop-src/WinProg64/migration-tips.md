---
title: Tipps zur Migration
description: Es ist wichtig, Adress Berechnungen und Zeigerarithmetik zu berücksichtigen, wenn Sie Ihren Code auf 64-Bit-Fenster portieren.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Tipps zur Migration
- Migrations Tipps 64-Bit-Windows-Programmierung
- Kompatibilität 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711711"
---
# <a name="migration-tips"></a>Tipps zur Migration

Bei der Untersuchung des Codes für die 64-Bit-Kompatibilität sind die folgenden beiden Hauptbereiche von Bedeutung:

-   Adress Berechnungen
-   Zeigerarithmetik

Aus vielen Gründen haben Entwickler Adressen als **ulong** -Wert gespeichert. Schließlich sind auf 32-Bit-Fenstern eine Adresse, ein Zeiger und ein **ulong** -Wert alle 32 Bits lang. Bei 64-Bit-Fenstern weisen jedoch eine Adresse und ein **ulong** nicht die gleiche Länge auf. Während ein **ulong** -Wert ein 32-Bit-Wert ist, sind alle Zeiger jetzt 64-Bit-Werte.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Allgemeine Richtlinien für die Portierung](general-porting-guidelines.md)
-   [Speichern eines 64-Bit-Werts](storing-a-64-bit-value.md)
-   [Häufige Compilerfehler](common-compiler-errors.md)
-   [Weitere Überlegungen](additional-considerations.md)

 

 




