---
description: WMI enthält eine Reihe von Klassen für die Problembehandlung von Clientanwendungen, die WMI-Anbieter verwenden.
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: Problembehandlung bei WMI-Clientanwendungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7fb9eb8c438faab8915691ee2c9c8a4c77d247c6802f8f114683a79d2833bd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050028"
---
# <a name="troubleshooting-wmi-client-applications"></a>Problembehandlung bei WMI-Clientanwendungen

WMI enthält eine Reihe von Klassen für die [Problembehandlung von](wmi-troubleshooting-classes.md) Clientanwendungen, die WMI-Anbieter verwenden. Die Ereignisklassen zur Problembehandlung sind an WMI-Ereignisklassen gekoppelt, sodass Sie die Anwendungsausführung mithilfe eines Protokolls erfasster Problembehandlungsereignisse nachverfolgen können.

Die folgende Liste enthält Beispiele für Ereignisklassen zur Problembehandlung:

-   [**Msft \_ WmiProvider \_ ExecMethodAsyncEvent \_ Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Wird ausgelöst, bevor WMI [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) für den Anbieter aufruft.

-   [**Msft \_ WmiProvider \_ ExecMethodAsyncEvent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Wird ausgelöst, nachdem WMI [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) für den Anbieter aufgerufen hat.

Das folgende Verfahren veranschaulicht die Problembehandlung bei der Anwendungsausführung.

**So richten Sie die WMI-Problembehandlung ein**

1.  Erstellen und kompilieren Sie eine MOF-Datei, um den WMI-Protokollierungsereignis-Consumer zu verwenden.
2.  Führen Sie Ihre Clientanwendung aus.
3.  Zeigen Sie die Protokolldatei zur Problembehandlung für alle Anbietervorgangs- und Fehlerereignisse an, und analysieren Sie das Protokoll, um die aufgetretenen Clientprobleme zu diagnostizieren.

Ein weiterer Ansatz zur Problembehandlung besteht darin, die Liste der Anbieter anzuzeigen, die sich derzeit im Computercache befinden, indem [**\_ MSFT-Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) im **\\ Cimv2-Stammnamespace** aufgeführt werden. Es gibt Methoden in dieser Klasse, mit denen Sie Anbieter zu Debug- oder Setupzwecken laden und entladen können.

Im folgenden Codebeispiel wird der WMI-Protokollierungsereignis-Consumer verwendet, um alle Ereignisse der übergeordneten Ereignisklasse zu erfassen und somit alle Anbietervorgangsereignisse zu erfassen.

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

Wenn Fehlermeldungen auf einen Fehler beim Laden des Anbieters hinweisen, verwenden Sie [**MSFT \_ WmiProvider \_ LoadOperationFailureEvent,**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) um zu ermitteln, welcher Anbieter den Fehler verursacht hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[WMI-Problembehandlungsklassen](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
