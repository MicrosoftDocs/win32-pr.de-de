---
title: "\"Auxusertype\""
description: Gibt den kurzen anzeigen Amen und Anwendungsnamen einer Anwendung an.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- Registrierungsschlüssel für "auxusertype" com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707032"
---
# <a name="auxusertype"></a><span data-ttu-id="0b519-104">"Auxusertype"</span><span class="sxs-lookup"><span data-stu-id="0b519-104">AuxUserType</span></span>

<span data-ttu-id="0b519-105">Gibt den kurzen anzeigen Amen und Anwendungsnamen einer Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="0b519-105">Specifies an application's short display name and application names.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0b519-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="0b519-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a><span data-ttu-id="0b519-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b519-107">Remarks</span></span>

<span data-ttu-id="0b519-108">Die empfohlene maximale Länge für *ShortDisplayName* beträgt 15 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0b519-108">The recommended maximum length for *ShortDisplayName* is 15 characters.</span></span> <span data-ttu-id="0b519-109">Dieser Name wird in Menüs wie Popup Menüs verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b519-109">This name is used in menus, including pop-up menus.</span></span>

<span data-ttu-id="0b519-110">*ApplicationName* muss den tatsächlichen Namen der Anwendung enthalten (z. b. "Acme Draw 2,0").</span><span class="sxs-lookup"><span data-stu-id="0b519-110">*ApplicationName* should contain the actual name of the application (such as "Acme Draw 2.0").</span></span> <span data-ttu-id="0b519-111">Dieser Name wird im **Ergebnis** Feld des Dialog Felds " **spezielles einfügen** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b519-111">This name is used in the **Results** field of the **Paste Special** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b519-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b519-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b519-113">**IOleObject:: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="0b519-113">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




