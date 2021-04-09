---
description: Bei der Weiterleitung wird eine eingehende Sitzung an eine andere Zieladresse umgeleitet.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Weiter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862619"
---
# <a name="forward"></a><span data-ttu-id="bdbff-103">Weiter</span><span class="sxs-lookup"><span data-stu-id="bdbff-103">Forward</span></span>

<span data-ttu-id="bdbff-104">Bei der Weiterleitung wird eine eingehende Sitzung an eine andere Zieladresse umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bdbff-104">Forwarding is the deflection of an incoming session to a different destination address.</span></span> <span data-ttu-id="bdbff-105">TAPI ermöglicht es einer Anwendung, eine Liste von Weiterleitungs Bedingungen für eine Adresse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bdbff-105">TAPI allows an application to specify a list of forwarding conditions for an address.</span></span> <span data-ttu-id="bdbff-106">Weiterleitungs Bedingungen können für jede aufrufende Adresse so fein wie ein anderes Ziel und [**Weiterleitungs Modus**](./lineforwardmode--constants.md) sein.</span><span class="sxs-lookup"><span data-stu-id="bdbff-106">Forwarding conditions can be as finely grained as a different destination and [**forwarding mode**](./lineforwardmode--constants.md) for each caller address.</span></span>

<span data-ttu-id="bdbff-107">Der Weiterleitungs Vorgang kann auch verwendet werden, um eine selektive Funktion zum stören von Funktionen zu implementieren, indem einige Aufrufer an Voicemail weitergeleitet werden und anderen Benutzer den abschlussversuch gestatten.</span><span class="sxs-lookup"><span data-stu-id="bdbff-107">The forwarding operation can also be used to implement a selective do-not-disturb feature, by forwarding some callers to voice mail and allowing others to attempt completion.</span></span>

<span data-ttu-id="bdbff-108">Der Weiterleitungs Vorgang kann auch alle derzeit gültigen Weiterleitungen abbrechen.</span><span class="sxs-lookup"><span data-stu-id="bdbff-108">The forwarding operation can also cancel any forwarding currently in effect.</span></span>

<span data-ttu-id="bdbff-109">Einige Dienstanbieter erfordern, dass eine Anwendung vor einem Weiterleitungs Vorgang einen Beratungs Rückruf erstellt.</span><span class="sxs-lookup"><span data-stu-id="bdbff-109">Some service providers require that an application create a consultation call prior to a forwarding operation.</span></span> <span data-ttu-id="bdbff-110">Der Weiterleitungs Vorgang wird dann als Zeiger auf den-Rückruf übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bdbff-110">The forwarding operation is then passed a pointer to the consultation call.</span></span>

<span data-ttu-id="bdbff-111">Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bdbff-111">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="bdbff-112">**TAPI 2. x:** Wenn Sie [**lineforward**](/windows/win32/api/tapi/nf-tapi-lineforward) festlegen möchten, um [**linegetaddressstatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)zu erhalten, ändern Sie die [**Zeile \_ addressstate**](./line-addressstate.md) -Benachrichtigungs Meldung mit lineaddressstate \_ Forward.</span><span class="sxs-lookup"><span data-stu-id="bdbff-112">**TAPI 2.x:** To set [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) to get [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), change the [**LINE\_ADDRESSSTATE**](./line-addressstate.md) notification message with LINEADDRESSSTATE\_FORWARD.</span></span>

<span data-ttu-id="bdbff-113">**TAPI 3. x:** Weitere Informationen finden Sie unter [**itaddress:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**itaddress:: get \_ currentforwardinfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), Change Notification: [**itadressssevent:: get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ Forward.</span><span class="sxs-lookup"><span data-stu-id="bdbff-113">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get\_CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification: [**ITAddressEvent::get\_Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE\_FORWARD.</span></span>

> [!Note]  
> <span data-ttu-id="bdbff-114">Es ist möglicherweise nicht möglich, dass ein Dienstanbieter immer weiß, welche Weiterleitung für eine Adresse wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="bdbff-114">It may be impossible for a service provider to know at all times what forwarding is in effect for an address.</span></span> <span data-ttu-id="bdbff-115">Die Weiterleitung kann auf eine Weise abgebrochen oder geändert werden, die nicht zur Benachrichtigung an den Dienstanbieter führt.</span><span class="sxs-lookup"><span data-stu-id="bdbff-115">Forwarding can be canceled or changed in ways that do not result in notification to the service provider.</span></span>

 

 

 
