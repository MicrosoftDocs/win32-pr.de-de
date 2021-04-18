---
title: Aktivieren der com-Sicherheit mithilfe von DCOMCNFG
description: "\"Dcomcnfg.exe\" verfügt über eine Benutzeroberfläche, über die Sie bestimmte Einstellungen in der Registrierung ändern können."
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340422"
---
# <a name="enabling-com-security-using-dcomcnfg"></a><span data-ttu-id="d2338-103">Aktivieren der com-Sicherheit mithilfe von DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="d2338-103">Enabling COM Security Using DCOMCNFG</span></span>

<span data-ttu-id="d2338-104">"Dcomcnfg.exe" verfügt über eine Benutzeroberfläche, über die Sie bestimmte Einstellungen in der Registrierung ändern können.</span><span class="sxs-lookup"><span data-stu-id="d2338-104">Dcomcnfg.exe provides a user interface for modifying certain settings in the registry.</span></span> <span data-ttu-id="d2338-105">Mithilfe von Dcomcnfg.exe können Sie die Sicherheit entweder auf Computer-oder Prozessebene aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d2338-105">By using Dcomcnfg.exe, you can enable security either on a computer-wide or a process-wide basis.</span></span> <span data-ttu-id="d2338-106">Sie können die Sicherheit für einen bestimmten Computer aktivieren, sodass, wenn ein Prozess weder Programm gesteuert noch durch Registrierungs Werte seine eigenen Sicherheitseinstellungen bereitstellt, die von Dcomcnfg.exe festgelegten Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2338-106">You can enable security for a particular computer so that when a process does not provide its own security settings, either programmatically or through registry values, the values set by Dcomcnfg.exe will be used.</span></span> <span data-ttu-id="d2338-107">Oder Sie können Dcomcnfg.exe verwenden, um die Sicherheit nur für eine bestimmte Anwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d2338-107">Or you can use Dcomcnfg.exe to enable security for a particular application only.</span></span>

<span data-ttu-id="d2338-108">Wenn Sie die Sicherheit aktivieren, müssen Sie zwei Hauptaufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="d2338-108">When enabling security, there are two primary tasks to accomplish:</span></span>

-   <span data-ttu-id="d2338-109">Legen Sie eine Authentifizierungs Ebene fest, die nicht "None" ist.</span><span class="sxs-lookup"><span data-stu-id="d2338-109">Set an authentication level that is not None.</span></span>
-   <span data-ttu-id="d2338-110">Legen Sie Berechtigungen fest, einschließlich Start-und Zugriffsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="d2338-110">Set permissions, including both launch and access permissions.</span></span>

<span data-ttu-id="d2338-111">Die Schritte, die zum Ausführen dieser Aufgaben ausgeführt werden, hängen davon ab, ob Sie die Sicherheit für den gesamten Computer oder nur für eine bestimmte Anwendung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d2338-111">The steps taken to accomplish these tasks depend on whether you are enabling security for the whole computer or just for a particular application.</span></span> <span data-ttu-id="d2338-112">Sie können auch andere Werte für den Computer oder die Anwendung festlegen.</span><span class="sxs-lookup"><span data-stu-id="d2338-112">Also, you may want to set other values for the computer or application.</span></span>

> [!Note]  
> <span data-ttu-id="d2338-113">Sie müssen ein Administrator sein, um Dcomcnfg.exe ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="d2338-113">You must be an administrator to run Dcomcnfg.exe.</span></span>

 

<span data-ttu-id="d2338-114">Die folgenden Themen enthalten Schritt-für-Schritt-Anleitungen zum Festlegen der Sicherheit mit Dcomcnfg.exe:</span><span class="sxs-lookup"><span data-stu-id="d2338-114">The following topics provide step-by-step procedures on how to set security with Dcomcnfg.exe:</span></span>

-   [<span data-ttu-id="d2338-115">Festlegen der System-Wide Sicherheit mithilfe von DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="d2338-115">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="d2338-116">Festlegen der Processwide-Sicherheit mithilfe von DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="d2338-116">Setting Processwide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="d2338-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2338-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2338-118">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="d2338-118">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="d2338-119">Ausschalten der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d2338-119">Turning Off Security</span></span>](turning-off-security.md)
</dt> </dl>

 

 




