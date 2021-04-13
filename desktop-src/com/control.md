---
title: Control
description: Identifiziert ein Objekt als ActiveX-Steuerelement.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Registrierungsschlüssel-com Steuern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388750"
---
# <a name="control"></a><span data-ttu-id="0e332-104">Control</span><span class="sxs-lookup"><span data-stu-id="0e332-104">Control</span></span>

<span data-ttu-id="0e332-105">Identifiziert ein Objekt als ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e332-105">Identifies an object as an ActiveX Control.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0e332-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="0e332-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a><span data-ttu-id="0e332-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e332-107">Remarks</span></span>

<span data-ttu-id="0e332-108">Dieser optionale Eintrag wird von Containern zum Ausfüllen von Dialogfeldern verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e332-108">This optional entry is used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="0e332-109">Der Container verwendet diesen Unterschlüssel, um zu bestimmen, ob ein Objekt in ein Dialogfeld eingeschlossen werden soll, das ActiveX-Steuerelemente anzeigt.</span><span class="sxs-lookup"><span data-stu-id="0e332-109">The container uses this subkey to determine whether to include an object in a dialog box that displays ActiveX Controls.</span></span> <span data-ttu-id="0e332-110">Ein Steuerelement kann diesen Eintrag weglassen, wenn er nur für den Einsatz mit einem bestimmten Container vorgesehen ist und daher nicht in anderen Containern eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e332-110">A control can omit this entry if it is designed to work only with a specific container and therefore does is not intended to be inserted in other containers.</span></span>

 

 




