---
title: LocalService
description: Installiert ein-Objekt als Dienst Anwendung.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Registrierungs Wert für LocalService (com)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858505"
---
# <a name="localservice"></a><span data-ttu-id="3d45c-104">LocalService</span><span class="sxs-lookup"><span data-stu-id="3d45c-104">LocalService</span></span>

<span data-ttu-id="3d45c-105">Installiert ein-Objekt als Dienst Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3d45c-105">Installs an object as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3d45c-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="3d45c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a><span data-ttu-id="3d45c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d45c-107">Remarks</span></span>

<span data-ttu-id="3d45c-108">Zusätzlich zur Ausführung als ausführbare Datei des lokalen Servers (exe) kann ein COM-Objekt sich auch für die Ausführung als Dienst Anwendung Verpacken, wenn es von einem lokalen oder Remote Client aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="3d45c-108">In addition to running as a local server executable (EXE), a COM object may also choose to package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="3d45c-109">-Dienste unterstützen zahlreiche nützliche und Benutzeroberflächen integrierte Verwaltungsfunktionen, einschließlich lokaler und Remote Starts, beenden, anhalten und Neustarts, sowie die Möglichkeit, den Server für die Ausführung unter einem bestimmten Benutzerkonto und einer Fenster Station einzurichten.</span><span class="sxs-lookup"><span data-stu-id="3d45c-109">Services support numerous useful and UI-integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific user account and window station.</span></span>

<span data-ttu-id="3d45c-110">Ein Objekt, das als Dienst geschrieben wird, wird für die Verwendung durch com installiert, indem ein **LocalService** -Wert eingerichtet und eine Standard Dienst Installation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d45c-110">An object written as a service is installed for use by COM by establishing a **LocalService** value and performing a standard service installation.</span></span> <span data-ttu-id="3d45c-111">Der Wert für **LocalService** muss auf den Dienstnamen festgelegt werden, der im **lokalen HKEY- \_ \_ \\ System \\ CurrentControlSet \\ Services** als Standard- **reg \_ SZ** -Wert konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3d45c-111">The **LocalService** value must be set to the service name, as configured in **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services**, as the default **REG\_SZ** value.</span></span>

<span data-ttu-id="3d45c-112">Wenn " **LocalService** " festgelegt ist, wird jede Zeichenfolge, die [**Service Parameters**](serviceparameters.md) zugewiesen ist, beim Starten als Befehlszeilenargument an den Dienst übermittelt.</span><span class="sxs-lookup"><span data-stu-id="3d45c-112">When **LocalService** is set, any string assigned to [**ServiceParameters**](serviceparameters.md) is passed as a command-line argument to the service as it is being launched.</span></span>

<span data-ttu-id="3d45c-113">Die Dienst Konfiguration wird in vielen Situationen bevorzugt, in denen die Funktionen der lokalen und Remote-Dienstverwaltungs-APIs und die Benutzeroberfläche für die Dienste nützlich sein können, die das Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3d45c-113">The service configuration is preferred in many situations where the capabilities of the local and remote service management APIs and user interface might be useful for the services that the object provides.</span></span> <span data-ttu-id="3d45c-114">Beispielsweise sollte die Verwendung des vorhandenen administrativen Frameworks der Dienst Architektur eine offensichtliche Wahl sein, wenn es sich um ein langlebiges Objekt handelt, oder es werden problemlos Konzepte wie das starten, beenden, zurücksetzen oder anhalten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d45c-114">For example, leveraging the existing administrative framework of the service architecture should be an obvious choice if the object is long-lived or readily supports concepts such as starting, stopping, resetting, or pausing.</span></span>

<span data-ttu-id="3d45c-115">Dienste können dynamisch konfiguriert werden, und Sie können so konfiguriert werden, dass Sie automatisch ausgeführt werden, wenn der Computer gestartet wird oder wenn Sie von einer Client Anwendung angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3d45c-115">Services can be dynamically configured and can be configured to run automatically when the machine boots, or to be launched when requested by a client application.</span></span>

<span data-ttu-id="3d45c-116">Wenn Sie Klassen als Dienste implementieren, sollten Sie die folgenden Punkte beachten:</span><span class="sxs-lookup"><span data-stu-id="3d45c-116">If you are implementing classes as services, you should be aware of the following points:</span></span>

-   <span data-ttu-id="3d45c-117">Dieser Wert wird im Gegensatz zum [**LocalServer32**](localserver32.md) -Schlüssel für lokale und Remote Aktivierungs Anforderungen verwendet, wenn " **LocalService** " vorhanden ist und sich auf einen gültigen Dienst bezieht, wird die **LocalServer32** -Taste ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3d45c-117">This value is used in preference to the [**LocalServer32**](localserver32.md) key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>
-   <span data-ttu-id="3d45c-118">Zurzeit kann nur eine einzelne Instanz einer Dienst Anwendung zu einem bestimmten Zeitpunkt auf einem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3d45c-118">Currently, only a single instance of a service application may be running at a given time on a computer.</span></span> <span data-ttu-id="3d45c-119">COM-Dienste müssen daher Ihre Klassen Objekte beim Start mithilfe von REGCLS \_ multipleuse registrieren, um mehrere Clients zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3d45c-119">COM services must therefore register their class objects on launch using REGCLS\_MULTIPLEUSE to support multiple clients.</span></span>
-   <span data-ttu-id="3d45c-120">Um ordnungsgemäß zu starten und zu initialisieren, müssen COM-Dienste, die für die automatische Ausführung beim Starten eines Computers konfiguriert sind, RPCSS in der Liste der abhängigen Dienste enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d45c-120">To launch and initialize properly, COM services configured to run automatically when a machine boots must include RPCSS in their list of dependent services.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d45c-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d45c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d45c-122">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="3d45c-122">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="3d45c-123">**Service Parameters**</span><span class="sxs-lookup"><span data-stu-id="3d45c-123">**ServiceParameters**</span></span>](serviceparameters.md)
</dt> <dt>

[<span data-ttu-id="3d45c-124">Dienste</span><span class="sxs-lookup"><span data-stu-id="3d45c-124">Services</span></span>](/windows/desktop/Services/services)
</dt> </dl>

 

 