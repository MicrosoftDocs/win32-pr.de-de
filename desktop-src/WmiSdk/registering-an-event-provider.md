---
description: Um einen WMI-Ereignisanbieter zu erstellen, müssen Sie die Win32Provider-Instanz registrieren, die Ihren Anbieter darstellt, indem Sie eine \_ \_ Instanz von \_ \_ EventProviderRegistration verwenden.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registrieren eines Ereignisanbieters
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 44c6521e56441c929ef108ce4c4b624c11b06ca26dc508c8f2f924e2f87babba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992510"
---
# <a name="registering-an-event-provider"></a>Registrieren eines Ereignisanbieters

Um einen [*WMI-Ereignisanbieter zu erstellen,*](gloss-e.md) müssen Sie die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) registrieren, die Ihren Anbieter darstellt, indem Sie eine Instanz von [**\_ \_ EventProviderRegistration verwenden.**](--eventproviderregistration.md) Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Beim folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters beschrieben.](registering-a-provider.md)

Im folgenden Verfahren wird beschrieben, wie Sie einen Ereignisanbieter registrieren.

**So registrieren Sie einen Ereignisanbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) die den Anbieter beschreibt.
2.  Erstellen Sie eine Instanz der [**\_ \_ EventProviderRegistration-Klasse,**](--eventproviderregistration.md) die den Funktionssatz des Anbieters beschreibt.

    Die [**\_ \_ EventProviderRegistration-Klasse**](--eventproviderregistration.md) erbt viele Eigenschaften von der übergeordneten [**\_ \_ ObjectProviderRegistration-Klasse.**](--objectproviderregistration.md) Die lokalen Eigenschaften der **\_ \_ EventProviderRegistration-Klasse** sind der Objektpfad zum Anbieter und eine Liste von Abfragen, die die vom Anbieter unterstützten Ereignisse beschreiben. Weitere Informationen finden Sie unter [Abfragen von WMI.](querying-wmi.md)

3.  Laden Sie Ihre Implementierung der [**\_ \_ Klassen Win32Provider**](--win32provider.md) [**\_ \_ und EventProviderRegistration**](--eventproviderregistration.md) in das WMI-Repository.

    WMI verwendet Ihre Klassendefinition, um Ihren Ereignisanbieter zu registrieren und darauf zu zugreifen. Weitere Informationen finden Sie unter [Registrieren eines Anbieters.](registering-a-provider.md)

Im folgenden Codebeispiel wird eine Implementierung einer [**\_ \_ Win32Provider-Klasse**](--win32provider.md) und einer [**\_ \_ EventProviderRegistration-Klasse**](--eventproviderregistration.md) beschrieben.

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

Die erste Abfrage gibt an, dass der Anbieter alle Ereignisbenachrichtigungen für die extrinsische Ereignisklasse FaxEvent generiert. Da der ISA-Operator verwendet wird, impliziert die zweite Abfrage, dass der Anbieter Benachrichtigungen für alle Instanzerstellungsereignisse für die [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) und alle ihre Unterklassen generiert.

Wenn ein Anbieter registriert wird, um ein systeminternes Ereignis zur Verfügung zu stellen, muss das Ereignis auf alle Instanzen einer Klasse angewendet werden. Anders ausgedrückt: Eine Abfrage kann nicht geschrieben werden, um Instanzerstellungsereignisse nur für einige der Laufwerke zu liefern, die zur [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) gehören.

 

 
