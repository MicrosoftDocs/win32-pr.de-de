---
title: Point-to-Point-Protokoll über Ethernet-Verbindungen
description: Windows Server 2003, Windows XP und spätere Betriebssysteme bieten Unterstützung für Point-to-Point-Protokoll over Ethernet (PPPoE). Legen Sie für eine PPPoE-Verbindung die folgenden Werte in der rasentry-Struktur fest.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949041"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a><span data-ttu-id="21b24-104">Point-to-Point-Protokoll über Ethernet-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="21b24-104">Point-to-Point Protocol over Ethernet Connections</span></span>

<span data-ttu-id="21b24-105">Windows Server 2003, Windows XP und spätere Betriebssysteme bieten Unterstützung für Point-to-Point-Protokoll over Ethernet (PPPoE).</span><span class="sxs-lookup"><span data-stu-id="21b24-105">Windows Server 2003, Windows XP, and later operating systems provide support for Point-to-Point Protocol over Ethernet (PPPoE).</span></span> <span data-ttu-id="21b24-106">Legen Sie für eine PPPoE-Verbindung die folgenden Werte in der [**rasentry**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="21b24-106">For a PPPoE connection, set the following values in the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure.</span></span>



| <span data-ttu-id="21b24-107">Member</span><span class="sxs-lookup"><span data-stu-id="21b24-107">Member</span></span>                      | <span data-ttu-id="21b24-108">Wert</span><span class="sxs-lookup"><span data-stu-id="21b24-108">Value</span></span>             |
|-----------------------------|-------------------|
| <span data-ttu-id="21b24-109">Rasentry. dwType</span><span class="sxs-lookup"><span data-stu-id="21b24-109">RASENTRY.dwType</span></span>             | <span data-ttu-id="21b24-110">Breitband- \_ Breitband</span><span class="sxs-lookup"><span data-stu-id="21b24-110">RASET\_Broadband</span></span>  |
| <span data-ttu-id="21b24-111">Raentry. szde vicetype</span><span class="sxs-lookup"><span data-stu-id="21b24-111">RAENTRY.szDeviceType</span></span>        | <span data-ttu-id="21b24-112">Rasdt \_ PPPoE</span><span class="sxs-lookup"><span data-stu-id="21b24-112">RASDT\_PPPoE</span></span>      |
| <span data-ttu-id="21b24-113">Rasentry. szlocalphonenumber</span><span class="sxs-lookup"><span data-stu-id="21b24-113">RASENTRY.szLocalPhoneNumber</span></span> | <span data-ttu-id="21b24-114">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="21b24-114">The service name.</span></span> |



 

<span data-ttu-id="21b24-115">Verwenden Sie die [**rassetentryproperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) -Funktion, um diese Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="21b24-115">Use the [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) function to set these values.</span></span>

<span data-ttu-id="21b24-116">Sie können auch die Datei " [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) " und das Flag "rasedflag \_ newbroadbandentry" für " [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) " verwenden, um einen Assistenten zum Erstellen eines PPPoE Phonebook-Eintrags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="21b24-116">You can also use [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) and the RASEDFLAG\_NewBroadbandEntry flag for [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) to display a wizard for creating a PPPoE phonebook entry.</span></span>

 

 