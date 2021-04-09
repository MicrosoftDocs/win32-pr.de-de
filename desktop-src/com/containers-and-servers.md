---
title: Container und Server
description: Container und Server
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856904"
---
# <a name="containers-and-servers"></a><span data-ttu-id="2497e-103">Container und Server</span><span class="sxs-lookup"><span data-stu-id="2497e-103">Containers and Servers</span></span>

<span data-ttu-id="2497e-104">Verbund Dokument Anwendungen haben zwei grundlegende Typen: Container Anwendungen und Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2497e-104">Compound document applications are of two basic types: container applications and server applications.</span></span> <span data-ttu-id="2497e-105">OLE-Container Anwendungen bieten Benutzern die Möglichkeit, Verbund Dokumente zu erstellen, zu bearbeiten, zu speichern und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2497e-105">OLE container applications provide users with the ability to create, edit, save, and retrieve compound documents.</span></span> <span data-ttu-id="2497e-106">OLE-Server Anwendungen bieten Benutzern die Möglichkeit, Dokumente und andere Daten Darstellungen zu erstellen, die entweder als Links oder als Einbettungen in Container Anwendungen enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="2497e-106">OLE server applications provide users with the means to create documents and other data representations that can be contained as either links or embeddings in container applications.</span></span> <span data-ttu-id="2497e-107">Bei einer OLE-Anwendung kann es sich um eine Containeranwendung, eine Serveranwendung oder beides handeln.</span><span class="sxs-lookup"><span data-stu-id="2497e-107">An OLE application can be a container application, a server application, or both.</span></span>

<span data-ttu-id="2497e-108">OLE-Server Anwendungen unterscheiden sich auch darin, ob Sie als *Prozess interne Server* oder *lokale Server* implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2497e-108">OLE server applications also differ in whether they are implemented as *in-process servers* or *local servers*.</span></span> <span data-ttu-id="2497e-109">Ein Prozess interner Server ist eine Dynamic Link Library (dll), die im Prozessbereich der Containeranwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2497e-109">An in-process server is a dynamic link library (DLL) that runs in the container application's process space.</span></span> <span data-ttu-id="2497e-110">Sie können einen in-Process-Server nur innerhalb der Containeranwendung ausführen.</span><span class="sxs-lookup"><span data-stu-id="2497e-110">You can run an in-process server only from within the container application.</span></span>

> [!Note]  
> <span data-ttu-id="2497e-111">In zukünftigen Versionen von OLE können Verknüpfungen und Einbettungen über Computer Grenzen hinweg aktiviert werden, damit eine Containeranwendung auf einem Computer ein Verbund Dokument Objekt verwenden kann, das von einem *Remote Server* auf einem anderen Computer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2497e-111">Future releases of OLE will enable linking and embedding across computer boundaries, so that a container application on one computer will be able to use a compound document object provided by a *remote server* running on another computer.</span></span> <span data-ttu-id="2497e-112">Aus Sicht der Containeranwendung ist jede OLE-Serveranwendung, die in einem eigenen Prozessbereich ausgeführt wird, unabhängig davon, ob Sie auf demselben Computer oder auf einem Remote Computer ausgeführt wird, ein Prozess *außerhalb des* Prozesses.</span><span class="sxs-lookup"><span data-stu-id="2497e-112">From a container application's point of view, any OLE server application that runs in its own process space, whether on the same computer or a remote computer, is an *out-of-processÂ server*.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2497e-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2497e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2497e-114">Verbund Dokumente</span><span class="sxs-lookup"><span data-stu-id="2497e-114">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="2497e-115">Prozess interne Server</span><span class="sxs-lookup"><span data-stu-id="2497e-115">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




