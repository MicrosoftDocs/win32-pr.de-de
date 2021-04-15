---
title: Gerätefehler Codes
description: Die InvokeAction-und QueryStatus-ariable-Methoden geben HRESULT-Werte zurück, die möglicherweise auf einen Gerätefehler hinweisen (d. h. einen Fehler, der von einem UPnP-zertifizierten Gerät empfangen wird).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474541"
---
# <a name="device-error-codes"></a><span data-ttu-id="2d51b-103">Gerätefehler Codes</span><span class="sxs-lookup"><span data-stu-id="2d51b-103">Device Error Codes</span></span>

<span data-ttu-id="2d51b-104">Die [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) -und [**QueryStatus-ariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) -Methoden geben **HRESULT** -Werte zurück, die möglicherweise auf einen Gerätefehler hinweisen (d. h. einen Fehler, der von einem UPnP-zertifizierten Gerät empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="2d51b-104">The [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods return **HRESULT** values that might indicate a device error (that is, an error that is received from a UPnP-certified device).</span></span> <span data-ttu-id="2d51b-105">Wenn ein Fehler von einem Gerät empfangen wird, gibt die Methode ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) oder [**QueryStatus**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) einen **HRESULT** -Wert zurück, der auf dem Gerätefehler Code basiert, wie in diesem Thema erläutert.</span><span class="sxs-lookup"><span data-stu-id="2d51b-105">If an error is received from a device, the method ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) or [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) returns an **HRESULT** value that is based on the device error code, as explained in this topic.</span></span> <span data-ttu-id="2d51b-106">Da eine Konvertierung auf den Gerätefehler Code angewendet wird, um einen **HRESULT** -Wert zu erhalten, können Sie den Fehlercode des Geräts nicht direkt aus dem **HRESULT** -Wert lesen.</span><span class="sxs-lookup"><span data-stu-id="2d51b-106">Because a conversion is applied to the device error code to produce an **HRESULT** value, you cannot read the device error code directly from the **HRESULT** value.</span></span>

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a><span data-ttu-id="2d51b-107">Konvertierung eines Gerätefehler Codes in ein HRESULT</span><span class="sxs-lookup"><span data-stu-id="2d51b-107">Conversion of a Device Error Code to an HRESULT</span></span>

<span data-ttu-id="2d51b-108">Es gibt sowohl standardmäßige als auch nicht standardmäßige Gerätefehler Codes.</span><span class="sxs-lookup"><span data-stu-id="2d51b-108">There are both standard and non-standard device error codes.</span></span> <span data-ttu-id="2d51b-109">Die Standard Codes haben in allen UPnP-zertifizierten Geräten dieselbe Bedeutung und verfügen über Werte, die kleiner als 600 sind.</span><span class="sxs-lookup"><span data-stu-id="2d51b-109">The standard codes have the same meaning across all UPnP-certified devices and have values that are less than 600.</span></span> <span data-ttu-id="2d51b-110">Die nicht standardmäßigen Codes sind Hersteller spezifisch und weisen Werte zwischen 600 und 899 auf.</span><span class="sxs-lookup"><span data-stu-id="2d51b-110">The non-standard codes are vendor-specific and have values ranging from 600 through 899.</span></span>

<span data-ttu-id="2d51b-111">Unabhängig davon, ob der Gerätefehler Code "Standard" ist, bestimmt, wie der **HRESULT** -Wert generiert wird:</span><span class="sxs-lookup"><span data-stu-id="2d51b-111">Whether or not the device error code is standard determines how the **HRESULT** value is generated:</span></span>

-   <span data-ttu-id="2d51b-112">Ein standardmäßiger Gerätefehler Code ist einem **HRESULT** -Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2d51b-112">A standard device error code is mapped to an **HRESULT** value.</span></span>

<!-- -->

-   <span data-ttu-id="2d51b-113">Ein nicht standardmäßiger Gerätefehler Code wird durch Anwenden einer Formel in den **HRESULT** -Wert eingebettet.</span><span class="sxs-lookup"><span data-stu-id="2d51b-113">A non-standard device error code is embedded in the **HRESULT** value by applying a formula.</span></span>

<span data-ttu-id="2d51b-114">Beide Verfahren können umgekehrt werden, um den Gerätefehler Code aus einem bestimmten **HRESULT** -Wert zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2d51b-114">Both of these procedures can be reversed to determine the device error code from a particular **HRESULT** value.</span></span>

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a><span data-ttu-id="2d51b-115">Ableiten eines Gerätefehler Codes von einem HRESULT-Wert</span><span class="sxs-lookup"><span data-stu-id="2d51b-115">Deriving a Device Error Code from an HRESULT Value</span></span>

<span data-ttu-id="2d51b-116">Wenn der **HRESULT** -Wert größer als oder gleich **UPnP \_ e \_ Action \_ Specific \_ Base** (0x80040300) und kleiner als oder gleich **UPnP \_ e \_ Action \_ Specific \_ Max** (0x8004042b) ist, ist der Fehlercode des Geräts nicht dem Standard – verwenden Sie die Formel im folgenden Abschnitt, um den Fehlercode zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2d51b-116">If the **HRESULT** value is greater than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_BASE** (0x80040300) and less than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_MAX** (0x8004042B), the device error code is nonstandard — use the formula in the following section to determine the error code.</span></span> <span data-ttu-id="2d51b-117">Andernfalls ist der Gerätefehler Code Standard – verwenden Sie die Tabelle im Abschnitt Mapping for Standard Device Error Codes, die die Zuordnung vom **HRESULT** -Wert zum Gerätefehler Code bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2d51b-117">Otherwise, the device error code is standard — use the table in the Mapping for Standard Device Error Codes section, which provides the mapping from the **HRESULT** value to the device error code.</span></span>

<span data-ttu-id="2d51b-118">Legen Sie für eine Textbeschreibung des Fehlers nach einem Aufruf von [**iupnpservice:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction)den *pvarretval* -Parameter auf ein leeres Array fest.</span><span class="sxs-lookup"><span data-stu-id="2d51b-118">For a text description of the error after a call to [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), set the *pvarRetVal* parameter to an empty array.</span></span> <span data-ttu-id="2d51b-119">Bei der Rückgabe enthält dieser Parameter eine Textbeschreibung des Fehlers, sofern aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2d51b-119">Upon return, this parameter will contain a text description of the error, if any occurred.</span></span>

### <a name="formula-for-nonstandard-device-error-codes"></a><span data-ttu-id="2d51b-120">Formel für nicht dem Standard entsprechende Gerätefehler Codes</span><span class="sxs-lookup"><span data-stu-id="2d51b-120">Formula for Nonstandard Device Error Codes</span></span>

<span data-ttu-id="2d51b-121">Verwenden Sie die folgende Formel, wenn **UPnP \_ e \_ Action Specific \_ \_ Base** für **HRESULT** -**UPnP \_ e \_ Action \_ Specific \_ Max**.</span><span class="sxs-lookup"><span data-stu-id="2d51b-121">Use the following formula if **UPNP\_E\_ACTION\_SPECIFIC\_BASE** ≤ **HRESULT** ≤**UPNP\_E\_ACTION\_SPECIFIC\_MAX**.</span></span>

<span data-ttu-id="2d51b-122">Gerätefehler Code = (**HRESULT**  -  **UPnP \_ E \_ Action \_ Specific \_ Base**) + **Fehler \_ Aktions \_ spezifische \_ Basis**</span><span class="sxs-lookup"><span data-stu-id="2d51b-122">Device Error Code = (**HRESULT** - **UPNP\_E\_ACTION\_SPECIFIC\_BASE**) + **FAULT\_ACTION\_SPECIFIC\_BASE**</span></span>

<span data-ttu-id="2d51b-123">Durch Ersetzen der tatsächlichen numerischen Werte ist die Gleichung: Gerätefehler Code = (**HRESULT** -0x80040300) + 0x0258</span><span class="sxs-lookup"><span data-stu-id="2d51b-123">Substituting the actual numeric values, the equation is: Device Error Code = (**HRESULT** - 0x80040300) + 0x0258</span></span>

### <a name="mapping-for-standard-device-error-codes"></a><span data-ttu-id="2d51b-124">Zuordnung für Standard Geräte-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="2d51b-124">Mapping for Standard Device Error Codes</span></span>

<span data-ttu-id="2d51b-125">Verwenden Sie die folgende Zuordnung, wenn **HRESULT**  <  **UPnP \_ E \_ Action \_ Specific \_ Base** ist.</span><span class="sxs-lookup"><span data-stu-id="2d51b-125">Use the following mapping if **HRESULT** < **UPNP\_E\_ACTION\_SPECIFIC\_BASE**.</span></span>



| <span data-ttu-id="2d51b-126">HRESULT-Wert</span><span class="sxs-lookup"><span data-stu-id="2d51b-126">HRESULT value</span></span>                    | <span data-ttu-id="2d51b-127">Gerätefehler Code</span><span class="sxs-lookup"><span data-stu-id="2d51b-127">Device Error Code</span></span>                | <span data-ttu-id="2d51b-128">Tatsächlicher Wert</span><span class="sxs-lookup"><span data-stu-id="2d51b-128">Actual value</span></span> |
|----------------------------------|----------------------------------|--------------|
| <span data-ttu-id="2d51b-129">UPnP \_ E \_ ungültige \_ Aktion.</span><span class="sxs-lookup"><span data-stu-id="2d51b-129">UPNP\_E\_INVALID\_ACTION</span></span>         | <span data-ttu-id="2d51b-130">\_ungültige \_ Aktion</span><span class="sxs-lookup"><span data-stu-id="2d51b-130">FAULT\_INVALID\_ACTION</span></span>           | <span data-ttu-id="2d51b-131">401</span><span class="sxs-lookup"><span data-stu-id="2d51b-131">401</span></span>          |
| <span data-ttu-id="2d51b-132">UPnP \_ E \_ ungültige \_ Argumente.</span><span class="sxs-lookup"><span data-stu-id="2d51b-132">UPNP\_E\_INVALID\_ARGUMENTS</span></span>      | <span data-ttu-id="2d51b-133">Fehler \_ ungültiges \_ arg</span><span class="sxs-lookup"><span data-stu-id="2d51b-133">FAULT\_INVALID\_ARG</span></span>              | <span data-ttu-id="2d51b-134">402</span><span class="sxs-lookup"><span data-stu-id="2d51b-134">402</span></span>          |
| <span data-ttu-id="2d51b-135">UPnP \_ E \_ nicht \_ \_ synchron</span><span class="sxs-lookup"><span data-stu-id="2d51b-135">UPNP\_E\_OUT\_OF\_SYNC</span></span>           | <span data-ttu-id="2d51b-136">\_ungültige \_ Sequenz \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="2d51b-136">FAULT\_INVALID\_SEQUENCE\_NUMBER</span></span> | <span data-ttu-id="2d51b-137">403</span><span class="sxs-lookup"><span data-stu-id="2d51b-137">403</span></span>          |
| <span data-ttu-id="2d51b-138">UPnP \_ E \_ ungültige \_ Variable.</span><span class="sxs-lookup"><span data-stu-id="2d51b-138">UPNP\_E\_INVALID\_VARIABLE</span></span>       | <span data-ttu-id="2d51b-139">\_ungültige \_ Variable.</span><span class="sxs-lookup"><span data-stu-id="2d51b-139">FAULT\_INVALID\_VARIABLE</span></span>         | <span data-ttu-id="2d51b-140">404</span><span class="sxs-lookup"><span data-stu-id="2d51b-140">404</span></span>          |
| <span data-ttu-id="2d51b-141">UPnP \_ E- \_ Aktions \_ Anforderung \_ fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="2d51b-141">UPNP\_E\_ACTION\_REQUEST\_FAILED</span></span> | <span data-ttu-id="2d51b-142">\_ \_ interner \_ Fehler des Fehler Geräts</span><span class="sxs-lookup"><span data-stu-id="2d51b-142">FAULT\_DEVICE\_INTERNAL\_ERROR</span></span>   | <span data-ttu-id="2d51b-143">501</span><span class="sxs-lookup"><span data-stu-id="2d51b-143">501</span></span>          |



 

## <a name="more-information"></a><span data-ttu-id="2d51b-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2d51b-144">More Information</span></span>

<span data-ttu-id="2d51b-145">Gerätefehler Codes werden in der [UPnP-Geräte Architektur Version 1,0](https://openconnectivity.org/resources/documents.asp)angegeben.</span><span class="sxs-lookup"><span data-stu-id="2d51b-145">Device error codes are specified in [UPnP Device Architecture version 1.0](https://openconnectivity.org/resources/documents.asp).</span></span> <span data-ttu-id="2d51b-146">Die in diesem Thema erwähnten Konstanten sind in den Dateien "UPnP. h" und "UPnP. idl" definiert.</span><span class="sxs-lookup"><span data-stu-id="2d51b-146">The constants mentioned in this topic are defined in the files Upnp.h and Upnp.idl.</span></span>

 

 




