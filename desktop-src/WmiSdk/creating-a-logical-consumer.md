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
# <a name="creating-a-logical-consumer"></a><span data-ttu-id="467c0-103">Erstellen eines logischen Consumers</span><span class="sxs-lookup"><span data-stu-id="467c0-103">Creating a Logical Consumer</span></span>

<span data-ttu-id="467c0-104">Ein logischer Consumer ist eine Instanz einer permanenten ereignisconsumerklasse.</span><span class="sxs-lookup"><span data-stu-id="467c0-104">A logical consumer is an instance of a permanent event consumer class.</span></span> <span data-ttu-id="467c0-105">Der Hauptzweck eines logischen Consumers besteht darin, dem physischen Consumer die Parameter für die Aktivitäten, die der physische Consumer ausführt, bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="467c0-105">The main purpose of a logical consumer is to provide the physical consumer with the parameters for the activities the physical consumer performs.</span></span> <span data-ttu-id="467c0-106">Weitere Informationen finden Sie unter [Erstellen einer neuen dauerhaften Ereignisconsumer-Klasse](creating-a-new-permanent-event-consumer-class.md).</span><span class="sxs-lookup"><span data-stu-id="467c0-106">For more information, see [Creating a New Permanent Event Consumer Class](creating-a-new-permanent-event-consumer-class.md).</span></span> <span data-ttu-id="467c0-107">Der permanente Consumer muss in den Consumer-, Filter-und Binding-Instanzen die gleiche " [**kreatorsid**](--eventconsumer.md) " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="467c0-107">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="467c0-108">Weitere Informationen finden Sie unter [sicheres empfangen von Ereignissen](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="467c0-108">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span> <span data-ttu-id="467c0-109">Ein Beispiel für die Verwendung eines logischen Consumers finden Sie unter [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md), das zeigt, wie die Standard Consumerklasse [**activescripteventconsumer**](activescripteventconsumer.md) verwendet wird, um einen permanenten Consumer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="467c0-109">For an example of using a logical consumer, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md), which shows the use of the standard consumer class [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to configure a permanent consumer.</span></span>

<span data-ttu-id="467c0-110">Im folgenden Verfahren wird beschrieben, wie ein logischer Consumer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="467c0-110">The following procedure describes how to create a logical consumer.</span></span>

<span data-ttu-id="467c0-111">**So erstellen Sie einen logischen Consumer**</span><span class="sxs-lookup"><span data-stu-id="467c0-111">**To create a logical consumer**</span></span>

1.  <span data-ttu-id="467c0-112">Erstellen Sie eine Instanz ihrer permanenten Consumerklasse.</span><span class="sxs-lookup"><span data-stu-id="467c0-112">Create an instance of your permanent consumer class.</span></span>
2.  <span data-ttu-id="467c0-113">Füllen Sie die Eigenschaften der Instanz mit den Parametern der Aktion aus, die der physische Consumer durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="467c0-113">Fill the properties of the instance with the parameters of the action you want the physical consumer to perform.</span></span>

<span data-ttu-id="467c0-114">Im folgenden MOF-Codebeispiel wird ein logischer Consumer beschrieben, der ein Skript enthält.</span><span class="sxs-lookup"><span data-stu-id="467c0-114">The following MOF code example describes a logical consumer that contains a script.</span></span>

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

<span data-ttu-id="467c0-115">Nachdem Sie den logischen Consumer erstellt haben, müssen Sie jeden Filter mit einem Ereignis Filter verknüpfen, um die Aktion einem bestimmten Ereignis zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="467c0-115">After you create the logical consumer, you must then link each filter to an event filter to assign the action to a particular event.</span></span> <span data-ttu-id="467c0-116">Weitere Informationen finden Sie unter [Erstellen eines Ereignis Filters](creating-an-event-filter.md).</span><span class="sxs-lookup"><span data-stu-id="467c0-116">For more information, see [Creating an Event Filter](creating-an-event-filter.md).</span></span>

 

 



