---
description: Für jede Anwendung, die einen Autorisierungs Richtlinien Speicher verwendet, müssen Sie ein IAzApplication-Objekt erstellen und es anschließend in einem Richtlinien Speicher speichern.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Erstellen eines Anwendungs Objekts im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a4852ef0c06d721f9409c000989895f6767eb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753496"
---
# <a name="creating-an-application-object-in-script"></a><span data-ttu-id="fe208-103">Erstellen eines Anwendungs Objekts im Skript</span><span class="sxs-lookup"><span data-stu-id="fe208-103">Creating an Application Object in Script</span></span>

<span data-ttu-id="fe208-104">Ein Autorisierungs Richtlinien Speicher enthält Autorisierungs Richtlinien Informationen für eine oder mehrere Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="fe208-104">An authorization policy store contains authorization policy information for one or more applications.</span></span> <span data-ttu-id="fe208-105">Für jede Anwendung, die einen Autorisierungs Richtlinien Speicher verwendet, müssen Sie ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt erstellen und in einem Richtlinien Speicher speichern.</span><span class="sxs-lookup"><span data-stu-id="fe208-105">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>

<span data-ttu-id="fe208-106">Im folgenden Beispiel wird gezeigt, wie ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt erstellt wird, das eine Anwendung darstellt, und wie das **IAzApplication** -Objekt dem Autorisierungs Richtlinien Speicher hinzugefügt wird, der von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe208-106">The following example shows how to create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that represents an application and how to add the **IAzApplication** object to the authorization policy store the application uses.</span></span> <span data-ttu-id="fe208-107">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fe208-107">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.CreateApplication("Expense")

'  Save changes to the store.
expenseApp.Submit
```



 

 



