---
description: WMI enthält eine Reihe von Klassen zur Problembehandlung von Client Anwendungen, die WMI-Anbieter verwenden.
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: Problembehandlung bei WMI-Client Anwendungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a84646aa42cd0ccd649e3937f0eba257343e9a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217116"
---
# <a name="troubleshooting-wmi-client-applications"></a>Problembehandlung bei WMI-Client Anwendungen

WMI enthält eine Reihe von Klassen zur [Problem](wmi-troubleshooting-classes.md) Behandlung von Client Anwendungen, die WMI-Anbieter verwenden. Die Problem Behandlungs Ereignis Klassen sind an WMI-Ereignis Klassen gekoppelt, sodass Sie die Ausführung Ihrer Anwendung mithilfe eines Protokolls erfasster Problem Behandlungs Ereignisse verfolgen können.

Die folgende Liste enthält Beispiele für Ereignis Klassen zur Problembehandlung:

-   [**MSFT \_ WMIProvider \_ execmethodasyncevent ( \_ Pre)**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Wird ausgelöst, bevor WMI [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) für den Anbieter aufruft.

-   [**MSFT \_ WMIProvider \_ execmethodasyncevent- \_ Beitrag**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Wird ausgelöst, nachdem WMI " [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) " für den Anbieter aufgerufen hat.

Das folgende Verfahren zeigt, wie Sie Probleme bei der Anwendungs Ausführung beheben.

**So richten Sie die WMI-Problembehandlung ein**

1.  Erstellen und kompilieren Sie eine MOF-Datei, um den Consumer des WMI-Protokollierungs Ereignisses zu verwenden.
2.  Führen Sie Ihre Client Anwendung aus.
3.  Zeigen Sie die Protokolldatei zur Problembehandlung für alle Anbieter Vorgangs-und Fehlerereignisse an, und analysieren Sie das Protokoll, um die auftretenden Client Probleme zu diagnostizieren.

Ein weiterer Ansatz zur Problembehandlung besteht darin, die Liste der derzeit im Computer Cache gespeicherten Anbieter anzuzeigen, indem [**MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) im **root \\ CIMV2** -Namespace aufgelistet werden. Es gibt Methoden in dieser Klasse, die es Ihnen ermöglichen, Anbieter zu debuggen oder zu Setup Zwecken zu laden und zu entladen.

Im folgenden Codebeispiel wird der Consumer des WMI-Protokollierungs Ereignisses verwendet, um alle Ereignisse der übergeordneten Ereignisklasse aufzuzeichnen und so alle Ereignisse des Anbieter Vorgangs zu erfassen.

``` syntax
#pragma autorecover
#pragma namespace("\\\\.\\root\\subscription")

instance of __EventFilter as $Filter
{
  Name = "ProviderOperationEvents" ;
  EventNamespace = "root\\cimv2" ;
  Query = "SELECT * FROM MSFT_WmiProvider_OperationEvent" ;
  QueryLanguage = "WQL" ;
} ;

Instance of LogFileEventConsumer as $Consumer
{
  Name = "ProviderOperationEvents" ;
  FileName = "C:\\test.txt" ;
  Text = "Operation - %__TEXT%" ;
} ;

instance of __FilterToConsumerBinding
{
  Filter = $Filter ;
  Consumer = $Consumer ;
  MaintainSecurityContext = TRUE ;
} ;
```

Wenn Fehlermeldungen den Anbieter Ladefehler angeben, verwenden Sie den [**MSFT \_ WMIProvider \_ loadoperationfailureevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) , um zu ermitteln, welcher Anbieter den Fehler verursacht hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[WMI-Fehler Behebungs Klassen](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
