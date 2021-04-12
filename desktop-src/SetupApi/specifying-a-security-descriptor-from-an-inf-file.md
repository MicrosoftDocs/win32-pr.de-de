---
description: Sie können die Fähigkeit eines Prozesses steuern, auf Sicherungs fähige Objekte zuzugreifen oder Systemverwaltungsaufgaben auszuführen.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Angeben einer Sicherheits Beschreibung aus einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960748"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Angeben einer Sicherheits Beschreibung aus einer INF-Datei

Sie können die Fähigkeit eines Prozesses steuern, auf Sicherungs fähige Objekte zuzugreifen oder Systemverwaltungsaufgaben auszuführen. Ein Sicherungs fähiges Objekt ist ein Objekt, das über eine Sicherheits Beschreibung verfügen kann. Alle benannten Objekte sind Sicherungs fähig. Einige unbenannte Objekte (z. b. Prozess-und Thread Objekte) können auch Sicherheits Deskriptoren aufweisen. Weitere Informationen zum Steuern des Zugriffs auf Sicherungs fähige Objekte finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

[Sicherheits Deskriptoren](/windows/desktop/SecAuthZ/security-descriptors) enthalten die Sicherheitsinformationen, die Sicherungs fähigen Objekten zugeordnet sind. Bei den meisten Sicherungs fähigen Objekten können Sie die Sicherheits Beschreibung eines Objekts im Funktionsaufruf angeben, von dem das Objekt erstellt wird. Sie können z. b. eine Sicherheits Beschreibung [**in den Funktionen**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "up" und " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " angeben.

Um eine Sicherheits Beschreibung aus einer INF-Datei festzulegen, fügen Sie einen von INF-Writer erstellten Sicherheitsabschnitt direkt nach dem Abschnitt hinzu, der die Datei, den Registrierungsschlüssel oder die Komponente installiert. Der Abschnitt Security sollte eine Zeile mit der Zeichen folgen-Sicherheits Beschreibung enthalten, die das Format für [sicherheitsbeschreibungerzeichenfolgen](/windows/desktop/SecAuthZ/security-descriptor-strings)enthält. Die Zeile sollte auch in Anführungszeichen (") eingeschlossen werden.

Beispielsweise würde der folgende INF-Datei Ausschnitt einen Registrierungsschlüssel erstellen, auf den nur Administratoren und das System zugreifen können. Beachten Sie, dass für dieses Beispiel Administratorrechte erforderlich sind.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

In diesem Fall ist die Bedeutung der Zeichenfolge, dass Administratoren über Vollzugriff verfügen, das System über Vollzugriff verfügt und der Zugriff auf alle Unterschlüssel vererbt werden kann. Weitere Informationen finden Sie unter [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
