---
title: Ermitteln von Bluetooth-Geräten und -Diensten
description: Um die Ermittlung von Bluetooth-Geräten und-Diensten zu vereinfachen, ordnet Windows das Bluetooth Service Discovery-Protokoll (SDP) den Windows Sockets-Namespace Schnittstellen zu.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, Tasks, ermitteln von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2020
ms.locfileid: "106339049"
---
# <a name="discovering-bluetooth-devices-and-services"></a><span data-ttu-id="fe677-104">Ermitteln von Bluetooth-Geräten und -Diensten</span><span class="sxs-lookup"><span data-stu-id="fe677-104">Discovering Bluetooth Devices and Services</span></span>

<span data-ttu-id="fe677-105">Um die Ermittlung von Bluetooth-Geräten und-Diensten zu vereinfachen, ordnet Windows das Bluetooth Service Discovery-Protokoll (SDP) den Windows Sockets-Namespace Schnittstellen zu.</span><span class="sxs-lookup"><span data-stu-id="fe677-105">To facilitate the discovery of Bluetooth devices and services, Windows maps the Bluetooth Service Discovery Protocol (SDP) onto the Windows Sockets namespace interfaces.</span></span> <span data-ttu-id="fe677-106">Die primären Funktionen, die für diese Zuordnung verwendet werden, sind die Funktionen [**wsasetservice**](bluetooth-and-wsasetservice.md), [**wsalookupservicebegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)und [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) .</span><span class="sxs-lookup"><span data-stu-id="fe677-106">The primary functions used for this mapping are the [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) functions.</span></span> <span data-ttu-id="fe677-107">Die [**wsaqueryset**](bluetooth-and-wsaqueryset-for-set-service.md) -Struktur wird auch in Verbindung mit diesen Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe677-107">The [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure is also used in conjunction with these functions.</span></span>

<span data-ttu-id="fe677-108">Da bestimmte Konzepte und Parameter aus dem Bluetooth-SDP nicht notwendigerweise direkt in der [**wsaqueryset**](bluetooth-and-wsaqueryset-for-set-service.md) -Struktur zugeordnet werden, muss die Aufmerksamkeit für die Erstellung und Verwendung ihrer Mitglieder bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="fe677-108">Because certain concepts and parameters from the Bluetooth SDP do not necessarily map directly into the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure, attention must be paid to how its members are created and used.</span></span> <span data-ttu-id="fe677-109">Für viele komplexe Bluetooth-Vorgänge, wie z. b. die Erstellung von SDP-Datensätzen, wird das **lpblob** -Element von **wsaqueryset** verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe677-109">For many complex Bluetooth operations, such as the creation of SDP records, the **lpBlob** member of the **WSAQUERYSET** is used.</span></span> <span data-ttu-id="fe677-110">Wenn eine solche besondere Überlegung erforderlich ist, wird Sie speziell beschrieben, wie z. b. auf Verweis Seiten wie [**Bluetooth und WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), und anderen.</span><span class="sxs-lookup"><span data-stu-id="fe677-110">When such special consideration is necessary, it is specifically described, such as in reference pages like [**Bluetooth and WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and others.</span></span>

<span data-ttu-id="fe677-111">Es ist wichtig zu verstehen, dass die SDP-Registrierung vom socketsteuerelement getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="fe677-111">It is important to understand that SDP registration is separate from socket control.</span></span> <span data-ttu-id="fe677-112">Wenn eine Serveranwendung für die Annahme der Client Verbindung vorbereitet ist, sollte Sie die [**wsasetservice**](bluetooth-and-wsasetservice.md) -Funktion zum Registrieren eines Bluetooth-SDP-Datensatzes, der diesem Dienst entspricht, registrieren.</span><span class="sxs-lookup"><span data-stu-id="fe677-112">When a server application is prepared to accept client connection, it should call the [**WSASetService**](bluetooth-and-wsasetservice.md) function to register a Bluetooth SDP record that corresponds to that service.</span></span> <span data-ttu-id="fe677-113">Diese Bluetooth-Anwendung muss die **wsasetservice** -Funktion vor dem Schließen erneut abrufen, um die Registrierung des Bluetooth-SDP-Datensatzes aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="fe677-113">That Bluetooth application must call the **WSASetService** function again before closing, to deregister the Bluetooth SDP record.</span></span>

<span data-ttu-id="fe677-114">Wenn die auf dieser Seite beschriebenen Zuweisungs Funktionen verwendet werden, wird der NS- \_ BTH-Namespace zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fe677-114">When using the mapping functions described on this page, the NS\_BTH namespace is assigned.</span></span>

<span data-ttu-id="fe677-115">Weitere Informationen zum Ermitteln von Geräten und Diensten finden Sie auf den folgenden Referenzseiten:</span><span class="sxs-lookup"><span data-stu-id="fe677-115">For further information about discovering devices and services, consult the following reference pages:</span></span>

-   [<span data-ttu-id="fe677-116">**Bluetooth und wsasetservice**</span><span class="sxs-lookup"><span data-stu-id="fe677-116">**Bluetooth and WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
-   [<span data-ttu-id="fe677-117">**Bluetooth und wsalookupservicebegin für Geräte Anfrage**</span><span class="sxs-lookup"><span data-stu-id="fe677-117">**Bluetooth and WSALookupServiceBegin for Device Inquiry**</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [<span data-ttu-id="fe677-118">**Bluetooth und wsalookupservicebegin für die Dienst Ermittlung**</span><span class="sxs-lookup"><span data-stu-id="fe677-118">**Bluetooth and WSALookupServiceBegin for Service Discovery**</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [<span data-ttu-id="fe677-119">**Bluetooth und WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="fe677-119">**Bluetooth and WSALookupServiceNext**</span></span>](bluetooth-and-wsalookupservicenext.md)
-   [<span data-ttu-id="fe677-120">**Bluetooth und WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="fe677-120">**Bluetooth and WSALookupServiceEnd**</span></span>](bluetooth-and-wsalookupserviceend.md)
-   [<span data-ttu-id="fe677-121">**Bluetooth und BLOB**</span><span class="sxs-lookup"><span data-stu-id="fe677-121">**Bluetooth and BLOB**</span></span>](bluetooth-and-blob.md)
-   [<span data-ttu-id="fe677-122">**Bluetooth und wsaqueryset**</span><span class="sxs-lookup"><span data-stu-id="fe677-122">**Bluetooth and WSAQUERYSET**</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)

<span data-ttu-id="fe677-123">Sie können auch das [Bluetooth-Verbindungs](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) Beispiel herunterladen, um ein umfassendes Beispiel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fe677-123">You can also download the [Bluetooth connection sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) for a complete example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe677-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe677-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe677-125">Bluetooth-Programmierung mit Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="fe677-125">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[<span data-ttu-id="fe677-126">Beispiel für Bluetooth-Verbindung</span><span class="sxs-lookup"><span data-stu-id="fe677-126">Bluetooth connection sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




