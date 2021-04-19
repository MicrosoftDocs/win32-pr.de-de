---
description: Der System Registrierungs Anbieter wird als Teil des WMI-Installationsvorgangs unter Windows registriert.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Der System Registrierungs Anbieter wird registriert.
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359989"
---
# <a name="registering-the-system-registry-provider"></a>Der System Registrierungs Anbieter wird registriert.

Der System Registrierungs Anbieter wird als Teil des WMI-Installationsvorgangs unter Windows registriert. Wenn Sie eine andere Plattform verwenden und den System Registrierungs Anbieter verwenden möchten, müssen Sie zuerst den Anbieter registrieren, indem Sie die nachstehend beschriebenen Schritte ausführen.

Im folgenden Verfahren wird beschrieben, wie der System Registrierungs Anbieter registriert wird.

**So registrieren Sie den System Registrierungs Anbieter**

1.  Registrieren Sie den Anbieter als com-Server.

    Falls erforderlich, müssen Sie möglicherweise Registrierungseinträge erstellen. Dieser Vorgang gilt für alle com-Server und steht nicht im Zusammenhang mit WMI. Weitere Informationen finden Sie in der [com](https://msdn.microsoft.com/library/aa139695.aspx) -Dokumentation im Microsoft Windows Software Development Kit (SDK).

2.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, um die Implementierung des System Registrierungs Anbieters zu beschreiben.

    Die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz beschreibt den Namen des Anbieters und dessen Klassen Bezeichner (**CLSID**).

    Im folgenden Beispiel wird beschrieben, wie [**\_ \_ Win32Provider**](--win32provider.md) als Instanzeigenschaft, Ereignis oder Methoden Anbieter registriert wird.

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  Erstellen Sie eine oder mehrere Instanzen von Klassen, die von der [**\_ \_ providerregistration**](--providerregistration.md) -Klasse abgeleitet werden, um die logische Implementierung des System Registrierungs Anbieters zu beschreiben.

    Abhängig von dem Zweck, für den Sie den System Registrierungs Anbieter registrieren, können Sie eine oder mehrere der folgenden Klassen erstellen.

    [**\_\_Instanceproviderregistration**](--instanceproviderregistration.md)

    [**\_\_Propertyproviderregistration**](--propertyproviderregistration.md)

    [**\_\_Eventproviderregistration**](--eventproviderregistration.md)

    [**\_\_Methodproviderregistration**](--methodproviderregistration.md)

    Im folgenden MOF-Codebeispiel wird beschrieben, wie Sie den System Registrierungs Anbieter als Instanz, Eigenschaft, Ereignis oder Methoden Anbieter registrieren können.

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  Kompilieren Sie die MOF-Datei mit dem MOF-Compiler oder der [**imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Schnittstelle.

Die regevent. MOF-Datei, die im WMI-Abschnitt des Windows SDK bereitgestellt wird, enthält die [**\_ \_ Win32Provider**](--win32provider.md) -und [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Instanzen, die zum Registrieren des System Registrierungs Anbieters als Ereignis Anbieter erforderlich sind. Weitere Informationen zum Registrieren eines Anbieters finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md) und [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).

 

 



