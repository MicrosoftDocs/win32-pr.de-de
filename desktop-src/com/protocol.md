---
title: Protokoll
description: Gibt an, dass diese OLE 2-Klasse in OLE 1-Containern einfügbar ist.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- COM-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338006"
---
# <a name="protocol"></a><span data-ttu-id="fdfb7-104">Protokoll</span><span class="sxs-lookup"><span data-stu-id="fdfb7-104">Protocol</span></span>

<span data-ttu-id="fdfb7-105">Gibt an, dass diese OLE 2-Klasse in OLE 1-Containern einfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fdfb7-105">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="fdfb7-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="fdfb7-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a><span data-ttu-id="fdfb7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdfb7-107">Remarks</span></span>

<span data-ttu-id="fdfb7-108">Der Eintrag **stdfileediting** gibt OLE 1-Kompatibilitätsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="fdfb7-108">The **StdFileEditing** entry specifies OLE 1 compatibility information.</span></span> <span data-ttu-id="fdfb7-109">Sie sollte nur vorhanden sein, wenn Objekte dieser Klasse in OLE 1-Containern eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="fdfb7-109">It should be present only if objects of this class are insertable in OLE 1 containers.</span></span>

<span data-ttu-id="fdfb7-110">Der **Server** gibt den vollständigen Pfad zur OLE 2-Serveranwendung an, und das **Verb** gibt die Verben an.</span><span class="sxs-lookup"><span data-stu-id="fdfb7-110">**Server** specifies the full path to the OLE 2 server application and **Verb** specifies the verbs.</span></span> <span data-ttu-id="fdfb7-111">Verb 0 ist das primäre Verb, und zusätzliche Verben müssen nacheinander nummeriert werden.</span><span class="sxs-lookup"><span data-stu-id="fdfb7-111">Verb 0 is the primary verb and additional verbs must be numbered consecutively.</span></span>

 

 




