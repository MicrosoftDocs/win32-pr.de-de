---
description: Ein logischer Consumer ist eine Instanz einer permanenten Ereignis-Consumerklasse.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Erstellen eines logischen Consumers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9514ce3f1c7982a96692dcdea62ec9bb92ebf99dd4c47cfe1a64b70257dcfc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030660"
---
# <a name="creating-a-logical-consumer"></a>Erstellen eines logischen Consumers

Ein logischer Consumer ist eine Instanz einer permanenten Ereignis-Consumerklasse. Der Hauptzweck eines logischen Consumers besteht in der Bereitstellung der Parameter für die Aktivitäten, die der physische Consumer ausführt. Weitere Informationen finden Sie unter [Creating a New Permanent Event Consumer Class](creating-a-new-permanent-event-consumer-class.md). Der permanente Consumer muss dieselbe [**CreatorSID**](--eventconsumer.md) in den Consumer-, Filter- und Bindungsinstanzen haben. Weitere Informationen finden Sie unter [Sicheres Empfangen von Ereignissen.](receiving-events-securely.md) Ein Beispiel für die Verwendung eines logischen Consumers finden Sie unter Running a Script Based on an Event (Ausführen eines Skripts basierend auf einem [Ereignis),](running-a-script-based-on-an-event.md)in dem die Verwendung der Standardconsumerklasse [**ActiveScriptEventConsumer**](activescripteventconsumer.md) zum Konfigurieren eines permanenten Consumers veranschaulicht wird.

Im folgenden Verfahren wird beschrieben, wie ein logischer Consumer erstellt wird.

**So erstellen Sie einen logischen Consumer**

1.  Erstellen Sie eine Instanz Ihrer permanenten Consumerklasse.
2.  Füllen Sie die Eigenschaften der -Instanz mit den Parametern der Aktion aus, die der physische Consumer ausführen soll.

Im folgenden MOF-Codebeispiel wird ein logischer Consumer beschrieben, der ein Skript enthält.

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Nachdem Sie den logischen Consumer erstellt haben, müssen Sie jeden Filter mit einem Ereignisfilter verknüpfen, um die Aktion einem bestimmten Ereignis zu zuweisen. Weitere Informationen finden Sie unter [Erstellen eines Ereignisfilters.](creating-an-event-filter.md)

 

 



