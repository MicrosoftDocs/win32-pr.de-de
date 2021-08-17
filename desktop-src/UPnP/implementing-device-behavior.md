---
title: Implementieren des Geräteverhaltens
description: Das Verhalten eines Geräts wird durch die verfügbaren Dienste definiert.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce2857c11a02ef5eeebe7b2cd5e75ee76138929e5bd95a2e3bdfa7ffd2c71dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137263"
---
# <a name="implementing-device-behavior"></a>Implementieren des Geräteverhaltens

Das Verhalten eines Geräts wird durch die verfügbaren Dienste definiert. Jeder Dienst verfügt über eine Dienstbeschreibung, die seine Aktionen und Zustandsvariablen auflistet. Zusammen stellen diese Dienstbeschreibungen die Dienstschnittstelle zusammen, die definiert, wie ein Steuerungspunkt mit einem Dienst interagieren kann. Jeder Dienst muss mindestens eine Aktion haben.

Um einen Dienst zu implementieren, muss ein gehostetes Gerät ein Component Object Model (COM)-Objekt bereitstellen, das die Schnittstelle für den Dienst verfügbar macht. In der Dienstbeschreibung werden die Dienstschnittstellen in UPnP Template Language (UTL) angegeben. COM-Objektschnittstellen werden jedoch in der Regel in Interface Definition Language (IDL) angegeben. Sie können die COM-Schnittstelle auch in einer Typbibliothek oder Headerdatei angeben. Das Platform Software Development Kit (SDK) enthält das Utl2idl-Tool, das eine Dienstbeschreibung in UTL in eine COM-Schnittstelle in IDL übersetzt.

Die folgenden Beispiele veranschaulichen diesen Konvertierungsprozess. Die Dienstbeschreibung wird vom Geräteentwickler bereitgestellt und in UTL geschrieben.

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

Der nächste Schritt besteht im Ausführen des Utl2idl-Tools. Sie erzeugt die IDL-Datei, die die COM-Schnittstelle enthält. Weitere Informationen zu IDL-Dateien und dem **Schlüsselwort interface** finden Sie [**unter**](/windows/desktop/Midl/interface) Interface [Definition (IDL)-Datei](/windows/desktop/Midl/interface-definition-idl-file) und -Schnittstelle in der MIDL-Referenz.

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
> Der Rückgabewert ist der erste out-Parameter in der Liste der Argumente in der Dienstbeschreibung. Er wird jedoch als letzter Parameter nach der \[ \] Übersetzung aufgeführt.
> 
> Alle anderen Parameter bleiben in der gleichen Reihenfolge.

 

Implementieren Sie diese COM-Schnittstelle, um die Funktionalität des Diensts zur Verfügung zu stellen.

## <a name="obtaining-information-about-an-endpoint"></a>Abrufen von Informationen zu einem Endpunkt

Im UPnP-Framework enthalten Endpunktinformationen Informationen zu einer Anforderung und ihrer Quelle. Ein Gerät kann diese Informationen überprüfen, um eine Entscheidung über die Anforderung zu treffen.

Endpunktinformationen sind optional für den implementierten Dienst verfügbar. Der Gerätehost hat Zugriff auf Endpunktinformationen. Der Gerätehost übermittelt die Informationen jedoch nicht standardmäßig an den implementierten Dienst. Sie können es dem Gerätehost ermöglichen, die Endpunktinformationen für den implementierten Dienst zu teilen, indem Sie die COM-Schnittstelle in der IDL-Datei ändern (erstellt vom Utl2idl-Tool). Sie können jeder Methode, die \[ \] Endpunktinformationen erfordert, einen in-Parameter hinzufügen. Der zusätzliche in-Parameter muss der erste in der Liste der Argumente sein, ein Zeiger auf eine IUnknown-Schnittstelle und explizit mit dem Namen \[ \] **eigenschaftRemoteEndpointInfo**. [](/windows/win32/api/unknwn/nn-unknwn-iunknown) Änderungen an der Dienst-XML sind nicht erforderlich oder werden nicht empfohlen. Das folgende Beispiel zeigt die neue Definition der **PowerOn-Methode,** wenn sie geändert wird, sodass sie Endpunktinformationen empfängt:

"HRESULT PowerOn( \[ in \] IUnknown \* quot;RemoteEndpointInfo);"

Ein Zeiger auf ein Endpunktinformationsobjekt, eine [**IUPnPRemoteEndpointInfo-Schnittstelle,**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) wird durch diesen neuen Parameter vom Gerätehost übergeben. Die **IUPnPRemoteEndpointInfo-Schnittstelle** stellt drei Methoden für den Zugriff auf die Endpunktinformationen bereit. Sie müssen die entsprechende Methode aufrufen, um die Endpunktinformationen zu erhalten, die für die Dienstimplementierung erforderlich sind.

Als Alternative zur manuellen Änderung der COM-Schnittstelle können Sie das Utl2idl-Tool mit dem **Schalter -ci** verwenden. Dieser Schalter bewirkt, dass das Tool den Endpunktinformationsparameter zu jeder der Methoden in der COM-Schnittstelle hinzufüge. Die Verwendung **des Schalters -ci** erleichtert keine Änderung einzelner Methoden. Wenn Endpunktinformationen nicht von allen Methoden einer Schnittstelle benötigt werden, sollten Sie den Parameter manuell hinzufügen, um die effizientesten Implementierungen zu erzeugen.

## <a name="implementing-a-service-object"></a>Implementieren eines Dienstobjekts

Sie müssen das Utl2idl-Tool verwenden, um jede Dienstbeschreibung eines Geräts zu übersetzen.

Ein Objekt, das die Funktionalität für einen Dienst bietet, wird als [*Dienstobjekt bezeichnet.*](s-gly.md) Zusätzlich zur Bereitstellung von Dienstfunktionen behandeln Dienstobjekte Fehler mithilfe der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Weitere Informationen finden Sie unter [Verwenden der Gerätehost-API mit UPnP-Technologie.](using-the-device-host-api-with-upnp-technology.md)

Um die Kompatibilität mit Visual Basic zu gewährleisten, die keine Out-Parameter unterstützt, werden die Richtungs-/Richtungsparameter in der Dienstbeschreibung \[ \] in  \[ In-Out-Parameter in \] IDL konvertiert. Der Server muss diese \[ In-Out-Parameter \] frei geben.

## <a name="implementing-a-device-control-object"></a>Implementieren eines Gerätesteuerungsobjekts

Zusätzlich zur Implementierung von Dienstobjekten müssen Sie ein [*Gerätesteuerungsobjekt implementieren.*](d-gly.md) Ein Gerätesteuerungsobjekt ist der zentrale Verwaltungs- und Steuerungspunkt für die Dienstobjekte des Geräts. Zum Zeitpunkt der Registrierung wird das Gerätesteuerungsobjekt an den Gerätehost übergeben. Wenn ein Ereignisabonnement oder eine Steuerungsanforderung für einen der Gerätedienste eintrifft, ruft der Gerätehost dieses Gerätesteuerungsobjekt auf, um das entsprechende Dienstobjekt zu erhalten. Zu diesem Zeitpunkt erstellt das Gerätesteuerungsobjekt entweder eine Instanz des Dienstobjekts oder gibt die Schnittstelle einer vorhandenen Instanz des Dienstobjekts zurück.

Sie können eine Gerätebeschreibung auf mehreren Computern oder mehrmals auf demselben Computer registrieren. Da der eindeutige Gerätename (Unique Device Name, UDN) für jede Instanz des Geräts unterschiedlich sein muss, generiert der Gerätehost bei jeder Registrierung des Geräts einen eindeutigen UDN für jedes Gerät und eingebettete Gerät. Verwenden Sie den in der Gerätebeschreibungsvorlage angegebenen UDN, um die tatsächliche UDN zu erhalten, die vom Gerätehost generiert und dem Gerät zugeordnet wurde. Zum Aufheben der Registrierung eines Geräts müssen Sie die ID verwenden, die beim Registrieren des Geräts vom UPnP-Framework bereitgestellt wurde.

Gerätesteuerungsobjekte müssen die [**IUPnPDeviceControl-Schnittstelle**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) implementieren. Der Gerätehost ruft die [**IUPnPDeviceControl::Initialize-Methode**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) des Gerätesteuerungsobjekts auf und übergibt dabei die UPnP-basierte Gerätebeschreibung, die der Gerätehost zuvor für das Gerät veröffentlicht hat, und eine Initialisierungszeichenfolge, die zur Registrierungszeit angegeben wurde (siehe Registrieren eines gehosteten Geräts beim [Gerätehost).](registering-a-hosted-device-with-the-device-host.md) Aus dieser Gerätebeschreibung liest das Gerätesteuerungsobjekt die UDNs, die den einzelnen Geräten in der Gerätestruktur zugewiesen sind. Sie können diese Informationen auch mithilfe der [**IUPnPRegistrar::GetUniqueDeviceName-Methode**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) abrufen.

Wenn der Gerätehost einen Zeiger auf ein Dienstobjekt erfordert, das einen bestimmten Dienst implementiert, ruft er die [**IUPnPDeviceControl::GetServiceObject-Methode**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) für das Gerätesteuerungsobjekt auf. Der Gerätehost übergibt den UDN und die Dienst-ID des Diensts, für den er ein Dienstobjekt angibt, und die Adresse eines [**IDispatch-Zeigers,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) an dem die Methode voraussichtlich einen Zeiger auf das Dienstobjekt zurückgibt. Der UDN-Parameter ist erforderlich, da das Gerätesteuerungsobjekt Dienste für die gesamte Gerätestruktur verwaltet, einschließlich geschachtelter Geräte. Wenn der Gerätehost ein geschachtelte Gerät an fordert, verwendet **GetServiceObject** den UDN, um es zu identifizieren.

 

 