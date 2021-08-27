---
description: Veranschaulicht das Aufrufen eines DDE-Befehls mithilfe eines Shellverbs.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Zuordnen von Verben zu DDE-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216cfca1548ed16dfea2f018fc3a1607d5c29d080f0f54541ace0491813a73d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090580"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a>Zuordnen von Verben zu DDE-Befehlen

Durch aufrufen eines Verbs wird normalerweise die Anwendung gestartet, die durch den Befehlsunterschlüssel des Verbs angegeben wird. Wenn Ihre Anwendung jedoch dynamische Daten Exchange (DDE) unterstützt, können Sie stattdessen von der Shell eine DDE-Konversation initiieren lassen.

Um anzugeben, dass das Aufrufen eines Verbs eine DDE-Konversation initiieren soll, führen Sie die folgenden Schritte aus.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Fügen Sie dem Schlüssel des Verbs einen **ddeexec-Unterschlüssel** hinzu.

### <a name="step-2"></a>Schritt 2:

Legen Sie den Standardwert **von ddeexec auf** die DDE-Befehlszeichenfolge fest.

## <a name="remarks"></a>Hinweise

Der **ddeexec-Schlüssel** verfügt über drei optionale Unterschlüssel, die eine gewisse Kontrolle über den DDE-Prozess bieten:

-   **anwendung**. Legen Sie den Standardwert dieses Unterschlüssels auf den Anwendungsnamen fest, der zum Einrichten der DDE-Konversation verwendet werden soll. Wenn kein **Anwendungsunterschlüssel** angegeben ist, wird der  Standardwert des Befehlsunterschlüssels des Verbs als Anwendungsname verwendet.
-   **Thema**. Legen Sie den Standardwert dieses Unterschlüssels auf den Themennamen der DDE-Konversation fest. Wenn kein **Themenunterschlüssel** vor liegt, wird System als Themenname verwendet.
-   **ifexec**. Legen Sie den Standardwert dieses Unterschlüssels auf den DDE-Befehl fest, der verwendet werden soll, wenn die DDE-Konversation nicht initiiert werden kann. Wenn die Initiierung fehlschlägt, wird die Anwendung  gestartet, die durch den Standardwert des Befehlsunterschlüssels des Verbs angegeben wird. Wenn ein **ifexec-Schlüssel** vorhanden ist, wird sein Standardwert als DDE-Befehl verwendet. Wenn kein **ifexec-Unterschlüssel** angegeben ist, wird der Standardwert des **ddeexec-Schlüssels** erneut als DDE-Befehl verwendet.

Im folgenden Beispiel wird angegeben, dass beim Aufrufen des offenen Verbs für MyProgram.1 eine DDE-Konversation mit dem DDE-Befehl Open("%1") und dem Anwendungsnamen MyProgram initiiert wird.

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

 

 



