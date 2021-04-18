---
description: SNMP-Ereignis Anbieter empfangen SNMP-Ereignis Pakete vom WinSNMP-Stapel und übersetzen die Informationen, die in den Paketen enthalten sind, in WMI-Ereignisse.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Auswählen zwischen SNMP-Ereignis Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352227"
---
# <a name="choosing-between-snmp-event-providers"></a><span data-ttu-id="c053d-103">Auswählen zwischen SNMP-Ereignis Anbietern</span><span class="sxs-lookup"><span data-stu-id="c053d-103">Choosing Between SNMP Event Providers</span></span>

<span data-ttu-id="c053d-104">SNMP-Ereignis Anbieter empfangen SNMP-Ereignis Pakete vom WinSNMP-Stapel und übersetzen die Informationen, die in den Paketen enthalten sind, in WMI-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="c053d-104">SNMP event providers receive SNMP event packets from the WINSNMP stack and translate the information included in the packets into WMI events.</span></span>

<span data-ttu-id="c053d-105">WMI umfasst die folgenden zwei SNMP-Ereignis Anbieter:</span><span class="sxs-lookup"><span data-stu-id="c053d-105">WMI includes the following two SNMP event providers:</span></span>

-   <span data-ttu-id="c053d-106">SNMP-gekapselter Ereignis Anbieter (SEEP)</span><span class="sxs-lookup"><span data-stu-id="c053d-106">SNMP Encapsulated Event provider (SEEP)</span></span>

    <span data-ttu-id="c053d-107">Gekapselte Bereitstellung bedeutet, dass die Ereignis Instanz einfache Eigenschaften hat, die die direkt aus dem SNMP-Trap zugeordneten Informationen beschreiben</span><span class="sxs-lookup"><span data-stu-id="c053d-107">Encapsulated provision means that the event instance has simple properties describing the information mapped directly from the SNMP trap.</span></span>

-   <span data-ttu-id="c053d-108">SNMP-Referenz Ereignis Anbieter (SREP)</span><span class="sxs-lookup"><span data-stu-id="c053d-108">SNMP Referent Event provider (SREP)</span></span>

    <span data-ttu-id="c053d-109">Die Bereitstellung von Referenten abstrahiert die Informationen, die innerhalb des SNMP-Traps vorhanden sind, sodass Eigenschaften, die dieselbe Klasse und Instanz gemeinsam verwenden, als eingebettete Objekte</span><span class="sxs-lookup"><span data-stu-id="c053d-109">Referent provision abstracts the information present within the SNMP trap so that properties which share the same class and instance are presented as embedded objects.</span></span> <span data-ttu-id="c053d-110">Dadurch kann die eindeutige Instanz, mit der der Trap verknüpft ist, nach dem Empfang des Ereignisses mit dem SNMP- \_ \_ RelPath abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c053d-110">This allows for the unique instance, with which the trap is associated, to be retrieved after the receipt of the event, using the SNMP \_\_RELPATH.</span></span>

> [!Note]  
> <span data-ttu-id="c053d-111">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c053d-111">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="c053d-112">Unabhängig davon, ob es sich bei dem SNMP-Ereignis um eine SNMPv1 Trap oder eine SNMPv2C-Benachrichtigung handelt, meldet der Stapel Sie als SNMPv2-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c053d-112">Regardless of whether the SNMP event is an SNMPv1 trap or an SNMPv2C notification, the stack reports it as an SNMPv2 notification.</span></span> <span data-ttu-id="c053d-113">Aus diesem Grund verarbeiten die Ereignis Anbieter alle SNMP-Ereignisse als SNMPv2-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c053d-113">Therefore, the event providers process all SNMP events as SNMPv2 notifications.</span></span>

<span data-ttu-id="c053d-114">Um die SNMP-Ereignisse für WMI-Consumer zu beschreiben, unterstützt jeder Ereignis Anbieter eine Hierarchie von Klassen, die von der [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) -System Klasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c053d-114">To describe the SNMP events to WMI consumers, each event provider supports a hierarchy of classes that derives from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) system class.</span></span> <span data-ttu-id="c053d-115">Die [SnmpNotification](snmpnotification.md) -Klasse ist die übergeordnete Klasse für die-Hierarchie. die [snmpextendednotification](snmpextendednotification.md) -Klasse ist die übergeordnete Klasse der SREP-Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="c053d-115">The [SNMPNotification](snmpnotification.md) class is the parent class for the SEEP hierarchy; the [SNMPExtendedNotification](snmpextendednotification.md) class is the parent class for the SREP hierarchy.</span></span>

 

 



