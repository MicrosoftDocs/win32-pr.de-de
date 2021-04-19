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
# <a name="implementing-device-behavior"></a>Implementieren von Geräteverhalten

Das Verhalten eines Geräts wird durch die Dienste definiert, die es verfügbar macht. Jeder Dienst verfügt über eine Dienst Beschreibung, die seine Aktionen und Zustandsvariablen auflistet. Zusammen bilden diese Dienst Beschreibungen die Dienst Schnittstelle, die definiert, wie ein Steuerungspunkt mit einem Dienst interagieren kann. Jeder Dienst muss mindestens eine Aktion haben.

Um einen Dienst zu implementieren, muss ein gehostetes Gerät ein Component Object Model (com)-Objekt bereitstellen, das die-Schnittstelle für den Dienst verfügbar macht. In der Dienst Beschreibung werden die Dienst Schnittstellen in der UPnP-Vorlagen Sprache (UTL) angegeben. Allerdings werden COM-Objekt Schnittstellen in der Regel in IDL (Interface Definition Language) angegeben. Sie können auch die COM-Schnittstelle in einer Typbibliothek oder Header Datei angeben. Das Platform Software Development Kit (SDK) umfasst das Tool Utl2idl, das eine Dienst Beschreibung in UTL in eine COM-Schnittstelle in IDL übersetzt.

In den folgenden Beispielen wird dieser Konvertierungsprozess veranschaulicht. Die Dienst Beschreibung wird vom Geräte Entwickler bereitgestellt und in UTL geschrieben.

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

Der nächste Schritt besteht darin, das Utl2idl-Tool auszuführen. Sie erzeugt die IDL-Datei, die die COM-Schnittstelle enthält. Weitere Informationen zu IDL-Dateien und zum **Schnittstellen** Schlüsselwort finden Sie unter [Schnittstellen Definitionsdatei (IDL)](/windows/desktop/Midl/interface-definition-idl-file) und [**Schnittstelle**](/windows/desktop/Midl/interface) in der mittleren l-Referenz.

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
> Der Rückgabewert ist der erste \[ out- \] Parameter in der Liste der Argumente in der Dienst Beschreibung. er wird jedoch nach der Übersetzung als letzter Parameter aufgeführt.
> 
> Alle anderen Parameter verbleiben in derselben Reihenfolge.

 

Um die Funktionalität des Dienstanbieter bereitzustellen, implementieren Sie diese COM-Schnittstelle.

## <a name="obtaining-information-about-an-endpoint"></a>Abrufen von Informationen zu einem Endpunkt

Im UPnP-Framework enthalten die Endpunkt Informationen Informationen zu einer Anforderung und ihrer Quelle. Ein Gerät kann diese Informationen überprüfen, um eine Entscheidung über die Anforderung zu treffen.

Endpunkt Informationen sind optional für den implementierten Dienst verfügbar. Der Geräte Host hat Zugriff auf Endpunkt Informationen. der Geräte Host kommuniziert die Informationen jedoch nicht standardmäßig mit dem implementierten Dienst. Sie können den Geräte Host aktivieren, um die Endpunkt Informationen für den implementierten Dienst freizugeben, indem Sie die COM-Schnittstelle in der IDL-Datei (die vom Utl2idl-Tool erstellt wurde) ändern. Sie können \[ \] jeder Methode, die Endpunkt Informationen erfordert, einen in-Parameter hinzufügen. Der zusätzliche \[ in- \] Parameter muss der erste in der Liste der Argumente, ein Zeiger auf eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle und explizit " **punkremoteendpointinfo**" genannt werden. Änderungen an der Dienst-XML sind nicht erforderlich oder werden empfohlen. Das folgende Beispiel zeigt die neue Definition der **PowerOn** -Methode, wenn Sie so geändert wird, dass Sie Endpunkt Informationen empfängt:

"HRESULT PowerOn ( \[ in \] IUnknown \* punkremoteendpointinfo);"

Ein Zeiger auf ein Endpunkt Informationsobjekt, eine [**iupnpremoteendpointinfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) -Schnittstelle, wird durch den neuen Parameter vom Geräte Host übergeben. Die **iupnpremoteendpointinfo** -Schnittstelle bietet drei Methoden für den Zugriff auf die Endpunkt Informationen. Sie müssen die entsprechende-Methode zum Abrufen der Endpunkt Informationen abrufen, die für die Dienst Implementierung erforderlich sind.

Als Alternative zur manuellen Änderung der COM-Schnittstelle können Sie das Utl2idl-Tool mit dem Schalter **-CI** verwenden. Dieser Switch bewirkt, dass das Tool den Endpunkt Informations Parameter den einzelnen Methoden in der COM-Schnittstelle hinzufügt. Die Verwendung des **-CI-** Schalters vereinfacht die Änderung einzelner Methoden nicht. Wenn keine Endpunkt Informationen von allen Methoden einer Schnittstelle benötigt werden, sollten Sie den Parameter manuell hinzufügen, um die effizientesten Implementierungen zu entwickeln.

## <a name="implementing-a-service-object"></a>Implementieren eines Dienst Objekts

Sie müssen das Utl2idl-Tool verwenden, um die einzelnen Dienst Beschreibungen eines Geräts zu übersetzen.

Ein Objekt, das die Funktionalität für einen Dienst bereitstellt, wird als [*Dienst Objekt*](s-gly.md)bezeichnet. Neben der Bereitstellung von Dienstfunktionen behandeln Dienst Objekte Fehler mithilfe der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. Weitere Informationen finden Sie unter [Verwenden der Geräte Host-API mit UPnP-Technologie](using-the-device-host-api-with-upnp-technology.md).

Um die Kompatibilität mit Visual Basic zu gewährleisten, das keine out-Parameter unterstützt \[ \] , werden die Parameter **Direction** out **/Direction** in der Dienst Beschreibung in \[ , out- \] Parameter in IDL konvertiert. Der Server muss diese \[ in-, out- \] Parameter freigeben.

## <a name="implementing-a-device-control-object"></a>Implementieren eines Geräte Steuerungs Objekts

Zusätzlich zum Implementieren von Dienst Objekten müssen Sie ein [*Geräte Steuerungsobjekt*](d-gly.md)implementieren. Ein Geräte Steuerungsobjekt ist der zentrale Verwaltungspunkt für die Dienst Objekte des Geräts. Beim Registrierungs Zeitpunkt wird das Geräte Steuerungsobjekt an den Geräte Host übermittelt. Wenn ein Ereignis Abonnement oder eine Steuerungs Anforderung für einen der Dienste des Geräts eingeht, ruft der Geräte Host dieses Geräte Steuerungsobjekt auf, um das relevante Dienst Objekt abzurufen. Zu diesem Zeitpunkt erstellt das Geräte Steuerungsobjekt entweder eine Instanz des Dienst Objekts oder gibt die-Schnittstelle einer vorhandenen Instanz des Dienst Objekts zurück.

Sie können eine Geräte Beschreibung auf mehreren Computern oder mehrmals auf demselben Computer registrieren. Da der eindeutige Geräte Name (User Name, udn) für jede Instanz des Geräts anders sein muss, generiert der Geräte Host jedes Mal, wenn das Gerät registriert ist, für jedes Gerät und jedes eingebettete Gerät einen eindeutigen udn. Verwenden Sie den in der Vorlage Geräte Beschreibung angegebenen udn zum Abrufen des tatsächlichen vom Geräte Host generierten udn, der dem Gerät zugeordnet ist. Zum Aufheben der Registrierung eines Geräts müssen Sie die ID verwenden, die vom UPnP-Framework bereitgestellt wurde, als das Gerät registriert wurde.

Geräte Steuerungs Objekte müssen die [**iupnpabvicecontrol**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) -Schnittstelle implementieren. Der Geräte Host ruft die [**iupnpdevicecontrol:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) -Methode des Geräte Steuerungs Objekts auf und übergibt dabei die UPnP-basierte Geräte Beschreibung, die der Geräte Host zuvor für das Gerät veröffentlicht hat, sowie eine Initialisierungs Zeichenfolge, die zum Zeitpunkt der Registrierung angegeben wurde (siehe [Registrieren eines gehosteten Geräts beim Geräte Host](registering-a-hosted-device-with-the-device-host.md)). In dieser Geräte Beschreibung liest das Geräte Steuerungsobjekt die udns, die den einzelnen Geräten in der Gerätestruktur zugewiesen sind. Zum Abrufen dieser Informationen können Sie auch die [**iupnpregistrinner:: getuniquedevicename**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) -Methode verwenden.

Wenn der Geräte Host einen Zeiger auf ein Dienst Objekt benötigt, das einen bestimmten Dienst implementiert, ruft es die [**iupnpdevicecontrol:: getserviceobject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) -Methode für das Geräte Steuerungsobjekt auf. Der Geräte Host übergibt den udn und die Dienst-ID des Diensts, für den er ein Dienst Objekt anfordert, und die Adresse eines [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeigers, an dem die Methode einen Zeiger auf das Dienst Objekt zurückgeben soll. Der udn-Parameter ist erforderlich, da das Objekt "Gerätesteuerung" Dienste für die gesamte Gerätestruktur verwaltet, einschließlich der in den Netz Geräten. Wenn der Geräte Host ein geclusterte Gerät anfordert, verwendet **getserviceobject** den udn, um es zu identifizieren.

 

 