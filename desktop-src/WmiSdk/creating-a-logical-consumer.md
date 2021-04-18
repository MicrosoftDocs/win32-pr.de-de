---
description: Ein logischer Consumer ist eine Instanz einer permanenten ereignisconsumerklasse.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Erstellen eines logischen Consumers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352521"
---
# <a name="creating-a-logical-consumer"></a>Erstellen eines logischen Consumers

Ein logischer Consumer ist eine Instanz einer permanenten ereignisconsumerklasse. Der Hauptzweck eines logischen Consumers besteht darin, dem physischen Consumer die Parameter für die Aktivitäten, die der physische Consumer ausführt, bereitzustellen. Weitere Informationen finden Sie unter [Erstellen einer neuen dauerhaften Ereignisconsumer-Klasse](creating-a-new-permanent-event-consumer-class.md). Der permanente Consumer muss in den Consumer-, Filter-und Binding-Instanzen die gleiche " [**kreatorsid**](--eventconsumer.md) " aufweisen. Weitere Informationen finden Sie unter [sicheres empfangen von Ereignissen](receiving-events-securely.md). Ein Beispiel für die Verwendung eines logischen Consumers finden Sie unter [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md), das zeigt, wie die Standard Consumerklasse [**activescripteventconsumer**](activescripteventconsumer.md) verwendet wird, um einen permanenten Consumer zu konfigurieren.

Im folgenden Verfahren wird beschrieben, wie ein logischer Consumer erstellt wird.

**So erstellen Sie einen logischen Consumer**

1.  Erstellen Sie eine Instanz ihrer permanenten Consumerklasse.
2.  Füllen Sie die Eigenschaften der Instanz mit den Parametern der Aktion aus, die der physische Consumer durchführen soll.

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

Nachdem Sie den logischen Consumer erstellt haben, müssen Sie jeden Filter mit einem Ereignis Filter verknüpfen, um die Aktion einem bestimmten Ereignis zuzuweisen. Weitere Informationen finden Sie unter [Erstellen eines Ereignis Filters](creating-an-event-filter.md).

 

 



