---
description: Vor der Implementierung des Anbieters sollten Sie zunächst Ihren Anbieter bei WMI registrieren. Beim Registrieren des Anbieters werden der Typ des Anbieters und die vom Anbieter unterstützten Klassen definiert. WMI kann nur auf registrierte Anbieter zugreifen.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registrieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364054"
---
# <a name="registering-a-provider"></a>Registrieren eines Anbieters

Vor der Implementierung des Anbieters sollten Sie zunächst Ihren Anbieter bei WMI registrieren. Beim Registrieren des Anbieters werden der Typ des Anbieters und die vom Anbieter unterstützten Klassen definiert. WMI kann nur auf registrierte Anbieter zugreifen.

> [!Note]  
> Weitere Informationen zum Registrieren eines Mi-Anbieters finden Sie unter Gewusst [wie: Registrieren eines Mi-Anbieters](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).

 

Sie können den Anbieter Code schreiben, bevor Sie den Anbieter registrieren. Es ist jedoch sehr schwierig, einen Anbieter zu debuggen, der nicht bei WMI registriert ist. Wenn Sie die Schnittstellen für Ihren Anbieter ermitteln, können Sie auch den Zweck und die Struktur eines Anbieters gliedern. Daher hilft Ihnen die Registrierung Ihres Anbieters beim Entwerfen Ihres Anbieters.

Nur Administratoren können einen Anbieter registrieren oder löschen.

Ein Anbieter muss für alle unterschiedlichen Typen von Anbieter Funktionen registriert werden, die er ausführt. Fast alle Anbieter stellen Instanzen von Klassen bereit, die Sie definieren, aber Sie können auch Eigenschafts Daten, Methoden, Ereignisse oder Klassen bereitstellen. Der Anbieter kann auch als Ereignisconsumeranbieter oder Leistungsindikatorenanbieter registriert werden. Es wird empfohlen, dass Sie alle Anbieter Funktionen in einem Anbieter kombinieren, anstatt für jeden Typ viele separate Anbieter zu haben. Ein Beispiel hierfür ist der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider), der Methoden und Instanzen bereitstellt, sowie der Anbieter für Daten [Träger Kontingente](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), der Instanzen, Methoden und Ereignisse bereitstellt.

Ein Anbieter muss für alle unterschiedlichen Typen von Anbieter Funktionen registriert werden, die er ausführt. Fast alle Anbieter stellen Instanzen von Klassen bereit, die Sie definieren, aber Sie können auch Eigenschafts Daten, Methoden, Ereignisse oder Klassen bereitstellen. Der Anbieter kann auch als Ereignisconsumeranbieter oder Leistungsindikatorenanbieter registriert werden.

Dieselbe Instanz von [**\_ \_ Win32Provider**](--win32provider.md) wird für jeden Registrierungstyp verwendet:

-   [Registrieren eines Instanzanbieters](registering-an-instance-provider.md)
-   [Registrieren eines Klassen Anbieters](registering-a-class-provider.md)
-   [Registrieren eines Methoden Anbieters](registering-a-method-provider.md)
-   [Registrieren eines Ereignis Anbieters](registering-an-event-provider.md)
-   [Registrieren eines Ereignisconsumeranbieters](registering-an-event-consumer-provider.md)
-   [Erstellen eines Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>Beispiel: Erstellen und Registrieren einer Instanz eines Anbieters

Das folgende Beispiel zeigt eine MOF-Datei, die eine Instanz des [System Registrierungs Anbieters](/previous-versions/windows/desktop/regprov/system-registry-provider) im root cimv2-Namespace erstellt und registriert \\ . Er weist den Alias $reg dem Anbieter zu, um den für die Instanz-und Methoden Registrierungen erforderlichen langen Pfadnamen zu vermeiden. Weitere Informationen finden Sie unter [Erstellen eines Alias](creating-an-alias.md).

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a>Beispiel: Registrieren eines Anbieters

Im folgenden Verfahren wird beschrieben, wie Sie einen-Anbieter registrieren.

**So registrieren Sie einen Anbieter**

1.  Registrieren Sie den Anbieter als com-Server.

    Falls erforderlich, müssen Sie möglicherweise Registrierungseinträge erstellen. Dieser Vorgang gilt für alle com-Server und steht nicht im Zusammenhang mit WMI. Weitere Informationen finden Sie im Abschnitt zu com in der Dokumentation zum Microsoft Windows Software Development Kit (SDK).

2.  Erstellen Sie eine MOF-Datei, die Instanzen von [**\_ \_ Win32Provider**](--win32provider.md) und eine Instanz einer Klasse enthält, die entweder direkt oder indirekt von [**\_ \_ providerregistration**](--providerregistration.md)(z. b. [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md)) abgeleitet wird. Nur Administratoren können einen Anbieter registrieren oder löschen, indem Sie Instanzen von Klassen erstellen, die von **\_ \_ Win32Provider** oder [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet werden.
3.  Legen Sie das [**hostingmodel**](--win32provider.md) in der Instanz von **\_ \_ Win32Provider** entsprechend den Werten in den [Hostingmodellen](provider-hosting-and-security.md)fest.

    > [!Note]  
    > Wenn der Anbieter die hohen Berechtigungen des Kontos LocalSystem erfordert, sollte die Eigenschaft [**\_ \_ Win32Provider. hostingmodel**](--win32provider.md) auf networkservicehost festgelegt werden. Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

     

    Das folgende MOF-Beispiel aus dem vollständigen Beispiel zeigt den Code, der eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md)erstellt.

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  Eine Instanz einer Klasse, die entweder direkt oder indirekt von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet wird, um die logische Implementierung des Anbieters zu beschreiben. Ein Anbieter kann für verschiedene Arten von Funktionen registriert werden. Im obigen Beispiel wird RegProv als Instanz-und Methoden Anbieter registriert. Wenn RegProv die Funktionalität jedoch unterstützt, kann Sie auch als Eigenschaft oder Ereignis Anbieter registriert werden. In der folgenden Tabelle werden die-Klassen aufgelistet, die Anbieter Funktionen registrieren.

    

    | Anbieter Registrierungs Klassen                                                        | BESCHREIBUNG                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_Instanceproviderregistration**](--instanceproviderregistration.md)           | Registriert einen [Instanzanbieter](registering-an-instance-provider.md).             |
    | [**\_\_Eventproviderregistration**](--eventproviderregistration.md)                 | Registriert einen [Ereignis Anbieter](registering-an-event-provider.md).                   |
    | [**\_\_Eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) | Registriert einen [Ereignisconsumeranbieter](registering-an-event-consumer-provider.md). |
    | [**\_\_Methodproviderregistration**](--methodproviderregistration.md)               | Registriert einen [Methoden Anbieter](registering-an-event-consumer-provider.md).          |
    | [**\_\_Propertyproviderregistration**](--propertyproviderregistration.md)           | Registriert einen [Eigenschaften Anbieter](registering-a-property-provider.md).               |

    

     

5.  Platzieren Sie die MOF-Datei in einem permanenten Verzeichnis.

    In der Regel sollten Sie die Datei im Installationsverzeichnis des Anbieters platzieren.

6.  Kompilieren [Sie die](mofcomp.md) MOF-Datei mit der [**-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) von "MOF".

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

    **Windows 8 und Windows Server 2012:** Beim Installieren von Anbietern werden [](mofcomp.md) [**die**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) \[ Schlüssel \] -und \[ statischen \] Qualifizierer unabhängig von ihren tatsächlichen Werten als true behandelt, wenn Sie vorhanden sind. Andere Qualifizierer werden als false behandelt, wenn Sie vorhanden sind, aber nicht explizit auf true festgelegt sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 
