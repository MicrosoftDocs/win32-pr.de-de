---
title: Implementieren von Geräteverhalten
description: Das Verhalten eines Geräts wird durch die Dienste definiert, die es verfügbar macht.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb702adf3ccb0f21bc71f08e98427cca15495f3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363904"
---
# <a name="implementing-device-behavior"></a><span data-ttu-id="a7300-103">Implementieren von Geräteverhalten</span><span class="sxs-lookup"><span data-stu-id="a7300-103">Implementing Device Behavior</span></span>

<span data-ttu-id="a7300-104">Das Verhalten eines Geräts wird durch die Dienste definiert, die es verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="a7300-104">The behavior of a device is defined by the services it exposes.</span></span> <span data-ttu-id="a7300-105">Jeder Dienst verfügt über eine Dienst Beschreibung, die seine Aktionen und Zustandsvariablen auflistet.</span><span class="sxs-lookup"><span data-stu-id="a7300-105">Each service has a service description that lists its actions and state variables.</span></span> <span data-ttu-id="a7300-106">Zusammen bilden diese Dienst Beschreibungen die Dienst Schnittstelle, die definiert, wie ein Steuerungspunkt mit einem Dienst interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="a7300-106">Taken together, these service descriptions make up the service interface, which defines the way in which a control point can interact with a service.</span></span> <span data-ttu-id="a7300-107">Jeder Dienst muss mindestens eine Aktion haben.</span><span class="sxs-lookup"><span data-stu-id="a7300-107">Each service must have at least one action.</span></span>

<span data-ttu-id="a7300-108">Um einen Dienst zu implementieren, muss ein gehostetes Gerät ein Component Object Model (com)-Objekt bereitstellen, das die-Schnittstelle für den Dienst verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="a7300-108">To implement a service, a hosted device must provide a Component Object Model (COM) object that exposes the interface for the service.</span></span> <span data-ttu-id="a7300-109">In der Dienst Beschreibung werden die Dienst Schnittstellen in der UPnP-Vorlagen Sprache (UTL) angegeben. Allerdings werden COM-Objekt Schnittstellen in der Regel in IDL (Interface Definition Language) angegeben.</span><span class="sxs-lookup"><span data-stu-id="a7300-109">In the service description, the service interfaces are specified in UPnP Template Language (UTL); however, COM object interfaces typically are specified in Interface Definition Language (IDL).</span></span> <span data-ttu-id="a7300-110">Sie können auch die COM-Schnittstelle in einer Typbibliothek oder Header Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="a7300-110">You can also specify the COM interface in a type library or header file.</span></span> <span data-ttu-id="a7300-111">Das Platform Software Development Kit (SDK) umfasst das Tool Utl2idl, das eine Dienst Beschreibung in UTL in eine COM-Schnittstelle in IDL übersetzt.</span><span class="sxs-lookup"><span data-stu-id="a7300-111">The Platform Software Development Kit (SDK) includes the Utl2idl tool, which translates a service description in UTL to a COM interface in IDL.</span></span>

<span data-ttu-id="a7300-112">In den folgenden Beispielen wird dieser Konvertierungsprozess veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a7300-112">The following samples illustrate this conversion process.</span></span> <span data-ttu-id="a7300-113">Die Dienst Beschreibung wird vom Geräte Entwickler bereitgestellt und in UTL geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7300-113">The service description is provided by the device developer and is written in UTL.</span></span>

``` syntax
<?xml version="1.0" ?> 
  <scpd xmlns="urn:schemas-upnp-org:service-1-0">

    <specVersion>
      <major>1</major> 
      <minor>0</minor> 
    </specVersion>

    <serviceStateTable>
      <stateVariable>
        <name>Power</name> 
        <dataType>Boolean</dataType> 
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>Level</name> 
        <dataType>i4</dataType> 
        <allowedValueRange>
          <minimum>0</minimum> 
            <maximum>10</maximum> 
            <step>1</step> 
        </allowedValueRange>
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>State</name> 
        <dataType>string</dataType> 
        <allowedValueList>
          <allowedValue>ON</allowedValue> 
          <allowedValue>OFF</allowedValue> 
          <allowedValue>DIMMED</allowedValue> 
        </allowedValueList>
        <defaultValue>OFF</defaultValue> 
      </stateVariable>
    </serviceStateTable>

    <actionList>
      <action>
        <name>PowerOn</name> 
      </action>

      <action>
        <name>PowerOff</name> 
      </action>

      <action>
        <name>SetLevel</name> 
        <argumentList>
          <argument>
            <name>NewLevel</name> 
            <relatedStateVariable>Level</relatedStateVariable> 
            <direction>in</direction> 
          </argument>
          <argument>
            <name>NewState</name> 
            <relatedStateVariable>State</relatedStateVariable> 
            <direction>out</direction> 
          </argument>
        </argumentList>
      </action>

      <action>
        <name>IncreaseLevel</name> 
      </action>

      <action>
        <name>DecreaseLevel</name> 
      </action>
    </actionList>
</scpd>
```

<span data-ttu-id="a7300-114">Der nächste Schritt besteht darin, das Utl2idl-Tool auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a7300-114">The next step is to run the Utl2idl tool.</span></span> <span data-ttu-id="a7300-115">Sie erzeugt die IDL-Datei, die die COM-Schnittstelle enthält.</span><span class="sxs-lookup"><span data-stu-id="a7300-115">It produces the IDL file that contains the COM interface.</span></span> <span data-ttu-id="a7300-116">Weitere Informationen zu IDL-Dateien und zum **Schnittstellen** Schlüsselwort finden Sie unter [Schnittstellen Definitionsdatei (IDL)](/windows/desktop/Midl/interface-definition-idl-file) und [**Schnittstelle**](/windows/desktop/Midl/interface) in der mittleren l-Referenz.</span><span class="sxs-lookup"><span data-stu-id="a7300-116">For more information about IDL files and the **interface** keyword, see [Interface Definition (IDL) File](/windows/desktop/Midl/interface-definition-idl-file) and [**interface**](/windows/desktop/Midl/interface) in the MIDL reference.</span></span>

``` syntax
#include <windows.h>
typedef [v1_enum] enum SCPD_DISPIDS
{
     DISPID_POWER = 1,
     DISPID_LEVEL,
     DISPID_STATE,
     DISPID_POWERON,
     DISPID_POWEROFF,
     DISPID_SETLEVEL,
     DISPID_INCREASELEVEL,
     DISPID_DECREASELEVEL
} SCPD_DISPIDS;

[
     uuid(68369839-960d-4c8c-8d0d-c319c69e73be),
     oleautomation,
     pointer_default(unique)
]
interface IUPnPService_scpd : IUnknown 
{
     [propget, id(DISPID_POWER), helpstring("Property Power")]
     HRESULT Power(
          [out, retval] VARIANT_BOOL *pPower);

     [propget, id(DISPID_LEVEL), helpstring("Property Level")]
     HRESULT Level(
          [out, retval] long *pLevel);

     [propget, id(DISPID_STATE), helpstring("Property State")]
     HRESULT State(
          [out, retval] BSTR *pState);

     [ id(DISPID_POWERON), helpstring("Method PowerOn")]
     HRESULT PowerOn();

     [ id(DISPID_POWEROFF), helpstring("Method PowerOff")]
     HRESULT PowerOff();

     [ id(DISPID_SETLEVEL), helpstring("Method SetLevel")]
     HRESULT SetLevel(
          [in] long NewLevel,
          [in, out] BSTR *pNewState;
                                
     [ id(DISPID_INCREASELEVEL), helpstring("Method IncreaseLevel")]
     HRESULT IncreaseLevel();

     [ id(DISPID_DECREASELEVEL), helpstring("Method DecreaseLevel")]
     HRESULT DecreaseLevel();
};
```

> [!Note]
> <span data-ttu-id="a7300-117">Der Rückgabewert ist der erste \[ out- \] Parameter in der Liste der Argumente in der Dienst Beschreibung. er wird jedoch nach der Übersetzung als letzter Parameter aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7300-117">The return value is the first \[out\] parameter in the list of arguments in the service description; however, it is listed as the last parameter after translation.</span></span>
> 
> <span data-ttu-id="a7300-118">Alle anderen Parameter verbleiben in derselben Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="a7300-118">All other parameters remain in the same order.</span></span>

 

<span data-ttu-id="a7300-119">Um die Funktionalität des Dienstanbieter bereitzustellen, implementieren Sie diese COM-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a7300-119">To provide the functionality of the service, implement this COM interface.</span></span>

## <a name="obtaining-information-about-an-endpoint"></a><span data-ttu-id="a7300-120">Abrufen von Informationen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="a7300-120">Obtaining Information About an Endpoint</span></span>

<span data-ttu-id="a7300-121">Im UPnP-Framework enthalten die Endpunkt Informationen Informationen zu einer Anforderung und ihrer Quelle.</span><span class="sxs-lookup"><span data-stu-id="a7300-121">In the UPnP framework, endpoint information includes information about a request and its source.</span></span> <span data-ttu-id="a7300-122">Ein Gerät kann diese Informationen überprüfen, um eine Entscheidung über die Anforderung zu treffen.</span><span class="sxs-lookup"><span data-stu-id="a7300-122">A device can examine this information in order to make a decision about the request.</span></span>

<span data-ttu-id="a7300-123">Endpunkt Informationen sind optional für den implementierten Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7300-123">Endpoint information is optionally available to the implemented service.</span></span> <span data-ttu-id="a7300-124">Der Geräte Host hat Zugriff auf Endpunkt Informationen. der Geräte Host kommuniziert die Informationen jedoch nicht standardmäßig mit dem implementierten Dienst.</span><span class="sxs-lookup"><span data-stu-id="a7300-124">The device host has access to endpoint information; however, the device host does not communicate the information to the implemented service by default.</span></span> <span data-ttu-id="a7300-125">Sie können den Geräte Host aktivieren, um die Endpunkt Informationen für den implementierten Dienst freizugeben, indem Sie die COM-Schnittstelle in der IDL-Datei (die vom Utl2idl-Tool erstellt wurde) ändern.</span><span class="sxs-lookup"><span data-stu-id="a7300-125">You can enable the device host to share the endpoint information with the implemented service by modifying the COM interface in the IDL file (produced by the Utl2idl tool).</span></span> <span data-ttu-id="a7300-126">Sie können \[ \] jeder Methode, die Endpunkt Informationen erfordert, einen in-Parameter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a7300-126">You can add an \[in\] parameter to each method that requires endpoint information.</span></span> <span data-ttu-id="a7300-127">Der zusätzliche \[ in- \] Parameter muss der erste in der Liste der Argumente, ein Zeiger auf eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle und explizit " **punkremoteendpointinfo**" genannt werden.</span><span class="sxs-lookup"><span data-stu-id="a7300-127">The additional \[in\] parameter must be the first one in the list of arguments, a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, and explicitly named **punkRemoteEndpointInfo**.</span></span> <span data-ttu-id="a7300-128">Änderungen an der Dienst-XML sind nicht erforderlich oder werden empfohlen.</span><span class="sxs-lookup"><span data-stu-id="a7300-128">Modifications to the Service XML are not required, or recommended.</span></span> <span data-ttu-id="a7300-129">Das folgende Beispiel zeigt die neue Definition der **PowerOn** -Methode, wenn Sie so geändert wird, dass Sie Endpunkt Informationen empfängt:</span><span class="sxs-lookup"><span data-stu-id="a7300-129">The following example shows the new definition of the **PowerOn** method when it is amended so that it receives endpoint information:</span></span>

<span data-ttu-id="a7300-130">"HRESULT PowerOn ( \[ in \] IUnknown \* punkremoteendpointinfo);"</span><span class="sxs-lookup"><span data-stu-id="a7300-130">"HRESULT PowerOn(\[in\] IUnknown \*punkRemoteEndpointInfo);"</span></span>

<span data-ttu-id="a7300-131">Ein Zeiger auf ein Endpunkt Informationsobjekt, eine [**iupnpremoteendpointinfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) -Schnittstelle, wird durch den neuen Parameter vom Geräte Host übergeben.</span><span class="sxs-lookup"><span data-stu-id="a7300-131">A pointer to an endpoint information object, an [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface, is passed through this new parameter by the device host.</span></span> <span data-ttu-id="a7300-132">Die **iupnpremoteendpointinfo** -Schnittstelle bietet drei Methoden für den Zugriff auf die Endpunkt Informationen.</span><span class="sxs-lookup"><span data-stu-id="a7300-132">The **IUPnPRemoteEndpointInfo** interface provides three methods for accessing the endpoint information.</span></span> <span data-ttu-id="a7300-133">Sie müssen die entsprechende-Methode zum Abrufen der Endpunkt Informationen abrufen, die für die Dienst Implementierung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a7300-133">You must call the appropriate method to get the endpoint information that is required by the service implementation.</span></span>

<span data-ttu-id="a7300-134">Als Alternative zur manuellen Änderung der COM-Schnittstelle können Sie das Utl2idl-Tool mit dem Schalter **-CI** verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7300-134">As an alternative to manual modification of the COM interface, you can use the Utl2idl tool with the **-ci** switch.</span></span> <span data-ttu-id="a7300-135">Dieser Switch bewirkt, dass das Tool den Endpunkt Informations Parameter den einzelnen Methoden in der COM-Schnittstelle hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="a7300-135">This switch causes the tool to add the endpoint information parameter to each of the methods in the COM interface.</span></span> <span data-ttu-id="a7300-136">Die Verwendung des **-CI-** Schalters vereinfacht die Änderung einzelner Methoden nicht.</span><span class="sxs-lookup"><span data-stu-id="a7300-136">Using the **-ci** switch does not facilitate modification of individual methods.</span></span> <span data-ttu-id="a7300-137">Wenn keine Endpunkt Informationen von allen Methoden einer Schnittstelle benötigt werden, sollten Sie den Parameter manuell hinzufügen, um die effizientesten Implementierungen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="a7300-137">If endpoint information is not needed by all methods of an interface, you should add the parameter manually in order to produce the most efficient implementations.</span></span>

## <a name="implementing-a-service-object"></a><span data-ttu-id="a7300-138">Implementieren eines Dienst Objekts</span><span class="sxs-lookup"><span data-stu-id="a7300-138">Implementing a Service Object</span></span>

<span data-ttu-id="a7300-139">Sie müssen das Utl2idl-Tool verwenden, um die einzelnen Dienst Beschreibungen eines Geräts zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="a7300-139">You must use the Utl2idl tool to translate each service description of a device.</span></span>

<span data-ttu-id="a7300-140">Ein Objekt, das die Funktionalität für einen Dienst bereitstellt, wird als [*Dienst Objekt*](s-gly.md)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a7300-140">An object that provides the functionality for a service is referred to as a [*service object*](s-gly.md).</span></span> <span data-ttu-id="a7300-141">Neben der Bereitstellung von Dienstfunktionen behandeln Dienst Objekte Fehler mithilfe der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a7300-141">In addition to providing service functionality, service objects handle errors by using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a7300-142">Weitere Informationen finden Sie unter [Verwenden der Geräte Host-API mit UPnP-Technologie](using-the-device-host-api-with-upnp-technology.md).</span><span class="sxs-lookup"><span data-stu-id="a7300-142">For more information, see [Using the Device Host API with UPnP Technology](using-the-device-host-api-with-upnp-technology.md).</span></span>

<span data-ttu-id="a7300-143">Um die Kompatibilität mit Visual Basic zu gewährleisten, das keine out-Parameter unterstützt \[ \] , werden die Parameter **Direction** out **/Direction** in der Dienst Beschreibung in \[ , out- \] Parameter in IDL konvertiert.</span><span class="sxs-lookup"><span data-stu-id="a7300-143">To ensure compatibility with Visual Basic, which does not support \[out\] parameters, the **direction** out **/direction** parameters in the service description are converted to \[in, out\] parameters in IDL.</span></span> <span data-ttu-id="a7300-144">Der Server muss diese \[ in-, out- \] Parameter freigeben.</span><span class="sxs-lookup"><span data-stu-id="a7300-144">The server must free these \[in, out\] parameters.</span></span>

## <a name="implementing-a-device-control-object"></a><span data-ttu-id="a7300-145">Implementieren eines Geräte Steuerungs Objekts</span><span class="sxs-lookup"><span data-stu-id="a7300-145">Implementing a Device Control Object</span></span>

<span data-ttu-id="a7300-146">Zusätzlich zum Implementieren von Dienst Objekten müssen Sie ein [*Geräte Steuerungsobjekt*](d-gly.md)implementieren.</span><span class="sxs-lookup"><span data-stu-id="a7300-146">In addition to implementing service objects, you must implement a [*device control object*](d-gly.md).</span></span> <span data-ttu-id="a7300-147">Ein Geräte Steuerungsobjekt ist der zentrale Verwaltungspunkt für die Dienst Objekte des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a7300-147">A device control object is the central point of management and control for the device's service objects.</span></span> <span data-ttu-id="a7300-148">Beim Registrierungs Zeitpunkt wird das Geräte Steuerungsobjekt an den Geräte Host übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a7300-148">At registration time, the device control object is passed to the device host.</span></span> <span data-ttu-id="a7300-149">Wenn ein Ereignis Abonnement oder eine Steuerungs Anforderung für einen der Dienste des Geräts eingeht, ruft der Geräte Host dieses Geräte Steuerungsobjekt auf, um das relevante Dienst Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7300-149">When an event subscription or control request arrives for one of the device's services, the device host calls into this device control object to obtain the relevant service object.</span></span> <span data-ttu-id="a7300-150">Zu diesem Zeitpunkt erstellt das Geräte Steuerungsobjekt entweder eine Instanz des Dienst Objekts oder gibt die-Schnittstelle einer vorhandenen Instanz des Dienst Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="a7300-150">At that time, the device control object either creates an instance of the service object or returns the interface of an existing instance of the service object.</span></span>

<span data-ttu-id="a7300-151">Sie können eine Geräte Beschreibung auf mehreren Computern oder mehrmals auf demselben Computer registrieren.</span><span class="sxs-lookup"><span data-stu-id="a7300-151">You can register a device description on multiple computers or multiple times on the same computer.</span></span> <span data-ttu-id="a7300-152">Da der eindeutige Geräte Name (User Name, udn) für jede Instanz des Geräts anders sein muss, generiert der Geräte Host jedes Mal, wenn das Gerät registriert ist, für jedes Gerät und jedes eingebettete Gerät einen eindeutigen udn.</span><span class="sxs-lookup"><span data-stu-id="a7300-152">Because the Unique Device Name (UDN) must be different for each instance of the device, the device host generates a unique UDN for each device and embedded device each time the device is registered.</span></span> <span data-ttu-id="a7300-153">Verwenden Sie den in der Vorlage Geräte Beschreibung angegebenen udn zum Abrufen des tatsächlichen vom Geräte Host generierten udn, der dem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a7300-153">Use the UDN specified in the device description template to obtain the actual UDN generated by the device host and associated with the device.</span></span> <span data-ttu-id="a7300-154">Zum Aufheben der Registrierung eines Geräts müssen Sie die ID verwenden, die vom UPnP-Framework bereitgestellt wurde, als das Gerät registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7300-154">To unregister a device, you must use the ID provided by the UPnP framework when the device was registered.</span></span>

<span data-ttu-id="a7300-155">Geräte Steuerungs Objekte müssen die [**iupnpabvicecontrol**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="a7300-155">Device control objects must implement the [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) interface.</span></span> <span data-ttu-id="a7300-156">Der Geräte Host ruft die [**iupnpdevicecontrol:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) -Methode des Geräte Steuerungs Objekts auf und übergibt dabei die UPnP-basierte Geräte Beschreibung, die der Geräte Host zuvor für das Gerät veröffentlicht hat, sowie eine Initialisierungs Zeichenfolge, die zum Zeitpunkt der Registrierung angegeben wurde (siehe [Registrieren eines gehosteten Geräts beim Geräte Host](registering-a-hosted-device-with-the-device-host.md)).</span><span class="sxs-lookup"><span data-stu-id="a7300-156">The device host invokes the [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method of the device control object, passing in the UPnP-based device description that the device host previously published for the device and an initialization string that was specified at registration time (see [Registering a Hosted Device with the Device Host](registering-a-hosted-device-with-the-device-host.md)).</span></span> <span data-ttu-id="a7300-157">In dieser Geräte Beschreibung liest das Geräte Steuerungsobjekt die udns, die den einzelnen Geräten in der Gerätestruktur zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="a7300-157">From this device description, the device control object reads the UDNs assigned to each of the devices in the device tree.</span></span> <span data-ttu-id="a7300-158">Zum Abrufen dieser Informationen können Sie auch die [**iupnpregistrinner:: getuniquedevicename**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7300-158">You can also use the [**IUPnPRegistrar::GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) method to obtain this information.</span></span>

<span data-ttu-id="a7300-159">Wenn der Geräte Host einen Zeiger auf ein Dienst Objekt benötigt, das einen bestimmten Dienst implementiert, ruft es die [**iupnpdevicecontrol:: getserviceobject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) -Methode für das Geräte Steuerungsobjekt auf.</span><span class="sxs-lookup"><span data-stu-id="a7300-159">When the device host requires a pointer to a service object that implements a particular service, it invokes the [**IUPnPDeviceControl::GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) method on the device control object.</span></span> <span data-ttu-id="a7300-160">Der Geräte Host übergibt den udn und die Dienst-ID des Diensts, für den er ein Dienst Objekt anfordert, und die Adresse eines [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeigers, an dem die Methode einen Zeiger auf das Dienst Objekt zurückgeben soll.</span><span class="sxs-lookup"><span data-stu-id="a7300-160">The device host passes the UDN and the service ID of the service for which it is requesting a service object and the address of an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer at which the method is expected to return a pointer to the service object.</span></span> <span data-ttu-id="a7300-161">Der udn-Parameter ist erforderlich, da das Objekt "Gerätesteuerung" Dienste für die gesamte Gerätestruktur verwaltet, einschließlich der in den Netz Geräten.</span><span class="sxs-lookup"><span data-stu-id="a7300-161">The UDN parameter is necessary because the device control object manages services for the entire device tree, including nested devices.</span></span> <span data-ttu-id="a7300-162">Wenn der Geräte Host ein geclusterte Gerät anfordert, verwendet **getserviceobject** den udn, um es zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a7300-162">If the device host requests a nested device, **GetServiceObject** uses the UDN to identify it.</span></span>

 

 