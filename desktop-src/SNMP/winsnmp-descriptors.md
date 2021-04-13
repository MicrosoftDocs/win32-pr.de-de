---
title: WinSNMP-Deskriptoren
description: In der WinSNMP-Programmierumgebung handelt es sich bei einem Deskriptor um eine der beiden folgenden Strukturen.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309443"
---
# <a name="winsnmp-descriptors"></a>WinSNMP-Deskriptoren

In der WinSNMP-Programmierumgebung handelt es sich bei einem *Deskriptor* um eine der folgenden beiden Strukturen:

-   Eine [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Struktur, die eine Oktett-Zeichen folgen Variable beschreibt.
-   Eine [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Struktur, die eine SNMP-objektbezeichnervariable beschreibt.

Ein WinSNMP-Deskriptor ist eine Struktur mit zwei Membern: einem Längen Element, **len** und einem Zeigermember ( **ptr**). Das **ptr** -Element verweist auf die Oktett-Zeichenfolge oder den Objekt Bezeichner von Interesse. Der **ptr** -Member kann entweder der Datentyp " **smilpbyte** " oder " **smiLPUINT32** " sein.

Ein [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Deskriptor oder ein [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Deskriptor kann der **Wertmember** einer **smivalue** -Struktur sein. Die [**smivalue**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) -Struktur beschreibt den Wert, der einem Variablennamen in einem Variablen Bindungs Eintrag zugeordnet ist.

Die Microsoft WinSNMP-Implementierung ordnet Speicher für alle **ausgabesmioctets** und **smioid** -Strukturen zu und hebt deren Zuordnung auf. Daher muss die Anwendung die [**snmpfreedescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) -Funktion aufruft, um den Arbeitsspeicher für den **ptr** -Member dieser Strukturen freizugeben.

Zeichen folgen Elemente in Deskriptoren benötigen kein **null** -terminierendes Byte. Weitere Informationen zum Verwalten des Arbeitsspeichers, der Deskriptoren zugeordnet ist, finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).

 

 




