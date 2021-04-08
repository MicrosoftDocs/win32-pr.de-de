---
title: Der Serverstub
description: Der Serverstub stellt für jeden Vorgang, der in der Eingabe-IDL-Datei definiert ist, Ersatz Einstiegspunkte auf dem Server bereit.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- Mittel l-compilermittell, Mittel l-und RPC-Mittell, Schnittstellen, Serverstub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037396"
---
# <a name="the-server-stub"></a><span data-ttu-id="18268-104">Der Serverstub</span><span class="sxs-lookup"><span data-stu-id="18268-104">The Server Stub</span></span>

<span data-ttu-id="18268-105">Der Serverstub stellt für jeden Vorgang, der in der Eingabe-IDL-Datei definiert ist, Ersatz Einstiegspunkte auf dem Server bereit.</span><span class="sxs-lookup"><span data-stu-id="18268-105">The server stub provides surrogate entry points on the server for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="18268-106">Wenn eine Server-Stub-Routine von der RPC-Lauf Zeit Bibliothek aufgerufen wird, führt Sie die folgenden Funktionen aus:</span><span class="sxs-lookup"><span data-stu-id="18268-106">When a server stub routine is invoked by the RPC run-time library, it performs the following functions:</span></span>

-   <span data-ttu-id="18268-107">Entfernt Eingabeargumente (entpackt die Argumente aus ihren übertragenen Formaten).</span><span class="sxs-lookup"><span data-stu-id="18268-107">Unmarshals input arguments (unpacks the arguments from their transmitted formats).</span></span>
-   <span data-ttu-id="18268-108">Ruft die tatsächliche Implementierung der Prozedur auf dem Server auf.</span><span class="sxs-lookup"><span data-stu-id="18268-108">Calls the actual implementation of the procedure on the server.</span></span>
-   <span data-ttu-id="18268-109">Marsheit Ausgabe Argumente (verpackt die Argumente in die übertragenen Formulare).</span><span class="sxs-lookup"><span data-stu-id="18268-109">Marshals output arguments (packages the arguments into the transmitted forms).</span></span>

<span data-ttu-id="18268-110">Der-Compilerschalter [**/Server**](-server.md), [**/sstub**](-sstub.md)und [**/out**](-out.md) wirkt sich auf die Server-Stub-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="18268-110">The MIDL compiler switches [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

 

 




