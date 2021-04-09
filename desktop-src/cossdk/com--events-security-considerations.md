---
description: Wenn Sie den com+-Ereignis Dienst verwenden, müssen Sie Maßnahmen ergreifen, um sicherzustellen, dass alle in einem Ereignis enthaltenen vertraulichen Informationen nicht gefährdet sind.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Sicherheitsüberlegungen für COM+-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958629"
---
# <a name="com-events-security-considerations"></a><span data-ttu-id="abcc6-103">Sicherheitsüberlegungen für COM+-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="abcc6-103">COM+ Events Security Considerations</span></span>

<span data-ttu-id="abcc6-104">Wenn Sie den com+-Ereignis Dienst verwenden, müssen Sie Maßnahmen ergreifen, um sicherzustellen, dass alle in einem Ereignis enthaltenen vertraulichen Informationen nicht gefährdet sind.</span><span class="sxs-lookup"><span data-stu-id="abcc6-104">When using the COM+ events service, there are steps you can take to ensure that any sensitive information contained in an event is not compromised.</span></span>

<span data-ttu-id="abcc6-105">Ereignis Herausgeber sollten bedenken, dass jede Partei, die in den com+-Katalog schreiben kann, Ihre Ereignisse abonnieren kann.</span><span class="sxs-lookup"><span data-stu-id="abcc6-105">Event publishers should keep in mind that any party that can write to your COM+ catalog can subscribe to your events.</span></span> <span data-ttu-id="abcc6-106">Wenn die in einem Ereignis Klassenobjekt enthaltenen Informationen sensibel sind, sollten Sie daher mithilfe des Verwaltungs Tools Komponenten Dienste überprüfen, ob die Kommunikation mit Abonnenten für die Anwendung, die die Ereignis Klassen Komponenten enthält, verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="abcc6-106">Therefore, if the information contained in an event class object is sensitive, you should use the Component Services administration tool to verify that communications with subscribers are encrypted for the application that contains the event class components.</span></span> <span data-ttu-id="abcc6-107">(Wählen Sie im Eigenschaften Blatt der com+-Anwendung auf der Registerkarte **Sicherheit** die Option **Paket Datenschutz** als **Authentifizierungs Ebene für die Einstellung Aufrufe aus** .) Außerdem sollten Sie [Ereignis Filter](filtering-events-in-com-.md) verwenden, um sicherzustellen, dass Ereignisse nur an die entsprechenden Abonnenten übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="abcc6-107">(On the **Security** tab of the COM+ application property sheet, select **Packet Privacy** as the **Authentication Level for Calls** setting.) Also, you should use [event filters](filtering-events-in-com-.md) to help ensure that events are delivered only to the appropriate subscribers.</span></span>

<span data-ttu-id="abcc6-108">Ereignis Abonnenten sollten bedenken, dass eine böswillige Partei mit Zugriff auf Ihr Netzwerk und das Wissen Ihres Ereignis Klassen Objekts falsche Ereignisse erstellen könnte.</span><span class="sxs-lookup"><span data-stu-id="abcc6-108">Event subscribers should keep in mind that a malicious party with access to your network and knowledge of your event class object could create false events.</span></span> <span data-ttu-id="abcc6-109">Daher sollten Sie die [rollenbasierte Sicherheit](role-based-security-administration.md) verwenden, um sicherzustellen, dass Aufrufer der Methoden des Ereignis Klassen Objekts über die entsprechenden Anmelde Informationen verfügen, um die von der Implementierung beschriebenen Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="abcc6-109">You should therefore use [role-based security](role-based-security-administration.md) to help ensure that callers of your event class object's methods have appropriate credentials to perform the actions described by your implementation.</span></span>

<span data-ttu-id="abcc6-110">Verwenden Sie zum Schutz von Verlegern und Abonnenten den com+-Ereignis Dienst in einem privaten Netzwerk vertrauenswürdiger Hosts, die von einer Firewall aus dem Internet isoliert sind.</span><span class="sxs-lookup"><span data-stu-id="abcc6-110">To help protect both publishers and subscribers, use the COM+ Events service on a private network of trusted hosts that is isolated from the Internet by a firewall.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abcc6-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="abcc6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abcc6-112">Com+-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="abcc6-112">COM+ Security</span></span>](com--security.md)
</dt> <dt>

[<span data-ttu-id="abcc6-113">Filtern von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="abcc6-113">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="abcc6-114">Das com+-Ereignis Klassenobjekt</span><span class="sxs-lookup"><span data-stu-id="abcc6-114">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



