---
description: Sie können die Fähigkeit eines Prozesses steuern, auf sicherungsfähige Objekte zu zugreifen oder Systemverwaltungsaufgaben auszuführen.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Angeben eines Sicherheitsdeskriptors aus einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52267f443bf20fe8a9b71a64e2422ac43688d7a54bca2692f1b61ad891fda8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964836"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Angeben eines Sicherheitsdeskriptors aus einer INF-Datei

Sie können die Fähigkeit eines Prozesses steuern, auf sicherungsfähige Objekte zu zugreifen oder Systemverwaltungsaufgaben auszuführen. Ein sicherungsfähiges Objekt ist ein Objekt, das über einen Sicherheitsdeskriptor verfügen kann. Alle benannten Objekte sind sicherungsfähig. Einige unbenannte Objekte, z. B. Prozess- und Threadobjekte, können auch Sicherheitsdeskriptoren aufweisen. Weitere Informationen zum Steuern des Zugriffs auf sicherungsfähige Objekte finden Sie [unter Access Control](/windows/desktop/SecAuthZ/access-control).

[Sicherheitsdeskriptoren](/windows/desktop/SecAuthZ/security-descriptors) enthalten die Sicherheitsinformationen, die sicherungsfähige Objekte zugeordnet sind. Für die meisten sicherungsfähige Objekte können Sie den Sicherheitsdeskriptor eines Objekts im Funktionsaufruf angeben, der das Objekt erstellt. Beispielsweise können Sie einen Sicherheitsdeskriptor in den [**Funktionen CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) und [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) angeben.

Wenn Sie einen Sicherheitsdeskriptor aus einer INF-Datei festlegen möchten, fügen Sie unmittelbar nach dem Abschnitt, in dem die Datei, der Registrierungsschlüssel oder die Komponente installiert wird, einen vom INF Writer geschriebenen Abschnitt Sicherheit hinzu. Der Abschnitt Sicherheit sollte eine Zeile mit der darauf geschriebenen Zeichenfolgensicherheitsbeschreibung enthalten, die das Format für [Sicherheitsbeschreibungszeichenfolgen verwendet.](/windows/desktop/SecAuthZ/security-descriptor-strings) Die Zeile sollte auch in Anführungszeichen () eingeschlossen werden.

Der folgende INF-Dateiausschnitt würde beispielsweise einen Registrierungsschlüssel erstellen, auf den nur Administratoren und das System Zugriff haben. Beachten Sie, dass für dieses Beispiel Administratorrechte erforderlich sind.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

In diesem Fall hat die Zeichenfolge die Bedeutung, dass Administratoren Vollzugriff haben, das System Vollzugriff hat und der Zugriff für alle Unterschlüssel vererbt werden kann. Weitere Informationen finden Sie unter [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
