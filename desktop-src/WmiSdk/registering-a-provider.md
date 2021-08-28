---
description: Bevor Sie Ihren Anbieter implementieren, sollten Sie zuerst Ihren Anbieter bei WMI registrieren. Beim Registrieren des Anbieters werden der Typ des Anbieters und die vom Anbieter unterstützten Klassen definiert. WMI kann nur auf registrierte Anbieter zugreifen.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registrieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265d3a9f8617c68793fc30c0dc23fd3e9f0106ee98a9e3c757754e2fe589dda8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995920"
---
# <a name="registering-a-provider"></a>Registrieren eines Anbieters

Bevor Sie Ihren Anbieter implementieren, sollten Sie zuerst Ihren Anbieter bei WMI registrieren. Beim Registrieren des Anbieters werden der Typ des Anbieters und die vom Anbieter unterstützten Klassen definiert. WMI kann nur auf registrierte Anbieter zugreifen.

> [!Note]  
> Weitere Informationen zum Registrieren eines MI-Anbieters finden Sie unter [Vorgehensweise: Registrieren eines MI-Anbieters.](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider)

 

Sie können Ihren Anbietercode schreiben, bevor Sie den Anbieter registrieren. Es ist jedoch sehr schwierig, einen Anbieter zu debuggen, der nicht bei WMI registriert ist. Die Bestimmung der Schnittstellen für Ihren Anbieter hilft auch dabei, den Zweck und die Struktur eines Anbieters zu beschreiben. Daher hilft Ihnen die Registrierung Ihres Anbieters beim Entwerfen Ihres Anbieters.

Nur Administratoren können einen Anbieter registrieren oder löschen.

Ein Anbieter muss für alle verschiedenen Typen von Anbieterfunktionen registriert werden, die er ausführt. Fast alle Anbieter stellen Instanzen von Klassen bereit, die sie definieren, aber sie können auch Eigenschaftsdaten, Methoden, Ereignisse oder Klassen bereitstellen. Der Anbieter kann auch als Ereignisverbraucheranbieter oder Leistungsindikatoranbieter registriert werden. Es wird empfohlen, alle Anbieterfunktionen in einem Anbieter zu kombinieren, anstatt für jeden Typ mehrere separate Anbieter zu verwenden. Ein Beispiel ist der [Systemregistrierungsanbieter](/previous-versions/windows/desktop/regprov/system-registry-provider), der Methoden und Instanzen bereitstellt, und der [Datenträgerkontingentanbieter](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), der Instanzen, Methoden und Ereignisse bereitstellt.

Ein Anbieter muss für alle verschiedenen Typen von Anbieterfunktionen registriert werden, die er ausführt. Fast alle Anbieter stellen Instanzen von Klassen bereit, die sie definieren, aber sie können auch Eigenschaftsdaten, Methoden, Ereignisse oder Klassen bereitstellen. Der Anbieter kann auch als Ereignisverbraucheranbieter oder Leistungsindikatoranbieter registriert werden.

Die gleiche Instanz von [**\_ \_ Win32Provider**](--win32provider.md) wird für jeden Registrierungstyp verwendet:

-   [Registrieren eines Instanzanbieters](registering-an-instance-provider.md)
-   [Registrieren eines Klassenanbieters](registering-a-class-provider.md)
-   [Registrieren eines Methodenanbieters](registering-a-method-provider.md)
-   [Registrieren eines Ereignisanbieters](registering-an-event-provider.md)
-   [Registrieren eines Ereignisverbraucheranbieters](registering-an-event-consumer-provider.md)
-   [Erstellen eines Instanzanbieters zu einem High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>Beispiel: Erstellen und Registrieren einer Instanz eines Anbieters

Das folgende Beispiel zeigt eine MOF-Datei, die eine Instanz des [Systemregistrierungsanbieters](/previous-versions/windows/desktop/regprov/system-registry-provider) im \\ cimv2-Stammnamespace erstellt und registriert. Sie weist dem Anbieter den Alias $Reg zu, um den langen Pfadnamen zu vermeiden, der in den Instanz- und Methodenregistrierungen erforderlich ist. Weitere Informationen finden Sie unter [Erstellen eines Alias.](creating-an-alias.md)

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

Im folgenden Verfahren wird beschrieben, wie ein Anbieter registriert wird.

**So registrieren Sie einen Anbieter**

1.  Registrieren Sie den Anbieter als COM-Server.

    Bei Bedarf müssen Sie möglicherweise Registrierungseinträge erstellen. Dieser Prozess gilt für alle COM-Server und steht nicht im Zusammenhang mit WMI. Weitere Informationen finden Sie im Com-Abschnitt in der Dokumentation zum Microsoft Windows Software Development Kit (SDK).

2.  Erstellen Sie eine MOF-Datei, die Instanzen von [**\_ \_ Win32Provider**](--win32provider.md) und eine Instanz einer Klasse enthält, die entweder direkt oder indirekt von [**\_ \_ ProviderRegistration**](--providerregistration.md)abgeleitet wird, z. B. [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Nur Administratoren können einen Anbieter registrieren oder löschen, indem sie Instanzen von Klassen erstellen, die von **\_ \_ Win32Provider** oder [**\_ \_ ProviderRegistration**](--providerregistration.md)abgeleitet sind.
3.  Legen Sie das [**HostingModel**](--win32provider.md) in der Instanz von **\_ \_ Win32Provider** entsprechend den Werten in [Hostingmodelle](provider-hosting-and-security.md)fest.

    > [!Note]  
    > Sofern der Anbieter nicht die hohen Berechtigungen des LocalSystem-Kontos erfordert, sollte die [**\_ \_ Win32Provider.HostingModel-Eigenschaft**](--win32provider.md) auf "NetworkServiceHost" festgelegt werden. Weitere Informationen finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)

     

    Das folgende MOF-Beispiel aus dem vollständigen Beispiel zeigt den Code, der eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md)erstellt.

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  Eine Instanz einer Klasse, die entweder direkt oder indirekt von [**\_ \_ ProviderRegistration**](--providerregistration.md)abgeleitet wird, um die logische Implementierung des Anbieters zu beschreiben. Ein Anbieter kann für verschiedene Arten von Funktionen registriert werden. Im obigen Beispiel wird RegProv als Instanz- und Methodenanbieter registriert. Wenn RegProv die Funktionalität jedoch unterstützt, kann sie auch als Eigenschaften- oder Ereignisanbieter registriert werden. In der folgenden Tabelle sind die Klassen aufgeführt, die die Anbieterfunktionalität registrieren.

    

    | Anbieterregistrierungsklassen                                                        | Beschreibung                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)           | Registriert einen [Instanzanbieter.](registering-an-instance-provider.md)             |
    | [**\_\_EventProviderRegistration**](--eventproviderregistration.md)                 | Registriert einen [Ereignisanbieter.](registering-an-event-provider.md)                   |
    | [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) | Registriert einen [Ereignisverbraucheranbieter.](registering-an-event-consumer-provider.md) |
    | [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)               | Registriert einen [Methodenanbieter.](registering-an-event-consumer-provider.md)          |
    | [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)           | Registriert einen [Eigenschaftenanbieter.](registering-a-property-provider.md)               |

    

     

5.  Platzieren Sie die MOF-Datei in einem permanenten Verzeichnis.

    In der Regel sollten Sie die Datei im Installationsverzeichnis des Anbieters platzieren.

6.  Kompilieren Sie die MOF-Datei mithilfe von [mofcomp](mofcomp.md) oder der [**IMofCompiler-Schnittstelle.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

    **Windows 8 und Windows Server 2012:** Beim Installieren von Anbietern behandeln [**sowohl mofcomp**](mofcomp.md) als auch die [**IMofCompiler-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) die \[ Key- \] und \[ \] Static-Qualifizierer als true, wenn sie vorhanden sind, unabhängig von ihren tatsächlichen Werten. Andere Qualifizierer werden als FALSE behandelt, wenn sie vorhanden sind, aber nicht explizit auf TRUE festgelegt sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsbeschreibungen](setting-namespace-security-descriptors.md)
</dt> <dt>

[Schützen Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 
