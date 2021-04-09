---
description: Der Netzwerk Lademodus (Asynchronous Transfer Mode, ATM) basiert auf dem Rechenzentrum, und die Unterstützung für ATM wurde vielen Teilen des Betriebssystems hinzugefügt.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Quality of Service (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867368"
---
# <a name="quality-of-service-telephony-api"></a><span data-ttu-id="bf735-103">Quality of Service (telefonieapi)</span><span class="sxs-lookup"><span data-stu-id="bf735-103">Quality of Service (Telephony API)</span></span>

<span data-ttu-id="bf735-104">Der Netzwerk Lademodus (Asynchronous Transfer Mode, ATM) basiert auf dem Rechenzentrum, und die Unterstützung für ATM wurde vielen Teilen des Betriebssystems hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf735-104">Asynchronous Transfer Mode (ATM) networking is emerging into the mainstream of computing, and support for ATM has been added to many parts of the operating system.</span></span> <span data-ttu-id="bf735-105">TAPI unterstützt auch Schlüssel Attribute der Einrichtung von Anrufen in ATM-Einrichtungen.</span><span class="sxs-lookup"><span data-stu-id="bf735-105">TAPI also supports key attributes of establishing calls on ATM facilities.</span></span> <span data-ttu-id="bf735-106">Die wichtigste davon aus der Anwendungsperspektive ist die Möglichkeit, Quality of Service (QoS)-Parameter für eingehende und ausgehende Aufrufe anzufordern, zu aushandeln, zu aushandeln und Anzeichen dafür zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bf735-106">The most important of these from an application perspective is the ability to request, negotiate, renegotiate, and receive indications of Quality of Service (QOS) parameters on incoming and outgoing calls.</span></span>

<span data-ttu-id="bf735-107">QoS-Informationen in TAPI werden zwischen Anwendungen und Dienstanbietern in [**Flowspec**](/windows/desktop/api/qos/ns-qos-flowspec) -Strukturen ausgetauscht, die in Windows Sockets 2,0 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bf735-107">QOS information in TAPI is exchanged between applications and service providers in [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) structures that are defined in Windows Sockets 2.0.</span></span>

<span data-ttu-id="bf735-108">Anwendungen fordern QoS für ausgehende Aufrufe an, indem Sie die Sitzungs Informationswerte festlegen, bevor Sie eine Kommunikationssitzung starten.</span><span class="sxs-lookup"><span data-stu-id="bf735-108">Applications request QOS on outgoing calls by setting session information values prior to starting a communications session.</span></span> <span data-ttu-id="bf735-109">Der Dienstanbieter versucht, die angegebene QoS anzugeben, und schlägt fehl, wenn dies nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="bf735-109">The service provider will try to provide the specified QOS, and fail the call if it cannot.</span></span> <span data-ttu-id="bf735-110">Die Anwendung kann dann Ihre Parameter anpassen und den Rückruf erneut versuchen.</span><span class="sxs-lookup"><span data-stu-id="bf735-110">The application can then adjust its parameters and try the call again.</span></span> <span data-ttu-id="bf735-111">Nachdem ein-Rückruf erstellt wurde, kann eine Anwendung eine Änderung im QoS anfordern.</span><span class="sxs-lookup"><span data-stu-id="bf735-111">After a call is established, an application can request a change in the QOS.</span></span>

<span data-ttu-id="bf735-112">TAPI stellt Ereignis Benachrichtigungen für den Besitzer oder die Überwachung von Anwendungen bereit, wenn eine Änderung der QoS-Ebenen vorliegt.</span><span class="sxs-lookup"><span data-stu-id="bf735-112">TAPI provides event notifications to owner or monitor applications if there is any change in QOS levels.</span></span>

<span data-ttu-id="bf735-113">Die Unterstützung für QoS ist nicht auf ATM-Transporte beschränkt. Jeder Dienstanbieter kann QoS-Funktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="bf735-113">Support for QOS is not restricted to ATM transports; any service provider can implement QOS features.</span></span>

<span data-ttu-id="bf735-114">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="bf735-114">Not all service providers support use of this information.</span></span>

<span data-ttu-id="bf735-115">\* \* TAPI 2. x: \* \*[**linesetcallqualityofservice**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwsendingflowspecsize**, **dwsendingflowspecoffset**, **dwreceivingflowspecsize** und **dwreceivingflowspecoffset** Member von [**linecallpara**](/windows/win32/api/tapi/ns-tapi-linecallparams) Metern</span><span class="sxs-lookup"><span data-stu-id="bf735-115">\*\*TAPI 2.x:  \*\*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize**, and **dwReceivingFlowspecOffset** members of [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span></span>

<span data-ttu-id="bf735-116">\* \* TAPI 3. x: \* \*[**itbasiccallcontrol:: setqos**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**itqosevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span><span class="sxs-lookup"><span data-stu-id="bf735-116">\*\*TAPI 3.x:  \*\*[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span></span>

 

 
