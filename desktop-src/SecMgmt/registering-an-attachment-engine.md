---
description: Bevor die Sicherheitskonfigurations-Engine die Anlagen-Engine zum Verarbeiten Dienst spezifischer Aufgaben aufruft, müssen Sie die Anlagen-Engine installieren und bei der Sicherheitskonfigurations-Engine registrieren.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrieren einer Anlage-Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347135"
---
# <a name="registering-an-attachment-engine"></a>Registrieren einer Anlage-Engine

Bevor die Sicherheitskonfigurations-Engine die Anlagen-Engine zum Verarbeiten Dienst spezifischer Aufgaben aufruft, müssen Sie die Anlagen-Engine installieren und bei der Sicherheitskonfigurations-Engine registrieren.

**So installieren und registrieren Sie die Anlage-Engine-dll**

1.  Kopieren Sie die Anlage-Engine-dll in ein Verzeichnis auf dem System. Das bevorzugte Verzeichnis ist% windir% \\ secedit- \\ Anlagen. Wenn dieses Verzeichnis nicht vorhanden ist, sollten Sie es erstellen.
2.  Erstellen Sie unter dem folgenden Knoten einen Registrierungsschlüssel. Der *Dienst Name* ist der registrierte Name für die Anlage. er muss dem Dienstnamen entsprechen, der im Dienststeuerungs-Manager verwendet wird. dabei handelt es sich um ein Modul, das das Beenden und starten von Diensten verwaltet. Der Name muss auch eindeutig sein, sodass er nicht mit den Namen anderer Anhänge in Konflikt steht.

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  Erstellen Sie den folgenden Zeichen folgen Wert im neuen Registrierungsschlüssel. der *Pfad der Anlage-Engine* ist der vollständige Pfad zum Anlage-Engine-Modul.<dl> <dd>**Serviceattachmentpath**  =  *Pfad der Anlage-Engine*<dl> <dt>

Datentyp
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



