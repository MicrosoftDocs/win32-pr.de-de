---
description: Mithilfe dieser System Richtlinie können Sie angeben, dass der Windows Installer während einer verwalteten Installation mithilfe erweiterter Berechtigungen Alle öffentlichen Eigenschaften an die Serverseite übergibt.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: Enableusercontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130685"
---
# <a name="enableusercontrol"></a><span data-ttu-id="63232-103">Enableusercontrol</span><span class="sxs-lookup"><span data-stu-id="63232-103">EnableUserControl</span></span>

<span data-ttu-id="63232-104">Im Fall einer verwalteten Installation muss der Paket Ersteller möglicherweise einschränken, welche öffentlichen Eigenschaften an die Serverseite übermittelt werden, und er kann von einem Benutzer geändert werden, der kein Systemadministrator ist.</span><span class="sxs-lookup"><span data-stu-id="63232-104">In the case of a managed installation, the package author may need to limit which public properties are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="63232-105">Einige Einschränkungen sind im allgemeinen erforderlich, um eine sichere Umgebung zu verwalten, wenn die Installation erfordert, dass das Installationsprogramm erweiterte Berechtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="63232-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span>

<span data-ttu-id="63232-106">Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf "1" festgelegt ist, kann das Installationsprogramm während einer verwalteten Installation mit erweiterten Berechtigungen alle [öffentlichen Eigenschaften](public-properties.md) an die Serverseite übergeben.</span><span class="sxs-lookup"><span data-stu-id="63232-106">If this per-machine [system policy](system-policy.md) is set to "1", then the installer can pass all [public properties](public-properties.md) to the server side during a managed installation using elevated privileges.</span></span> <span data-ttu-id="63232-107">Das Festlegen dieser Richtlinie hat dieselbe Auswirkung wie das Festlegen der **enableusercontrol** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="63232-107">Setting this policy has the same effect as setting the **EnableUserControl** property.</span></span> <span data-ttu-id="63232-108">Wenn Sie diese Richtlinie festlegen, können alle öffentlichen Eigenschaften an den Dienst übermittelt werden und können von nicht Administratoren geändert werden.</span><span class="sxs-lookup"><span data-stu-id="63232-108">Setting this policy allows all public properties to be passed to the service and to be changeable by nonadministrative users.</span></span> <span data-ttu-id="63232-109">Diese Richtlinie ist standardmäßig nicht aktiviert. nur eingeschränkte öffentliche Eigenschaften werden an die Serverseite übermittelt und können von einem nicht Administrator geändert werden.</span><span class="sxs-lookup"><span data-stu-id="63232-109">By default, this policy is not enabled; only restricted public properties are passed to the server side and changeable by a nonadministrative user.</span></span> <span data-ttu-id="63232-110">Alle anderen öffentlichen Eigenschaften werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63232-110">All other public properties are ignored.</span></span>

<span data-ttu-id="63232-111">Wenn das Betriebssystem Windows 2000 ist, ist der Benutzer kein Systemadministrator, und die Anwendung bzw. das Produkt wird mit erhöhten Rechten installiert. ein Benutzer, der kein Systemadministrator ist, kann nur eine genehmigte Liste von eingeschränkten öffentlichen Eigenschaften außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="63232-111">If the operating system is Windows 2000, the user is not a system administrator, and the application or product is being installed with elevated privileges, then a user that is not a system administrator can only override an approved list of restricted public properties.</span></span> <span data-ttu-id="63232-112">Weitere Informationen finden Sie unter [Eingeschränkte öffentliche Eigenschaften](restricted-public-properties.md).</span><span class="sxs-lookup"><span data-stu-id="63232-112">For more information see [Restricted Public Properties](restricted-public-properties.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="63232-113">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="63232-113">Registry Key</span></span>

<span data-ttu-id="63232-114">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="63232-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="63232-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="63232-115">Data Type</span></span>

<span data-ttu-id="63232-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="63232-116">**REG\_DWORD**</span></span>

 

 



