---
description: Ein Namespace Objekt Pfad beschreibt den Speicherort eines bestimmten Namespaces auf einem Server. Ein Namespace Objekt Pfad enthält Server-und Namespace Elemente und wird entweder mit vorwärts-oder rückwärts Schrägstrichen formatiert.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Beschreiben eines Objekt Pfads für den WMI-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042058"
---
# <a name="describing-a-wmi-namespace-object-path"></a><span data-ttu-id="444b6-104">Beschreiben eines Objekt Pfads für den WMI-Namespace</span><span class="sxs-lookup"><span data-stu-id="444b6-104">Describing a WMI Namespace Object Path</span></span>

<span data-ttu-id="444b6-105">Ein Namespace Objekt Pfad beschreibt den Speicherort eines bestimmten Namespaces auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="444b6-105">A namespace object path describes the location of a particular namespace on a server.</span></span> <span data-ttu-id="444b6-106">Ein Namespace Objekt Pfad enthält Server-und Namespace Elemente und wird entweder mit vorwärts-oder rückwärts Schrägstrichen formatiert.</span><span class="sxs-lookup"><span data-stu-id="444b6-106">A namespace object path contains server and namespace elements, and is formatted using either forward or backward slashes.</span></span>

<span data-ttu-id="444b6-107">Das Server-Element gibt den Netzwerknamen des Computers an, auf dem der Namespace gehostet wird, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="444b6-107">The server element specifies the network name of the computer that is hosting the namespace, as shown in the following example.</span></span>

``` syntax
\\Server\Namespace
```

<span data-ttu-id="444b6-108">\- oder -</span><span class="sxs-lookup"><span data-stu-id="444b6-108">\- or -</span></span>

``` syntax
//Server/Namespace
```

<span data-ttu-id="444b6-109">Wenn der Server der lokale Computer ist, verwenden Sie einen einzelnen Punkt anstelle des Server namens, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="444b6-109">If the server is the local computer, use a single dot instead of the server name, as shown in the following example.</span></span>

``` syntax
\\.\Namespace
```

<span data-ttu-id="444b6-110">Das Namespace-Element gibt einen beliebigen gültigen Namespace an.</span><span class="sxs-lookup"><span data-stu-id="444b6-110">The namespace element specifies any valid namespace.</span></span> <span data-ttu-id="444b6-111">Ein Namespace wird durch eine hierarchische Zeichenfolge dargestellt, die Elemente enthält, die durch einzelne umgekehrte Schrägstriche (z. b. root cimv2) getrennt sind \\ .</span><span class="sxs-lookup"><span data-stu-id="444b6-111">A namespace is represented with a hierarchical string containing elements delimited by single backslashes, such as root\\cimv2.</span></span> <span data-ttu-id="444b6-112">Sie können keine Schrägstriche innerhalb von Namespace Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="444b6-112">You cannot use forward slashes within namespace names.</span></span>

 

 



