---
description: Zugriffssteuerung
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Access Control (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868272"
---
# <a name="access-control-wpd-api"></a><span data-ttu-id="891c6-103">Access Control (WPD-API)</span><span class="sxs-lookup"><span data-stu-id="891c6-103">Access Control (WPD API)</span></span>

<span data-ttu-id="891c6-104">Der Windows-Treibermodell (WDM) unterstützt die Beschränkung des Geräte Zugriffs über Access Control Listen (ACLs) auf dem Plug & Play (PNP)-Geräteknoten.</span><span class="sxs-lookup"><span data-stu-id="891c6-104">The Windows Driver Model (WDM) supports restricting device access via Access Control Lists (ACLs) on the Plug and Play (PnP) Device Nodes.</span></span> <span data-ttu-id="891c6-105">Dies bedeutet, dass Anbieter und Netzwerkadministratoren den Zugriff auf jeden Gerätetyp einschränken können.</span><span class="sxs-lookup"><span data-stu-id="891c6-105">This means that vendors and network administrators can restrict access to any device type.</span></span> <span data-ttu-id="891c6-106">Wenn eine Anwendung ein Handle für einen Treiber durch Aufrufen von [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)öffnet, überprüft der e/a-Manager des Treibers, ob der angegebene Benutzer über die erforderlichen Zugriffsrechte verfügt, und auf ähnliche Weise prüft der Zugriff, wenn IOCTLs von diesem Handle an den Treiber gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="891c6-106">When an application opens a handle to a driver by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), the driver's I/O Manager verifies whether the given user has the required access, and similarly does access checks when IOCTLs are sent to the driver from that handle.</span></span>

<span data-ttu-id="891c6-107">Ein Netzwerkadministrator könnte beispielsweise Gastbenutzer auf den schreibgeschützten Zugriff für tragbare Geräte beschränken und authentifizierten Benutzern Lese-/Schreibzugriff gewähren.</span><span class="sxs-lookup"><span data-stu-id="891c6-107">For example, a network administrator could restrict Guest users to read-only access for portable devices, while they could grant Authenticated users read/write access.</span></span> <span data-ttu-id="891c6-108">In diesem Fall bedeutet dies, dass ein Gast einen WPD-Befehl ausgegeben hat, der Lese-/Schreibzugriff erforderte (z. b. Delete-Objekt). der Fehler tritt auf, wenn ein authentifizierter Benutzer denselben Befehl ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="891c6-108">In this case, it implies that if a Guest issued a WPD command that required read/write access (such as Delete Object); it would fail with Access Denied, whereas if an Authenticated user issued the same command, it would succeed.</span></span>

<span data-ttu-id="891c6-109">Die Gruppenrichtlinie Einträge zum Steuern des Zugriffs auf Wechselmedien und tragbare Geräte sind tatsächlich nichts anderes als eine einfache Möglichkeit für Administratoren, PNP-Geräteknoten-ACLs gleichzeitig auf eine ganze Klasse von Geräten anzuwenden (z. b. durch Anwenden der "Schreibzugriff auf tragbare Geräte verweigern" Gruppenrichtlinie die ACLs aller WPD-Geräte so anpassen, dass der Schreibzugriff verweigert wird).</span><span class="sxs-lookup"><span data-stu-id="891c6-109">The Group Policy entries for controlling access to removable storage and portable devices is actually nothing more than an easy way for Administrators to apply PnP device node ACLs to a whole class of devices at a time (for example, applying the "Deny Write Access to Portable Devices" Group Policy would adjust the ACLs of all WPD devices to deny write access).</span></span>

## <a name="io-control-codes-in-wpd"></a><span data-ttu-id="891c6-110">E/a-Steuerungs Codes in WPD</span><span class="sxs-lookup"><span data-stu-id="891c6-110">I/O Control Codes in WPD</span></span>

<span data-ttu-id="891c6-111">WPD-Anwendungen kommunizieren mit Treibern, indem Sie Geräte Handles öffnen und e/a-Kontroll Codes (IOCTLs) senden.</span><span class="sxs-lookup"><span data-stu-id="891c6-111">WPD applications communicate with drivers by opening device handles and sending I/O Control Codes (IOCTLs).</span></span> <span data-ttu-id="891c6-112">Diese IOCTLs bestehen aus vier Abschnitten:</span><span class="sxs-lookup"><span data-stu-id="891c6-112">These IOCTLs consist of four sections:</span></span>

1.  <span data-ttu-id="891c6-113">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="891c6-113">Device Type</span></span>
2.  <span data-ttu-id="891c6-114">Funktions Code</span><span class="sxs-lookup"><span data-stu-id="891c6-114">Function Code</span></span>
3.  <span data-ttu-id="891c6-115">Buffer-Methode</span><span class="sxs-lookup"><span data-stu-id="891c6-115">Buffer Method</span></span>
4.  <span data-ttu-id="891c6-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="891c6-116">Access Type</span></span>

<span data-ttu-id="891c6-117">Der vierte Abschnitt, der Zugriffstyp, gibt die jeweilige Zugriffs Anforderung für den angegebenen Befehl an.</span><span class="sxs-lookup"><span data-stu-id="891c6-117">The fourth section, the Access Type, specifies the specific access requirement for the given command.</span></span> <span data-ttu-id="891c6-118">Der e/a-Manager des Treibers verwendet diese Daten zum Durchführen der Überprüfung der Access Control Liste (ACL).</span><span class="sxs-lookup"><span data-stu-id="891c6-118">The driver's I/O manager uses this data to perform the Access Control List (ACL) check.</span></span>

<span data-ttu-id="891c6-119">Wenn ein IOCTL-Element wie folgt definiert wurde:</span><span class="sxs-lookup"><span data-stu-id="891c6-119">So if an IOCTL were defined as:</span></span>


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



<span data-ttu-id="891c6-120">Der e/a-Manager des Treibers prüft, ob der Besitzer des Geräte Handles über Lesezugriff auf das Gerät verfügt, wenn diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="891c6-120">The driver's I/O manager would check that the owner of the device handle has read access to the device when this message is sent.</span></span>

<span data-ttu-id="891c6-121">Und, wenn eine ioctl definiert wurde:</span><span class="sxs-lookup"><span data-stu-id="891c6-121">And, if an IOCTL were defined as:</span></span>


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



<span data-ttu-id="891c6-122">Der e/a-Manager des Treibers prüft, ob der Besitzer des Geräte Handles Lese-/Schreibzugriff auf das Gerät hat, wenn diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="891c6-122">The driver's I/O manager would check that the owner of the device handle has read/write access to the device when this message is sent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="891c6-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="891c6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="891c6-124">**Anwendungs Übersicht**</span><span class="sxs-lookup"><span data-stu-id="891c6-124">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="891c6-125">**Iportabledevice:: Open**</span><span class="sxs-lookup"><span data-stu-id="891c6-125">**IPortableDevice::Open**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[<span data-ttu-id="891c6-126">**Iportabledevice:: Send Command**</span><span class="sxs-lookup"><span data-stu-id="891c6-126">**IPortableDevice::SendCommand**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



