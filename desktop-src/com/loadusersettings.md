---
title: Loadusersettings
description: Bestimmt, ob com das Benutzerprofil für com-Server lädt, die als Anwendungs Identität des Anwendungs Starts ausgeführt werden.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Loadusersettings-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947912"
---
# <a name="loadusersettings"></a><span data-ttu-id="4e147-104">Loadusersettings</span><span class="sxs-lookup"><span data-stu-id="4e147-104">LoadUserSettings</span></span>

<span data-ttu-id="4e147-105">Bestimmt, ob com das Benutzerprofil für com-Server lädt, die als Anwendungs Identität des Anwendungs Starts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4e147-105">Determines whether COM will load the user profile for COM servers running as the launching user application identity.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4e147-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="4e147-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a><span data-ttu-id="4e147-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e147-107">Remarks</span></span>

<span data-ttu-id="4e147-108">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="4e147-108">This is a **REG\_DWORD** value.</span></span> <span data-ttu-id="4e147-109">Wenn *value* ungleich NULL ist, lädt com das Profil des Benutzerkontos, mit dem der com-Server gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4e147-109">If *value* is nonzero, COM loads the profile of the user account with which it launches the COM server.</span></span> <span data-ttu-id="4e147-110">Wenn der *Wert* 0 (null) oder nicht vorhanden ist, lädt com das Profil des Benutzerkontos nicht, mit dem der com-Server gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4e147-110">If *value* is zero or not present, COM will not load the profile of the user account with which it launches the COM server.</span></span>

<span data-ttu-id="4e147-111">Diese Einstellung wird ignoriert, wenn ein [**runas**](runas.md) -Eintrag vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4e147-111">This setting is ignored if a [**RunAs**](runas.md) entry is present.</span></span>

 

 




