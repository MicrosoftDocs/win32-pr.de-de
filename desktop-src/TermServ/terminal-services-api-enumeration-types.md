---
title: API-Enumerationstypen Remotedesktopdienste
description: Listet Enumerationstypen auf, die mit der Remotedesktopdienste-API verwendet werden.
ms.assetid: b5ef61e2-07fa-4963-9b9b-977cc04dab10
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9523a7528fddff4e2dbcf6dde16c29084d4811d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310344"
---
# <a name="remote-desktop-services-api-enumeration-types"></a><span data-ttu-id="11130-103">API-Enumerationstypen Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="11130-103">Remote Desktop Services API Enumeration Types</span></span>

<span data-ttu-id="11130-104">Die folgenden Enumerationstypen werden mit der Remotedesktopdienste-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="11130-104">The following enumeration types are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11130-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="11130-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="11130-106">**WTS- \_ Konfigurations \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="11130-106">**WTS\_CONFIG\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_class)
</dt> <dd>

<span data-ttu-id="11130-107">Enthält Werte, die den Typ der Benutzer Konfigurationsinformationen angeben, die in einem Aufrufen der [**wzqueryuserconfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) -und [**wtsetuserconfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) -Funktionen festgelegt oder abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11130-107">Contains values that indicate the type of user configuration information to set or retrieve in a call to the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) and [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-108">**WTS- \_ Konfigurations \_ Quelle**</span><span class="sxs-lookup"><span data-stu-id="11130-108">**WTS\_CONFIG\_SOURCE**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_source)
</dt> <dd>

<span data-ttu-id="11130-109">Gibt die Quelle der Konfigurationsinformationen an, die von der [**wzqueryuserconfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="11130-109">Specifies the source of configuration information returned by the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) function.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-110">**WTS \_ connectstate- \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="11130-110">**WTS\_CONNECTSTATE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_connectstate_class)
</dt> <dd>

<span data-ttu-id="11130-111">Gibt den Verbindungsstatus einer Remotedesktopdienste Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="11130-111">Specifies the connection state of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-112">**WTS- \_ Informations \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="11130-112">**WTS\_INFO\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_info_class)
</dt> <dd>

<span data-ttu-id="11130-113">Enthält Werte, die den Typ der Sitzungsinformationen angeben, die bei einem Aufrufen der [**wzquerysessioninformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) -Funktion abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11130-113">Contains values that indicate the type of session information to retrieve in a call to the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-114">**WTS \_ - \_ Typklasse**</span><span class="sxs-lookup"><span data-stu-id="11130-114">**WTS\_TYPE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_type_class)
</dt> <dd>

<span data-ttu-id="11130-115">Gibt den Strukturtyp an, den eine Remotedesktopdienste Funktion in einem Puffer zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="11130-115">Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-116">**virtuelle WTS- \_ \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="11130-116">**WTS\_VIRTUAL\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_virtual_class)
</dt> <dd>

<span data-ttu-id="11130-117">Enthält Werte, die den Typ der abzurufenden Informationen des virtuellen Kanals angeben.</span><span class="sxs-lookup"><span data-stu-id="11130-117">Contains values that indicate the type of virtual channel information to retrieve.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-118">**wtssbx- \_ Adress \_ Familie**</span><span class="sxs-lookup"><span data-stu-id="11130-118">**WTSSBX\_ADDRESS\_FAMILY**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_address_family)
</dt> <dd>

<span data-ttu-id="11130-119">Enthält Werte, die die Adressfamilie einer Netzwerkadresse angeben, die für die Umleitung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11130-119">Contains values that indicate the address family of a network address that is being used for redirection.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-120">**wtssbx- \_ Computer \_ Ableitung**</span><span class="sxs-lookup"><span data-stu-id="11130-120">**WTSSBX\_MACHINE\_DRAIN**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_drain)
</dt> <dd>

<span data-ttu-id="11130-121">Enthält Werte, die den Ausgleichs Status eines Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servers angeben.</span><span class="sxs-lookup"><span data-stu-id="11130-121">Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-122">**wtssbx- \_ Computer \_ Sitzungs \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="11130-122">**WTSSBX\_MACHINE\_SESSION\_MODE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_session_mode)
</dt> <dd>

<span data-ttu-id="11130-123">Enthält Werte, die den Sitzungs Modus eines RD-Sitzungshost Servers angeben.</span><span class="sxs-lookup"><span data-stu-id="11130-123">Contains values that indicate the session mode of a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-124">**wtssbx- \_ Computer \_ Status**</span><span class="sxs-lookup"><span data-stu-id="11130-124">**WTSSBX\_MACHINE\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_state)
</dt> <dd>

<span data-ttu-id="11130-125">Enthält Werte, die den aktuellen Status eines Servers angeben.</span><span class="sxs-lookup"><span data-stu-id="11130-125">Contains values that indicate the current state of a server.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-126">**wtssbx \_ - \_ Benachrichtigungstyp**</span><span class="sxs-lookup"><span data-stu-id="11130-126">**WTSSBX\_NOTIFICATION\_TYPE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type)
</dt> <dd>

<span data-ttu-id="11130-127">Enthält Werte, die den Typ der Statusänderung angeben, die auf einem RD-Sitzungshost Server oder einer Benutzersitzung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="11130-127">Contains values that indicate the type of status change that occurred on a RD Session Host server or a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="11130-128">**wtssbx- \_ Sitzungs \_ Status**</span><span class="sxs-lookup"><span data-stu-id="11130-128">**WTSSBX\_SESSION\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_session_state)
</dt> <dd>

<span data-ttu-id="11130-129">Enthält Werte, die den Verbindungsstatus einer Benutzersitzung angeben.</span><span class="sxs-lookup"><span data-stu-id="11130-129">Contains values that indicate the connection state of a user session.</span></span>

</dd> </dl>

 

 




