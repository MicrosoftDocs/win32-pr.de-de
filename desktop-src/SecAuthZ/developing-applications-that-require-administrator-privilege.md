---
description: Es ist möglich, eine Anwendung zu entwickeln, die Vorgänge ausführt, für die Administratorrechte erforderlich sind, aber noch als Standardbenutzer ausgeführt werden.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363633"
---
# <a name="developing-applications-that-require-administrator-privilege"></a><span data-ttu-id="f5480-103">Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="f5480-103">Developing Applications that Require Administrator Privilege</span></span>

<span data-ttu-id="f5480-104">Es ist möglich, eine Anwendung zu entwickeln, die Vorgänge ausführt, für die Administratorrechte erforderlich sind, aber noch als Standardbenutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f5480-104">It is possible to develop an application that performs operations that require administrator privilege yet runs as a standard user.</span></span>

<span data-ttu-id="f5480-105">Es gibt mehrere Modelle, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="f5480-105">There are several models for accomplishing this.</span></span>



| <span data-ttu-id="f5480-106">Thema</span><span class="sxs-lookup"><span data-stu-id="f5480-106">Topic</span></span>                                                                | <span data-ttu-id="f5480-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5480-107">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5480-108">Modell mit erhöhten Rechten</span><span class="sxs-lookup"><span data-stu-id="f5480-108">Elevated Task Model</span></span>](elevated-task-model.md)                       | <span data-ttu-id="f5480-109">Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem eine geplante Aufgabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f5480-109">An application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>                                                                     |
| [<span data-ttu-id="f5480-110">Betriebs System-Dienstmodell</span><span class="sxs-lookup"><span data-stu-id="f5480-110">Operating System Service Model</span></span>](operating-system-service-model.md) | <span data-ttu-id="f5480-111">Eine Anwendung, die als Standardbenutzer ausgeführt wird, kommuniziert mithilfe eines [Remote Prozedur Aufrufs](/windows/desktop/Rpc/rpc-start-page) (RPC) mit einem Dienst, der als **System** ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5480-111">An application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>                                              |
| [<span data-ttu-id="f5480-112">Administrator Broker Modell</span><span class="sxs-lookup"><span data-stu-id="f5480-112">Administrator Broker Model</span></span>](administrator-broker-model.md)         | <span data-ttu-id="f5480-113">Die Anwendung ist in zwei Programme unterteilt.</span><span class="sxs-lookup"><span data-stu-id="f5480-113">The application is divided into two programs.</span></span> <span data-ttu-id="f5480-114">Eines der Programme wird als Standardbenutzer ausgeführt, und die andere wird mit Administrator Berechtigungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5480-114">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>                                                          |
| [<span data-ttu-id="f5480-115">COM-Objektmodell für Administratoren</span><span class="sxs-lookup"><span data-stu-id="f5480-115">Administrator COM Object Model</span></span>](administrator-com-object-model.md) | <span data-ttu-id="f5480-116">Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem ein Objekt mit [Component Object Model](/windows/desktop/com/component-object-model--com--portal) erhöhten Rechten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f5480-116">An application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> |



 

 

 
