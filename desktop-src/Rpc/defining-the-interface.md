---
title: Definieren der Schnittstelle
description: Eine Schnittstellen Definition ist eine formale Angabe, wie eine Client Anwendung und eine Serveranwendung miteinander kommunizieren.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Remote Prozedur Aufruf RPC, Tasks, definieren der Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036645"
---
# <a name="defining-the-interface"></a><span data-ttu-id="098d7-104">Definieren der Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="098d7-104">Defining the Interface</span></span>

<span data-ttu-id="098d7-105">Eine Schnittstellen Definition ist eine formale Angabe, wie eine Client Anwendung und eine Serveranwendung miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="098d7-105">An interface definition is a formal specification for how a client application and a server application communicate with each other.</span></span> <span data-ttu-id="098d7-106">Die-Schnittstelle definiert, wie der Client und der Server einander erkennen, die Remote Prozeduren, die von der Client Anwendung aufgerufen werden können, und die Datentypen für die Parameter und Rückgabewerte dieser Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="098d7-106">The interface defines how the client and server recognize each other, the remote procedures that the client application can call, and the data types for those procedures' parameters and return values.</span></span> <span data-ttu-id="098d7-107">Außerdem wird angegeben, wie die Daten zwischen Client und Server übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="098d7-107">It also specifies how the data is transmitted between client and server.</span></span>

<span data-ttu-id="098d7-108">Diese Schnittstelle wird in der Microsoft Interface Definition Language (mittlerer l) definiert, die aus C-sprach Definitionen besteht, die mit Schlüsselwörtern (Attribute genannt) erweitert werden, die beschreiben, wie die Daten über das Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="098d7-108">You define this interface in the Microsoft Interface Definition Language (MIDL) which consists of C-language definitions augmented with keywords, called attributes, which describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="098d7-109">Die Schnittstellen Definitionsdatei (IDL) enthält Typdefinitionen, Attribute und Funktionsprototypen, die beschreiben, wie Daten im Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="098d7-109">The interface definition (IDL) file contains type definitions, attributes and function prototypes that describe how data is transmitted on the network.</span></span> <span data-ttu-id="098d7-110">Die Anwendungs Konfigurationsdatei (ACF) enthält Attribute, mit denen die Anwendung für eine bestimmte Betriebsumgebung konfiguriert wird, ohne dass sich dies auf die Netzwerk Merkmale auswirkt.</span><span class="sxs-lookup"><span data-stu-id="098d7-110">The application configuration (ACF) file contains attributes that configure your application for a particular operating environment without affecting its network characteristics.</span></span>

 

 




