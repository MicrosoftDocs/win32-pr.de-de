---
description: Veranschaulicht den Aufruf eines DDE-Befehls mithilfe eines shellverbs.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Zuordnen von Verben zu DDE-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979608"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a>Zuordnen von Verben zu DDE-Befehlen

Wenn Sie ein Verb aufrufen, wird normalerweise die Anwendung gestartet, die durch den Befehls Unterschlüssel des Verbs angegeben wird. Wenn Ihre Anwendung jedoch dynamischer Datenaustausch (DDE) unterstützt, kann die Shell stattdessen eine DDE-Konversation initiieren.

Führen Sie die folgenden Schritte aus, um anzugeben, dass das Aufrufen eines Verbs eine DDE-Konversation initiieren soll.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Fügen Sie dem Schlüssel des Verbs einen **DDE Exec** -Unterschlüssel hinzu.

### <a name="step-2"></a>Schritt 2:

Legen Sie den Standardwert von **DDE Exec** auf die DDE-Befehls Zeichenfolge fest.

## <a name="remarks"></a>Bemerkungen

Der **ddeexec** -Schlüssel verfügt über drei optionale Unterschlüssel, die eine gewisse Kontrolle über den DDE-Prozess bieten:

-   **Anwendung**: Legen Sie den Standardwert dieses unter Schlüssels auf den Anwendungsnamen fest, der zum Einrichten der DDE-Konversation verwendet werden soll. Wenn kein **Anwendungs** Unterschlüssel vorhanden ist, wird der Standardwert des **Befehls** unter Schlüssels des Verbs als Anwendungsname verwendet.
-   **Thema**. Legen Sie den Standardwert dieses unter Schlüssels auf den Themen Namen der DDE-Konversation fest. Wenn kein **Themen** Unterschlüssel vorhanden ist, wird System als Themenname verwendet.
-   **ifexec**. Legen Sie den Standardwert dieses unter Schlüssels auf den DDE-Befehl fest, der verwendet werden soll, wenn DDE Conversation nicht initiiert werden kann. Wenn die Initiierung fehlschlägt, wird die Anwendung gestartet, die durch den Standardwert des **Befehls** unter Schlüssels des Verbs angegeben wird. Wenn ein **ifexec** -Schlüssel vorhanden ist, wird sein Standardwert als DDE-Befehl verwendet. Wenn kein **ifexec** -Unterschlüssel vorhanden ist, wird der Standardwert des **DDE Exec** -Schlüssels erneut als DDE-Befehl verwendet.

Im folgenden Beispiel wird angegeben, dass beim Aufrufen des geöffneten Verbs für "MyProgram. 1" eine DDE-Konversation mit dem Befehl "DDE" ("%1") und dem Anwendungsnamen "myprogram" initiiert wird.

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



