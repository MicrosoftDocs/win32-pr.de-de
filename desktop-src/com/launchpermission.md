---
title: Launchberechtigung
description: Beschreibt die Access Control Liste (ACL) der Prinzipale, die neue Server für diese Klasse starten können. Dieser Wert kann unter jedem AppID-Schlüssel hinzugefügt werden, um die Aktivierung durch Remote Clients bestimmter Klassen einzuschränken.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Launchberechtigungs-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037613"
---
# <a name="launchpermission"></a><span data-ttu-id="7dec7-105">Launchberechtigung</span><span class="sxs-lookup"><span data-stu-id="7dec7-105">LaunchPermission</span></span>

<span data-ttu-id="7dec7-106">Beschreibt die Access Control Liste (ACL) der Prinzipale, die neue Server für diese Klasse starten können.</span><span class="sxs-lookup"><span data-stu-id="7dec7-106">Describes the Access Control List (ACL) of the principals that can start new servers for this class.</span></span> <span data-ttu-id="7dec7-107">Dieser Wert kann unter jedem [**AppID**](appid-key.md) -Schlüssel hinzugefügt werden, um die Aktivierung durch Remote Clients bestimmter Klassen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="7dec7-107">This value may be added under any [**AppID**](appid-key.md) key to limit activation by remote clients of specific classes.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7dec7-108">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="7dec7-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="7dec7-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dec7-109">Remarks</span></span>

<span data-ttu-id="7dec7-110">Dies ist ein **reg- \_ Binärwert** .</span><span class="sxs-lookup"><span data-stu-id="7dec7-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="7dec7-111">Wenn eine lokale oder eine Remote Anforderung zum Starten des Servers dieser Klasse empfangen wird, wird die durch diesen Wert beschriebene ACL während der Identität des Clients aktiviert, und Ihr Erfolg erlaubt oder verweigert das Starten des Servers.</span><span class="sxs-lookup"><span data-stu-id="7dec7-111">Upon receiving a local or remote request to launch the server of this class, the ACL described by this value is checked while impersonating the client, and its success either allows or disallows the launching of the server.</span></span> <span data-ttu-id="7dec7-112">Wenn dieser Wert nicht vorhanden ist, wird der [**defaultlaunchberechtigungswert**](defaultlaunchpermission.md) auf dieselbe Weise überprüft, um zu bestimmen, ob der Klassen Code gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7dec7-112">If this value does not exist, the [**DefaultLaunchPermission**](defaultlaunchpermission.md) value is checked in the same way to determine whether the class code can be launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dec7-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7dec7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dec7-114">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="7dec7-114">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="7dec7-115">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="7dec7-115">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="7dec7-116">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="7dec7-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




