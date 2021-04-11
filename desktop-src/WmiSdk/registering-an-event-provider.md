---
description: Zum Erstellen eines WMI-Ereignis Anbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ eventproviderregistration registrieren.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registrieren eines Ereignis Anbieters
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131917"
---
# <a name="registering-an-event-provider"></a>Registrieren eines Ereignis Anbieters

Zum Erstellen eines WMI- [*Ereignis Anbieters*](gloss-e.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ eventproviderregistration**](--eventproviderregistration.md)registrieren. Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.

Im folgenden Verfahren wird beschrieben, wie ein Ereignis Anbieter registriert wird.

**So registrieren Sie einen Ereignis Anbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.
2.  Erstellen Sie eine Instanz der [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.

    Die [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse erbt viele Eigenschaften von der übergeordneten [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) -Klasse. Die lokalen Eigenschaften der **\_ \_ eventproviderregistration** -Klasse sind der Objekt Pfad zum Anbieter und eine Liste von Abfragen, die die vom Anbieter unterstützten Ereignisse beschreiben. Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).

3.  Laden Sie die Implementierung der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse und der [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse in das WMI-Repository.

    WMI verwendet Ihre Klassendefinition, um den Ereignis Anbieter zu registrieren und darauf zuzugreifen. Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).

Im folgenden Codebeispiel wird eine Implementierung einer [**\_ \_ Win32Provider**](--win32provider.md) -Klasse und einer [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse beschrieben.

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

Die erste Abfrage gibt an, dass der Anbieter alle Ereignis Benachrichtigungen für das faxereignis der System externe-Ereignisklasse generiert. Da der ISA-Operator verwendet wird, impliziert die zweite Abfrage, dass der Anbieter Benachrichtigungen für alle instanzerstellungsereignisse für die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse und alle seine Unterklassen generiert.

Wenn ein Anbieter registriert wird, um ein System internes Ereignis bereitzustellen, muss das Ereignis auf alle Instanzen einer Klasse angewendet werden. Anders ausgedrückt: Es kann keine Abfrage geschrieben werden, um instanzerstellungsereignisse nur für einige Laufwerke bereitzustellen, die zur [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse gehören.

 

 
