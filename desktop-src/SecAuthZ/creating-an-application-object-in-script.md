---
description: Für jede Anwendung, die einen Autorisierungsrichtlinienspeicher verwendet, müssen Sie ein IAzApplication-Objekt erstellen und es dann in einem Richtlinienspeicher speichern.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Erstellen eines Anwendungsobjekts im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 02a5ada4a8a79244cc454d9efc88e69a5d9a205241119b5dda371699f0c86552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782546"
---
# <a name="creating-an-application-object-in-script"></a>Erstellen eines Anwendungsobjekts im Skript

Ein Autorisierungsrichtlinienspeicher enthält Autorisierungsrichtlinieninformationen für eine oder mehrere Anwendungen. Für jede Anwendung, die einen Autorisierungsrichtlinienspeicher verwendet, müssen Sie ein [**IAzApplication-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) erstellen und in einem Richtlinienspeicher speichern.

Das folgende Beispiel zeigt, wie Sie ein [**IAzApplication-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) erstellen, das eine Anwendung darstellt, und wie Sie das **IAzApplication-Objekt** dem Autorisierungsrichtlinienspeicher hinzufügen, den die Anwendung verwendet. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein XML-Richtlinienspeicher namens MyStore.xml vorhanden ist.


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



 

 



