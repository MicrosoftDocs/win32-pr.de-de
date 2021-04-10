---
description: In diesem Abschnitt wird die Protokoll spezifische Quality of Service Struktur (QoS) für ATM beschrieben, die im Feld ProviderSpecific der QoS-Struktur enthalten ist.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Winsock ATM-QoS-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129105"
---
# <a name="winsock-atm-qos-extension"></a><span data-ttu-id="defad-103">Winsock ATM-QoS-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="defad-103">Winsock ATM QoS Extension</span></span>

<span data-ttu-id="defad-104">In diesem Abschnitt wird die Protokoll spezifische Quality of Service Struktur ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) für ATM beschrieben, die im Feld [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) der **QoS** -Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="defad-104">This section describes the protocol-specific Quality of Service ([**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)) structure for ATM, which is contained in the [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) field of the **QOS** structure.</span></span> <span data-ttu-id="defad-105">Beachten Sie, dass die Verwendung dieser ATM-spezifischen **QoS** -Struktur von Windows Sockets 2-Clients optional ist, und der ATM-Dienstanbieter ist erforderlich, um die generische [**Flowspec**](/windows/win32/api/qos/ns-qos-flowspec) -Struktur den entsprechenden Q. 2931-Informations Elementen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="defad-105">Note that the use of this ATM-specific **QOS** structure is optional by Windows Sockets 2 clients, and the ATM service provider is required to map the generic [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure to appropriate Q.2931 information elements.</span></span> <span data-ttu-id="defad-106">Wenn jedoch sowohl die generische **Flowspec** -Struktur als auch die ATM-spezifische **QoS** -Struktur angegeben werden, sollte der in der ATM-spezifischen **QoS** -Struktur angegebene Wert Vorrang haben, wenn Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="defad-106">However, if both the generic **FLOWSPEC** structure and ATM-specific **QOS** structure are specified, the value specified in the ATM-specific **QOS** structure should take precedence should there be any conflicts.</span></span> <span data-ttu-id="defad-107">Weitere Informationen zu QoS-und **Flowspec** -Strukturen finden Sie im Abschnitt 2,7 der Windows Sockets 2-API-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="defad-107">See Windows Sockets 2 API Specification Section 2.7 for more information about QoS provisions and **FLOWSPEC** structure.</span></span>

<span data-ttu-id="defad-108">Die Protokoll spezifische [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) -Struktur für ATM ist eine Verkettung von Q. 2931 Information Element-Strukturen (IE), die im folgenden Text definiert werden.</span><span class="sxs-lookup"><span data-stu-id="defad-108">The protocol-specific [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) structure for ATM is a concatenation of Q.2931 information element (IE) structures, which are defined in the following text.</span></span> <span data-ttu-id="defad-109">Wenn eine Anwendung einen Internetinformationsdienst (IE) auslässt, den die Uni 3. x nicht benötigt, sollte der Dienstanbieter einen angemessenen Standardwert einfügen, wobei die Informationen in der [**Flowspec**](/windows/win32/api/qos/ns-qos-flowspec) -Struktur ggf. berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="defad-109">If an application omits an IE that UNI 3.x mandates, the service provider should insert a reasonable default value, taking the information in the [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure into account if applicable.</span></span>

<span data-ttu-id="defad-110">Die Behandlung von wiederholten Wiederholungen hängt von der IE selbst ab.</span><span class="sxs-lookup"><span data-stu-id="defad-110">The handling of repeated IEs is dependent on the IE itself.</span></span> <span data-ttu-id="defad-111">Wenn ein Internet Explorer wiederholt wird und es sich um einen Wert handelt, der gemäß der Uni-Spezifikation des ATM-Forums wiederholt werden darf, muss der Anbieter ihn ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="defad-111">If an IE is repeated and it is one that is allowed to be repeated per the ATM Forum UNI specification then the provider must handle it properly.</span></span> <span data-ttu-id="defad-112">In diesem Fall bestimmt Order in der Liste die bevorzugte Reihenfolge, wobei Elemente, die an früherer Stelle in der Liste angezeigt werden, besser bevorzugt werden.</span><span class="sxs-lookup"><span data-stu-id="defad-112">In this case, order in the list determines preference order, with elements appearing earlier in the list being more preferred.</span></span> <span data-ttu-id="defad-113">Wenn ein Internet Explorer wiederholt wird und dies nicht pro ATM-Forums-UNI-Spezifikation zulässig ist, kann der Anbieter entweder die Anforderung vom Client (die bevorzugte Option) nicht ausführen oder den letzten IE dieses Typs verwenden.</span><span class="sxs-lookup"><span data-stu-id="defad-113">If an IE is repeated and this is not allowed per ATM Forum UNI specification, the provider may either fail the request from the client (the preferred option) or use the last IE of that type found.</span></span>

<span data-ttu-id="defad-114">Jede einzelne IE-Struktur wird wie folgt formatiert und durch das **ietype** -Feld identifiziert:</span><span class="sxs-lookup"><span data-stu-id="defad-114">Each individual IE structure is formatted in the following manner and identified by the **IEType** field:</span></span>

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

<span data-ttu-id="defad-115">Zulässige Werte für das **ietype** -Feld werden wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="defad-115">Legal values for the **IEType** field are defined as:</span></span>

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

<span data-ttu-id="defad-116">Das Feld " **IE** " wird durch eine bestimmte IE-Struktur überlagert, und das Feld " **ielength** " ist die Gesamtlänge in Byte der IE-Struktur, einschließlich der **ietype** -und **ielength** -Felder.</span><span class="sxs-lookup"><span data-stu-id="defad-116">The **IE** field is overlaid by a specific IE structure and the **IELength** field is the total length in bytes of the IE structure including the **IEType** and **IELength** fields.</span></span> <span data-ttu-id="defad-117">Die Semantik und die gültigen Werte für jedes Element dieser IE-Strukturen sind gemäß der ATM-Uni 3. x-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="defad-117">The semantics and legal values for each element of these IE structures are per ATM UNI 3.x specification.</span></span> <span data-ttu-id="defad-118">Ein nicht vorhandenes SAP- \_ Feld \_ kann für die Elemente verwendet werden, die für eine bestimmte IE-Struktur optional sind, und zwar gemäß der Angabe von ATM Uni 3. x</span><span class="sxs-lookup"><span data-stu-id="defad-118">SAP\_FIELD\_ABSENT can be used for those elements that are optional for a given IE structure, per ATM UNI 3.x specification.</span></span>

 

 
