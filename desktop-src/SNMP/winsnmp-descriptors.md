---
title: WinSNMP-Deskriptoren
description: In der WinSNMP-Programmierumgebung ist ein Deskriptor eine der beiden folgenden Strukturen.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875112d8519f93f4b5ae6729401f2689294a84c55dc729f0ffa24d05076e300b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142913"
---
# <a name="winsnmp-descriptors"></a>WinSNMP-Deskriptoren

In der WinSNMP-Programmierumgebung ist ein *Deskriptor* eine der folgenden beiden Strukturen:

-   Eine [**smiOCTETS-Struktur,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) die eine Oktettzeichenfolgenvariable beschreibt
-   Eine [**SmiOID-Struktur,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) die eine SNMP-Objektbezeichnervariable beschreibt

Ein WinSNMP-Deskriptor ist eine Struktur mit zwei Membern: einem Längenmember, **len** und einem **Zeigermember, ptr.** Der **ptr-Member** zeigt auf die Oktettzeichenfolge oder den Objektbezeichner, der von Interesse ist. Der **ptr-Member** kann entweder der Datentyp **smiLPBYTE** oder **smiLPUINT32** sein.

Ein [**smiOCTETS-Deskriptor**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) oder ein [**smiOID-Deskriptor**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) kann der **Wertmember** einer **smiVALUE-Struktur** sein. Die [**smiVALUE-Struktur**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) beschreibt den Wert, der einem Variablennamen in einem Variablenbindungseintrag zugeordnet ist.

Die Microsoft WinSNMP-Implementierung ordnet Arbeitsspeicher für alle **SmiOCTETS-** und **smiOID-Ausgabestrukturen** zu und hebt deren Zuordnung auf. Daher muss die Anwendung die [**SnmpFreeDescriptor-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) aufrufen, um den Arbeitsspeicher für den **ptr-Member** dieser Strukturen freizugeben.

Zeichenfolgenmember in Deskriptoren erfordern kein **abschließendes NULL-Byte.** Weitere Informationen zum Verwalten des Speichers, der deskriptoren zugeordnet ist, finden Sie unter [Zuordnen von WinSNMP-Speicherobjekten.](allocating-winsnmp-memory-objects.md)

 

 




