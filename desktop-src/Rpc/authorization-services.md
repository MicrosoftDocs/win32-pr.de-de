---
title: Autorisierungs Dienste
description: Ein Autorisierungs Dienst ist die Methode, die der SSP zum Autorisieren des Zugriffs auf eine Remote Prozedur verwendet. SSPs können mehr als einen Autorisierungs Dienst bereitstellen. Sie wählen jedoch in der Regel eine Standardeinstellung aus.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037272"
---
# <a name="authorization-services"></a>Autorisierungs Dienste

Ein Autorisierungs Dienst ist die Methode, die der SSP zum Autorisieren des Zugriffs auf eine Remote Prozedur verwendet. SSPs können mehr als einen Autorisierungs Dienst bereitstellen. Sie wählen jedoch in der Regel eine Standardeinstellung aus.

Die Anwendung kann die Standard Autorisierungs Methode für den aktuellen SSP verwenden, oder Sie kann eine-Methode angeben. Derzeit werden von Microsoft RPC zwei Autorisierungs Methoden unterstützt. Eine besteht darin, dass der Server Autorisierung basierend auf dem Namen des Client Programms bereitstellt. Die andere ist, dass der Server die Anmelde Informationen des Clients mit der Zugriffs Steuerungs Liste (Access Control List, ACL) des Servers vergleicht.

Eine Liste der Autorisierungs Dienste finden Sie unter [Authorization-Service-Konstanten](authorization-service-constants.md).

> [!Note]  
> Es wird empfohlen, dass der Entwickler RPC \_ C \_ Authz \_ None verwendet.

 

 

 




