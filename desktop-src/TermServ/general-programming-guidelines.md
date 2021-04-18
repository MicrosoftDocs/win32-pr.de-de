---
title: Allgemeine Programmier Richtlinien
description: Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste Umgebung.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340506"
---
# <a name="general-programming-guidelines"></a><span data-ttu-id="ebdc2-103">Allgemeine Programmier Richtlinien</span><span class="sxs-lookup"><span data-stu-id="ebdc2-103">General programming guidelines</span></span>

<span data-ttu-id="ebdc2-104">In den folgenden Abschnitten werden allgemeine Richtlinien zum Entwickeln von Anwendungen in einer Remotedesktopdienste Umgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-104">The following sections provide general guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ebdc2-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ebdc2-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ebdc2-106">Anwendungs Kompatibilitäts Ebene</span><span class="sxs-lookup"><span data-stu-id="ebdc2-106">Application compatibility layer</span></span>](application-compatibility-layer.md)
</dt> <dd>

<span data-ttu-id="ebdc2-107">Zum Ausführen von Legacy Anwendungen in einer Remotedesktopdienste Umgebung können Sie die Remotedesktopdienste Anwendungs Kompatibilitäts Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-107">To run legacy applications in a Remote Desktop Services environment you can use the Remote Desktop Services Application Compatibility layer.</span></span>

</dd> <dt>

[<span data-ttu-id="ebdc2-108">Richtlinien für Client/Server-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ebdc2-108">Client/Server application guidelines</span></span>](client-server-application-guidelines.md)
</dt> <dd>

<span data-ttu-id="ebdc2-109">Client/Server-Anwendungen dürfen nicht davon ausgehen, dass eine einzelne Computerverbindung einer einzelnen Benutzersitzung entspricht.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-109">Client/server applications must not assume that a single computer connection is equivalent to a single user session.</span></span>

</dd> <dt>

[<span data-ttu-id="ebdc2-110">Überwachen von Sitzungs Verbindungen und verbindungsverbindungen</span><span class="sxs-lookup"><span data-stu-id="ebdc2-110">Monitoring session connections and disconnections</span></span>](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

<span data-ttu-id="ebdc2-111">Um eine Anwendung bei Remotedesktopdienste zu registrieren, speichern Sie den Namen der virtuellen Kanal Serveranwendung in der Registrierung, indem Sie einen Unterschlüssel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-111">To register an application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey.</span></span>

</dd> <dt>

[<span data-ttu-id="ebdc2-112">Richtlinien für Peripheriegeräte</span><span class="sxs-lookup"><span data-stu-id="ebdc2-112">Peripheral hardware guidelines</span></span>](peripheral-hardware-guidelines.md)
</dt> <dd>

<span data-ttu-id="ebdc2-113">Wenn Ihr Hardware Gerät nicht für eine Remote Sitzung konzipiert ist, müssen die Anbieter sicherstellen, dass die Gerätetreibersoftware die Deaktivierung der Umleitung des Geräts mithilfe einer System Richtlinie oder Gruppenrichtlinie erzwingt.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-113">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

</dd> <dt>

[<span data-ttu-id="ebdc2-114">Lauf Zeit Verknüpfung mit Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="ebdc2-114">Run-Time linking to Wtsapi32.dll</span></span>](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

<span data-ttu-id="ebdc2-115">Die Anwendung kann die Remotedesktopdienste-API verwenden, um zur Laufzeit dynamisch mit der Wtsapi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-115">Your application can use the Remote Desktop Services API to dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="ebdc2-116">Zu diesem Zweck sollte die Anwendung die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion zum Laden Wtsapi32.dll abrufen.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-116">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span>

</dd> </dl>

 

 