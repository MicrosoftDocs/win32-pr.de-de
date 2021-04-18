---
description: Beim Systemstart startet der SCM alle automatischen Start Dienste und die Dienste, von denen Sie abhängig sind. Wenn z. b. ein Auto Start Dienst von einem Dienst zum Starten von Start abhängig ist, wird der Dienst für die Dienst Nachfrage ebenfalls automatisch gestartet.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Dienste werden automatisch gestartet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340176"
---
# <a name="automatically-starting-services"></a><span data-ttu-id="57273-104">Dienste werden automatisch gestartet</span><span class="sxs-lookup"><span data-stu-id="57273-104">Automatically Starting Services</span></span>

<span data-ttu-id="57273-105">Beim Systemstart startet der SCM alle automatischen Start Dienste und die Dienste, von denen Sie abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="57273-105">During system boot, the SCM starts all auto-start services and the services on which they depend.</span></span> <span data-ttu-id="57273-106">Wenn z. b. ein Auto Start Dienst von einem Dienst zum Starten von Start abhängig ist, wird der Dienst für die Dienst Nachfrage ebenfalls automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="57273-106">For example, if an auto-start service depends on a demand-start service, the demand-start service is also started automatically.</span></span>

<span data-ttu-id="57273-107">Die Lade Reihenfolge wird durch Folgendes bestimmt:</span><span class="sxs-lookup"><span data-stu-id="57273-107">The load order is determined by the following:</span></span>

1.  <span data-ttu-id="57273-108">Die Reihenfolge der Gruppen in der Gruppenliste der Lade Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="57273-108">The order of groups in the load ordering group list.</span></span> <span data-ttu-id="57273-109">Diese Informationen werden im Wert " **servicegrouporder** " im folgenden Registrierungsschlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="57273-109">This information is stored in the **ServiceGroupOrder** value in the following registry key:</span></span>

    <span data-ttu-id="57273-110">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet- \\ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="57273-110">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

    <span data-ttu-id="57273-111">Um die Gruppe der Lade Reihen für einen Dienst anzugeben, verwenden Sie den *lploadordergroup* - [**Parameter der Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) "Funktion" oder " [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ".</span><span class="sxs-lookup"><span data-stu-id="57273-111">To specify the load ordering group for a service, use the *lpLoadOrderGroup* parameter of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) or [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function.</span></span>

2.  <span data-ttu-id="57273-112">Die Reihenfolge der Dienste innerhalb einer Gruppe, die im Bestellungs Vektor für Tags angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="57273-112">The order of services within a group specified in the tags order vector.</span></span> <span data-ttu-id="57273-113">Diese Informationen werden im folgenden Registrierungsschlüssel im **grouporderlist** -Wert gespeichert:</span><span class="sxs-lookup"><span data-stu-id="57273-113">This information is stored in the **GroupOrderList** value in the following registry key:</span></span>

    <span data-ttu-id="57273-114">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet- \\ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="57273-114">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

3.  <span data-ttu-id="57273-115">Die für jeden Dienst aufgelisteten Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="57273-115">The dependencies listed for each service.</span></span>

<span data-ttu-id="57273-116">Nach Abschluss des Starts führt das System das Start Überprüfungs Programm aus, das vom Wert " **bootverificationprogram** " des folgenden Registrierungsschlüssels angegeben wird: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control**.</span><span class="sxs-lookup"><span data-stu-id="57273-116">When the boot is complete, the system executes the boot verification program specified by the **BootVerificationProgram** value of the following registry key: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control**.</span></span>

<span data-ttu-id="57273-117">Standardmäßig ist dieser Wert nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="57273-117">By default, this value is not set.</span></span> <span data-ttu-id="57273-118">Das System meldet einfach, dass der Start erfolgreich war, nachdem sich der erste Benutzer angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="57273-118">The system simply reports that the boot was successful after the first user has logged on.</span></span> <span data-ttu-id="57273-119">Sie können ein Start Überprüfungs Programm bereitstellen, das das System auf Probleme überprüft und den Startstatus mithilfe der [**notifybootconfigstatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) -Funktion an den SCM meldet.</span><span class="sxs-lookup"><span data-stu-id="57273-119">You can supply a boot verification program that checks the system for problems and reports the boot status to the SCM using the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>

<span data-ttu-id="57273-120">Nach einem erfolgreichen Start speichert das System einen Klon der Datenbank in der Konfiguration mit den letzten bekannten Voreinstellungen.</span><span class="sxs-lookup"><span data-stu-id="57273-120">After a successful boot, the system saves a clone of the database in the last-known-good (LKG) configuration.</span></span> <span data-ttu-id="57273-121">Das System kann diese Kopie der Datenbank wiederherstellen, wenn die an der aktiven Datenbank vorgenommenen Änderungen dazu führen, dass der Systemneustart fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="57273-121">The system can restore this copy of the database if changes made to the active database cause the system reboot to fail.</span></span> <span data-ttu-id="57273-122">Der Registrierungsschlüssel für diese Datenbank lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="57273-122">The following is the registry key for this database:</span></span>

<span data-ttu-id="57273-123">**Lokale HKEY- \_ \_ Computer- \\ \\ Controlset *xxx*- \\ Dienste**</span><span class="sxs-lookup"><span data-stu-id="57273-123">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\ControlSet *XXX*\\Services**</span></span>

<span data-ttu-id="57273-124">Dabei ist *xxx* der Wert, der im folgenden Registrierungs Wert gespeichert wird: **HKEY \_ local \_ Machine \\ System \\ Select \\ LastKnownGood**.</span><span class="sxs-lookup"><span data-stu-id="57273-124">where *XXX* is the value saved in the following registry value: **HKEY\_LOCAL\_MACHINE\\System\\Select\\LastKnownGood**.</span></span>

<span data-ttu-id="57273-125">Wenn ein automatischer Start Dienst mit einer \_ \_ Fehler Steuerungsebene des Dienst Fehlers nicht gestartet werden kann, startet der SCM den Computer mithilfe der LKG-Konfiguration neu.</span><span class="sxs-lookup"><span data-stu-id="57273-125">If an auto-start service with a SERVICE\_ERROR\_CRITICAL error control level fails to start, the SCM reboots the computer using the LKG configuration.</span></span> <span data-ttu-id="57273-126">Wenn die LKG-Konfiguration bereits verwendet wird, tritt beim Starten ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="57273-126">If the LKG configuration is already being used, the boot fails.</span></span>

<span data-ttu-id="57273-127">Ein Dienst für automatisches Starten kann als verzögerter Dienst für automatisches Starten konfiguriert werden, indem die [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) -Funktion \_ mit \_ verzögerten \_ automatischen \_ Start \_ Informationen für die Dienst Konfiguration aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="57273-127">An auto-start service can be configured as a delayed auto-start service by calling the [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function with SERVICE\_CONFIG\_DELAYED\_AUTO\_START\_INFO.</span></span> <span data-ttu-id="57273-128">Diese Änderung tritt nach dem nächsten Systemstart in Kraft.</span><span class="sxs-lookup"><span data-stu-id="57273-128">This change takes effect after the next system boot.</span></span> <span data-ttu-id="57273-129">Weitere Informationen finden Sie unter [**Dienst \_ verzögerte \_ automatische \_ Start \_ Informationen**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span><span class="sxs-lookup"><span data-stu-id="57273-129">For more information, see [**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span></span>

 

 



