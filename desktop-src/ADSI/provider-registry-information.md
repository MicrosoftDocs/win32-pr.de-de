---
title: Anbieter Registrierungsinformationen
description: In diesem Thema wird gezeigt, welche Schlüssel und Werte beim Hinzufügen eines ADSI-Anbieters festgelegt werden müssen.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790a80964bdcc6111a4c167056a0b85bda23e147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387956"
---
# <a name="provider-registry-information"></a><span data-ttu-id="d08a1-103">Anbieter Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="d08a1-103">Provider Registry Information</span></span>

<span data-ttu-id="d08a1-104">Der Anbieter wird bei ADSI mit den folgenden Schlüsseln und Werten registriert:</span><span class="sxs-lookup"><span data-stu-id="d08a1-104">The provider is registered with ADSI with the following keys and values:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

<span data-ttu-id="d08a1-105">Der Anbieter wird bei Windows mit den folgenden Schlüsseln und Werten registriert:</span><span class="sxs-lookup"><span data-stu-id="d08a1-105">The provider is registered with Windows with the following keys and values:</span></span>

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

<span data-ttu-id="d08a1-106">Der Anbieter Namespace wird bei Windows mit den folgenden Schlüsseln und Werten registriert:</span><span class="sxs-lookup"><span data-stu-id="d08a1-106">The provider namespace is registered with Windows with the following keys and values:</span></span>

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

<span data-ttu-id="d08a1-107">In den vorherigen Absätzen ist der *Anbieter* der Bezeichner des Objekts der obersten Ebene des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="d08a1-107">In the previous paragraphs, the *provider* is the identifier of the provider's top-level object.</span></span> <span data-ttu-id="d08a1-108">Der *Anbieter Namespace* ist der Bezeichner des Objekts, das den Namespace des Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="d08a1-108">The *provider namespace* is the identifier of the object which implements the provider's namespace.</span></span>

<span data-ttu-id="d08a1-109">Ein bestimmtes Beispiel finden Sie unter [Installieren der Beispiel Anbieter Komponente](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="d08a1-109">For a specific example, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

 

 




