---
description: Der VM-Speicherplatz auf 32-Bit-Systemen kann aufgrund der Fragmentierung erschöpft werden. Mehrere Registrierungsschlüssel können verwendet werden, um Arbeitsspeicher Limits auf 32-Bit-Systemen zu konfigurieren, bei denen dieses Problem auftritt.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Registrierungsschlüssel für die Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869064"
---
# <a name="memory-management-registry-keys"></a>Registrierungsschlüssel für die Speicherverwaltung

Der VM-Speicherplatz auf 32-Bit-Systemen kann aufgrund der Fragmentierung erschöpft werden. Mehrere Registrierungsschlüssel können verwendet werden, um Arbeitsspeicher Limits auf 32-Bit-Systemen zu konfigurieren, bei denen dieses Problem auftritt. Der System-VA-Speicherplatz auf 64-Bit-Systemen unterliegt nicht der Erschöpfung durch Fragmentierung. Daher haben diese Schlüssel keine Auswirkung auf 64-Bit-Systeme.

Bei 32-Bit-Systemen müssen diese Registrierungsschlüssel für die Speicherverwaltung explizit unter folgendem Registrierungsschlüssel erstellt werden:

**HKEY \_ Lokales \_** \\ **System** \\ steuerungsedienstesteuerungsedienstesteuerungssteuerungs- \\  \\  \\ **Speicherverwaltung**

**Windows Server 2008 und Windows Vista:** Diese Registrierungsschlüssel sind auf 32-Bit-Systemen ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) verfügbar.

Informationen zu den standardmäßigen Arbeitsspeicher-und Adressraum Limits für 32-Bit-und 64-Bit-Systeme finden Sie unter Arbeits [Speicher Grenzwerte für Windows-Versionen](memory-limits-for-windows-releases.md).

In der folgenden Tabelle werden die Registrierungsschlüssel für die Speicherverwaltung beschrieben, die zum Konfigurieren von Arbeitsspeicher Limits auf 32-Bit-Systemen verwendet werden können. Alle diese Schlüssel verfügen über einen reg \_ DWORD-Typ und mögliche Werte, die zwischen 0 und 2.048 MB liegen. Der Standardwert ist 0 (null). Dies bedeutet, dass keine Begrenzung erzwungen wird. Die Werte werden automatisch auf die nächste System-VA-Zuordnungs Grenze aufgerundet. diese ist 2 MB auf 32-Bit-Systemen, die über eine aktivierte [physische Adress Erweiterung](physical-address-extension.md) (PE) und 4 MB auf 32-Bit-Systemen verfügen, für die keine PE aktiviert ist.



| Schlüssel                   | BESCHREIBUNG                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nonteipoollimit** | Gibt die maximale Menge an System-VA-Speicherplatz an, die vom nicht auslagerenden Pool verwendet werden kann. Unter bestimmten Umständen wird dieser Grenzwert möglicherweise um einen kleinen Wert überschritten. |
| **Paar-poollimit**    | Gibt die maximale Menge an System-VA-Speicherplatz an, die vom Auslagerungs Pool verwendet werden kann.                                                                            |
| **Sessionspacelimit** | Gibt die maximale Menge an System-VA-Speicherplatz an, die von Sitzungs Speicher Belegungen verwendet werden kann.                                                                 |
| **Systemcachelimit**  | Gibt die maximale Menge an System-VA-Speicherplatz an, die vom System Cache verwendet werden kann. Unter bestimmten Umständen wird dieser Grenzwert möglicherweise um einen kleinen Wert überschritten.  |
| **Systempteslimit**   | Gibt die maximale Menge an System-VA-Speicherplatz an, der von e/a-Zuordnungen und anderen Ressourcen verwendet werden kann, die Seitentabellen Einträge (PTEs) für das System verwenden.            |



 

Wenn Sie bestimmen, ob der System-VA-Speicherplatz erschöpft ist, müssen Sie einen Kernel Debugger verwenden. Weitere Informationen finden Sie unter [Debugtools für Windows](https://msdn.microsoft.com/library/cc267445.aspx).

 

 



