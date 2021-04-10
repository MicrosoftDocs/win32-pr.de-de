---
description: Das POSIX-Subsystem muss jede beliebige Sicherheits-ID (SID), die er trifft, in einen 32-Bit-Wert übersetzen können, der als POSIX-ID bezeichnet wird.
ms.assetid: cd6c89ef-c3f1-47fe-8183-320b5d24b0dd
title: Mapping von POSIX-bezeichlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabb944b543fba65942eb89d526590a5aff2c26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867635"
---
# <a name="mapping-posix-identifiers"></a>Mapping von POSIX-bezeichlern

Das POSIX-Subsystem muss jede beliebige [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID), die er trifft, in einen 32-Bit-Wert übersetzen können, der als *POSIX-ID* bezeichnet wird. Außerdem muss Sie in der Lage sein, die ID als Benutzer-ID oder Gruppen-ID zu kategorisieren. Um zu verstehen, wie diese Zuordnung erreicht wird, sehen wir uns zunächst die SIDs an, die zugeordnet werden müssen.

SIDs verfügen über zwei Komponenten: die SID der Domäne und die relative ID des Kontos in der Domäne. Beispielsweise ist in der SID S-1-518364-21-43-8, die letzte Zahl 8, das relative ID (RID) des Kontos und S-1-518364-21-43 die SID der Domäne.

Domänen Informationen werden in " [**Treuhänder Domain**](trusteddomain-object.md) "-Objekten gespeichert. Ein Teil der in einem **Treuhänder Domain** -Objekt gespeicherten Informationen ist ein POSIX-ID-Offset, der für SIDs innerhalb dieser Domäne verwendet werden soll. Nehmen Sie beispielsweise an, dass eine " **Treuhänder Domain** " wie folgt definiert ist:

``` syntax
    Name:    NtPgm
    Sid:    S-1-518364-21-43
    Posix Offset:    0x130000
```

POSIX-IDs für Konten in dieser Domäne werden generiert, indem dem relative ID des Kontos 0x130000 hinzugefügt wird. Die POSIX-ID, die der SID S-1-518364-21-43-8 entspricht, wäre also 0x130008.

Nicht alle POSIX-ID-Übersetzungen verwenden ein " [**Treuhänder-Domain**](trusteddomain-object.md) "-Objekt. In der folgenden Tabelle werden SIDs angezeigt, die mit bekannten Offset Werten zugeordnet sind.



| `Source`                                              | POSIX-ID-Offset |
|-----------------------------------------------------|-----------------|
| SIDs aus der integrierten Domäne                       | 0x20000         |
| SIDs aus der Konto Domäne                        | 0x30000         |
| SIDs aus der primären Domäne (nur auf Arbeitsstationen) | 0x40000         |



 

Und schließlich ist für eine andere Gruppe von SIDs, Anmelde-SIDs, eine spezielle Verarbeitung erforderlich. Diese Werte werden vom Windows-Anmeldevorgang für jede Anmelde Sitzung zugewiesen und verfügen über die Form S-1-5-5-X-Y, wobei X und Y als eine einzelne große Ganzzahl behandelt werden, \_ die für jede Anmelde Sitzung inkrementiert wird. Diese SIDs werden der Konstanten POSIX-ID 0xfff zugeordnet. Um die POSIX-ID 0xfff zuzuordnen, können Sie einen beliebigen [*Anmelde Bezeichner*](/windows/desktop/SecGloss/l-gly) übersetzen, der sich am besten für die Situation eignet, oder Sie können S-1-5-5-0-0 standardmäßig verwenden. (Wenn ein POSIX-Benutzer z. b. den Schutz auf ein Objekt anwendet und fffx angibt, ist es besser, den Anmelde Bezeichner dieses Benutzers zu ersetzen, als nur "s-1-5-5-0-0" zuzuweisen.)

 

 
