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
# <a name="how-to-associate-verbs-with-dde-commands"></a><span data-ttu-id="c9307-103">Zuordnen von Verben zu DDE-Befehlen</span><span class="sxs-lookup"><span data-stu-id="c9307-103">How to Associate Verbs with DDE Commands</span></span>

<span data-ttu-id="c9307-104">Wenn Sie ein Verb aufrufen, wird normalerweise die Anwendung gestartet, die durch den Befehls Unterschlüssel des Verbs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9307-104">Invoking a verb ordinarily launches the application that is specified by the verb's command subkey.</span></span> <span data-ttu-id="c9307-105">Wenn Ihre Anwendung jedoch dynamischer Datenaustausch (DDE) unterstützt, kann die Shell stattdessen eine DDE-Konversation initiieren.</span><span class="sxs-lookup"><span data-stu-id="c9307-105">However, if your application supports Dynamic Data Exchange (DDE), you can instead have the Shell initiate a DDE conversation.</span></span>

<span data-ttu-id="c9307-106">Führen Sie die folgenden Schritte aus, um anzugeben, dass das Aufrufen eines Verbs eine DDE-Konversation initiieren soll.</span><span class="sxs-lookup"><span data-stu-id="c9307-106">To specify that invoking a verb should initiate a DDE conversation, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="c9307-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="c9307-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="c9307-108">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="c9307-108">Step 1:</span></span>

<span data-ttu-id="c9307-109">Fügen Sie dem Schlüssel des Verbs einen **DDE Exec** -Unterschlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9307-109">Add a **ddeexec** subkey to the verb's key.</span></span>

### <a name="step-2"></a><span data-ttu-id="c9307-110">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="c9307-110">Step 2:</span></span>

<span data-ttu-id="c9307-111">Legen Sie den Standardwert von **DDE Exec** auf die DDE-Befehls Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="c9307-111">Set the default value of **ddeexec** to the DDE command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9307-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9307-112">Remarks</span></span>

<span data-ttu-id="c9307-113">Der **ddeexec** -Schlüssel verfügt über drei optionale Unterschlüssel, die eine gewisse Kontrolle über den DDE-Prozess bieten:</span><span class="sxs-lookup"><span data-stu-id="c9307-113">The **ddeexec** key has three optional subkeys that provide some control over the DDE process:</span></span>

-   <span data-ttu-id="c9307-114">**Anwendung**:</span><span class="sxs-lookup"><span data-stu-id="c9307-114">**application**.</span></span> <span data-ttu-id="c9307-115">Legen Sie den Standardwert dieses unter Schlüssels auf den Anwendungsnamen fest, der zum Einrichten der DDE-Konversation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9307-115">Set the default value of this subkey to the application name to be used to establish the DDE conversation.</span></span> <span data-ttu-id="c9307-116">Wenn kein **Anwendungs** Unterschlüssel vorhanden ist, wird der Standardwert des **Befehls** unter Schlüssels des Verbs als Anwendungsname verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9307-116">If there is no **application** subkey, the default value of the verb's **command** subkey is used as the application name.</span></span>
-   <span data-ttu-id="c9307-117">**Thema**.</span><span class="sxs-lookup"><span data-stu-id="c9307-117">**topic**.</span></span> <span data-ttu-id="c9307-118">Legen Sie den Standardwert dieses unter Schlüssels auf den Themen Namen der DDE-Konversation fest.</span><span class="sxs-lookup"><span data-stu-id="c9307-118">Set the default value of this subkey to the topic name of the DDE conversation.</span></span> <span data-ttu-id="c9307-119">Wenn kein **Themen** Unterschlüssel vorhanden ist, wird System als Themenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9307-119">If there is no **topic** subkey, System is used as the topic name.</span></span>
-   <span data-ttu-id="c9307-120">**ifexec**.</span><span class="sxs-lookup"><span data-stu-id="c9307-120">**ifexec**.</span></span> <span data-ttu-id="c9307-121">Legen Sie den Standardwert dieses unter Schlüssels auf den DDE-Befehl fest, der verwendet werden soll, wenn DDE Conversation nicht initiiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9307-121">Set the default value of this subkey to the DDE command to be used if DDE conversation cannot be initiated.</span></span> <span data-ttu-id="c9307-122">Wenn die Initiierung fehlschlägt, wird die Anwendung gestartet, die durch den Standardwert des **Befehls** unter Schlüssels des Verbs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9307-122">When initiation fails, the application that is specified by the default value of the verb's **command** subkey is launched.</span></span> <span data-ttu-id="c9307-123">Wenn ein **ifexec** -Schlüssel vorhanden ist, wird sein Standardwert als DDE-Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9307-123">If an **ifexec** key exists, its default value will then be used as the DDE command.</span></span> <span data-ttu-id="c9307-124">Wenn kein **ifexec** -Unterschlüssel vorhanden ist, wird der Standardwert des **DDE Exec** -Schlüssels erneut als DDE-Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9307-124">If there is no **ifexec** subkey, the default value of the **ddeexec** key will be used again as the DDE command.</span></span>

<span data-ttu-id="c9307-125">Im folgenden Beispiel wird angegeben, dass beim Aufrufen des geöffneten Verbs für "MyProgram. 1" eine DDE-Konversation mit dem Befehl "DDE" ("%1") und dem Anwendungsnamen "myprogram" initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="c9307-125">The following example specifies that invoking the open verb for MyProgram.1 initiates a DDE conversation with a DDE command of Open("%1") and an application name of MyProgram.</span></span>

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

 

 



