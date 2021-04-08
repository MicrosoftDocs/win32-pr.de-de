---
title: Fehlstatus
description: Gibt an, wie ein Objekt erstellt und angezeigt wird.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- Falsch Status-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037190"
---
# <a name="miscstatus"></a><span data-ttu-id="3e79b-104">Fehlstatus</span><span class="sxs-lookup"><span data-stu-id="3e79b-104">MiscStatus</span></span>

<span data-ttu-id="3e79b-105">Gibt an, wie ein Objekt erstellt und angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3e79b-105">Specifies how to create and display an object.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3e79b-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="3e79b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a><span data-ttu-id="3e79b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e79b-107">Remarks</span></span>

<span data-ttu-id="3e79b-108">Weitere Informationen finden Sie unter [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) -Enumeration und [**IOleObject:: getfehlstatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span><span class="sxs-lookup"><span data-stu-id="3e79b-108">For more information, see the [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) enumeration and [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span></span>

<span data-ttu-id="3e79b-109">Wenn kein Unterschlüssel gefunden wird, der einem DVASPECT entspricht, wird der Standardwert von " **fehlstatus** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e79b-109">If no subkey that corresponds to a DVASPECT is found, the default value of **MiscStatus** is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e79b-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e79b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e79b-111">**IOleObject:: getfehlstatus**</span><span class="sxs-lookup"><span data-stu-id="3e79b-111">**IOleObject::GetMiscStatus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




