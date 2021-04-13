---
title: Namespaces
description: Objekte, die sich in einem bestimmten Namespace befinden, werden durch einen eindeutigen Namen identifiziert.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- Namespaces ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387958"
---
# <a name="namespaces"></a><span data-ttu-id="7a2e8-104">Namespaces</span><span class="sxs-lookup"><span data-stu-id="7a2e8-104">Namespaces</span></span>

<span data-ttu-id="7a2e8-105">Objekte, die sich in einem bestimmten Namespace befinden, werden durch einen eindeutigen Namen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-105">Objects that reside within a given namespace are identified by a unique name.</span></span> <span data-ttu-id="7a2e8-106">Beispielsweise befinden sich auf einem PC-Laufwerk gespeicherte Dateien im Dateisystem-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-106">For example, files stored on a PC disk drive reside in the file system namespace.</span></span> <span data-ttu-id="7a2e8-107">Der eindeutige Name einer Datei basiert darauf, wo Sie im Dateisystem-Namespace gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-107">The unique name of a file is based on where it is stored in the file system namespace.</span></span> <span data-ttu-id="7a2e8-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7a2e8-108">For example:</span></span>


```C++
C:\public\documents\adsi\adsi_spec.doc
```



<span data-ttu-id="7a2e8-109">Verzeichnisdienst-Namespaces identifizieren auch die Objekte, die Sie mit eindeutigen Namen enthalten, die normalerweise auf dem Speicherort im Verzeichnis basieren, an dem das Objekt gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-109">Directory service namespaces also identify the objects they contain by unique names which are usually based on the location in the directory where the object can be found.</span></span> <span data-ttu-id="7a2e8-110">Beispielsweise kann ein bestimmtes Objekt in einem X. 500-Verzeichnis einen Namen wie den folgenden aufweisen:</span><span class="sxs-lookup"><span data-stu-id="7a2e8-110">For example, in an X.500 directory, a given object might have a name like this:</span></span>


```C++
CN=John,OU=Marketing,O=Fabrikam
```



<span data-ttu-id="7a2e8-111">Verschiedene Verzeichnisdienste verwenden verschiedene Formulare, um die darin enthaltenen Objekte zu benennen.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-111">Different directory services use different forms for naming the objects they contain.</span></span> <span data-ttu-id="7a2e8-112">Dies vereinfacht den Umgang mit verschiedenen Namespaces, insbesondere für Entwickler, die alle unterschiedlichen Umgebungen in Betracht ziehen, in denen der Code möglicherweise ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-112">This makes dealing with different namespaces challenging, especially for developers, considering all of the different environments on which the code might be running.</span></span>

<span data-ttu-id="7a2e8-113">Ein Ziel von Active Directory Service Interfaces (ADSI) ist die Bereitstellung eines Benennungs Frameworks, das den Zugriff auf Namespaces verschiedener Verzeichnis Dienstanbieter ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-113">A goal of Active Directory Service Interfaces (ADSI) is to provide a naming framework that allows access to namespaces of different directory service providers.</span></span>

<span data-ttu-id="7a2e8-114">ADSI definiert eine Benennungs Konvention, mit der ein Objekt in einer heterogenen Umgebung eindeutig identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-114">ADSI defines a naming convention that can uniquely identify an object in a heterogeneous environment.</span></span> <span data-ttu-id="7a2e8-115">Diese Namen werden als ADsPath-Zeichen folgen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7a2e8-115">These names are called ADsPath strings.</span></span> <span data-ttu-id="7a2e8-116">ADsPath-Zeichen folgen benötigen verschiedene Formen:</span><span class="sxs-lookup"><span data-stu-id="7a2e8-116">ADsPath strings take several forms:</span></span>


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



<span data-ttu-id="7a2e8-117">Es können zusätzliche zusätzliche Formate von ADSI-Anbietern eingeführt werden (z. b. der ADSI-Anbieter für den Internetinformationsdienste-Server, der die adspaths "IIS://" unterstützt).</span><span class="sxs-lookup"><span data-stu-id="7a2e8-117">Additional ADsPath formats can be introduced by different ADSI providers (such as the ADSI provider for the Internet Information Services server, which support the "IIS://" ADsPaths).</span></span>

 

 




