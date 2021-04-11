---
title: Service Parameters
description: Gibt die Befehlszeilenparameter an, die an ein Objekt zu übertragen sind, das zur Verwendung durch com über den Registrierungs Wert LocalService installiert wird.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Registrierungs Wert von Service Parameters com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310123"
---
# <a name="serviceparameters"></a><span data-ttu-id="06222-104">Service Parameters</span><span class="sxs-lookup"><span data-stu-id="06222-104">ServiceParameters</span></span>

<span data-ttu-id="06222-105">Gibt die Befehlszeilenparameter an, die an ein Objekt zu übertragen sind, das zur Verwendung durch com über den Registrierungs Wert [**LocalService**](localservice.md) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="06222-105">Specifies the command-line parameters to be passed to an object installed for use by COM through the [**LocalService**](localservice.md) registry value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="06222-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="06222-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a><span data-ttu-id="06222-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06222-107">Remarks</span></span>

<span data-ttu-id="06222-108">Dies ist ein **reg \_ SZ** -Wert.</span><span class="sxs-lookup"><span data-stu-id="06222-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="06222-109">Diese Zeichenfolge wird beim Start als Befehlszeilenargument an den Dienst übermittelt.</span><span class="sxs-lookup"><span data-stu-id="06222-109">This string is passed to the service as a command-line argument as it is being launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06222-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06222-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06222-111">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="06222-111">**LocalService**</span></span>](localservice.md)
</dt> <dt>

[<span data-ttu-id="06222-112">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="06222-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 




