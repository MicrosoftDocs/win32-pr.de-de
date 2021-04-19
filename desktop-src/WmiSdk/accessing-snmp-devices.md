---
description: Ermöglicht Client Anwendungen den Zugriff auf SNMP-Informationen über WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Zugreifen auf SNMP-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362996"
---
# <a name="accessing-snmp-devices"></a><span data-ttu-id="c79ac-103">Zugreifen auf SNMP-Geräte</span><span class="sxs-lookup"><span data-stu-id="c79ac-103">Accessing SNMP Devices</span></span>

<span data-ttu-id="c79ac-104">Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Client Anwendungen den Zugriff auf SNMP-Informationen über WMI.</span><span class="sxs-lookup"><span data-stu-id="c79ac-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through WMI.</span></span> <span data-ttu-id="c79ac-105">Der [SNMP-Anbieter](snmp-provider.md) fungiert als Gateway für Systeme und Geräte, die SNMP für die Verwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c79ac-105">The [SNMP provider](snmp-provider.md) acts as a gateway to systems and devices that use SNMP for management.</span></span> <span data-ttu-id="c79ac-106">Nur der Verwaltungs-oder Überwachungscomputer muss WMI ausführen, da er von einem beliebigen SNMP-fähigen Gerät gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c79ac-106">Only the management or monitoring computer must be running WMI because it can read from any SNMP-enabled device.</span></span>

> [!Note]  
> <span data-ttu-id="c79ac-107">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c79ac-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="c79ac-108">Die Objektvariablen der SNMP-Management Information Base (MIB) können aus gelesen und geschrieben werden. SNMP-Traps können automatisch WMI-Ereignissen zugeordnet werden, die für beliebige Erstellungs-, Lösch-oder Aktualisierungs Vorgänge für Daten außerhalb der MIB-definierten Traps definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="c79ac-108">SNMP Management Information Base (MIB) object variables can be read from and written to, and SNMP traps can be automatically mapped to WMI events, which can be defined for any arbitrary create, delete, or update operations to data beyond the MIB-defined traps.</span></span> <span data-ttu-id="c79ac-109">Diese Funktion von WMI fungiert als Erweiterung von SNMP-Standardfunktionen.</span><span class="sxs-lookup"><span data-stu-id="c79ac-109">This feature of WMI functions as an extension of standard SNMP capabilities.</span></span> <span data-ttu-id="c79ac-110">Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="c79ac-110">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

<span data-ttu-id="c79ac-111">Die in den folgenden Themen beschriebenen Tools sind für die Verwendung durch Windows Scripting und C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="c79ac-111">The tools described in the following topics are designed for use by Windows scripting and C/C++ programmers.</span></span> <span data-ttu-id="c79ac-112">Es wird empfohlen, sich mit WMI, SNMPv1 und SNMPv2C vertraut zu machen und ein Wissen über Netzwerk-und Netzwerk Verwaltungs Konzepte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c79ac-112">Familiarity with WMI, SNMPv1 and SNMPv2C, and a working knowledge of networking and network management concepts are recommended.</span></span>

<span data-ttu-id="c79ac-113">Weitere Informationen zur Verwendung von WMI mit SNMP finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c79ac-113">For more information about using WMI with SNMP, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

 



