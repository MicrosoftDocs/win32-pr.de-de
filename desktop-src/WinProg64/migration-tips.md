---
title: Tipps zur Migration
description: Es ist wichtig, adressbasierte Berechnungen und Zeigerarithmetik zu berücksichtigen, wenn Sie Ihren Code in 64-Bit-Windows.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- 64-Bit-Windows 64-Bit-Programmierhandbuch Windows Programmierung, Tipps zur Migration
- Tipps zur Migration von 64-Bit-Windows Programmierung
- Kompatibilität mit 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee1480bec99bdc3b620d5d349343330aa3c34121ff697d5e8b15497c72baedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743595"
---
# <a name="migration-tips"></a>Tipps zur Migration

Die beiden hauptanliegenden Bereiche bei der Untersuchung Ihres Codes auf 64-Bit-Kompatibilität sind:

-   Adressberechnungen
-   Zeigerarithmetik

Aus vielen Gründen haben Entwickler Adressen als **ULONG-Wert** gespeichert. Auf 32-Bit-Windows sind eine Adresse, ein Zeiger und ein **ULONG-Wert** alle 32 Bits lang. Auf 64-Bit-Windows haben eine Adresse und **ein ULONG** jedoch nicht die gleiche Länge. Während ein **ULONG** ein 32-Bit-Wert bleibt, sind alle Zeiger jetzt 64-Bit-Werte.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Allgemeine Portierungsrichtlinien](general-porting-guidelines.md)
-   [Speichern eines 64-Bit-Werts](storing-a-64-bit-value.md)
-   [Häufige Compilerfehler](common-compiler-errors.md)
-   [Weitere Überlegungen](additional-considerations.md)

 

 




