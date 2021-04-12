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
# <a name="troubleshooting-wmi-client-applications"></a><span data-ttu-id="189c3-103">Problembehandlung bei WMI-Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="189c3-103">Troubleshooting WMI Client Applications</span></span>

<span data-ttu-id="189c3-104">WMI enthält eine Reihe von Klassen zur [Problem](wmi-troubleshooting-classes.md) Behandlung von Client Anwendungen, die WMI-Anbieter verwenden.</span><span class="sxs-lookup"><span data-stu-id="189c3-104">WMI contains a set of classes for [troubleshooting](wmi-troubleshooting-classes.md) client applications that use WMI providers.</span></span> <span data-ttu-id="189c3-105">Die Problem Behandlungs Ereignis Klassen sind an WMI-Ereignis Klassen gekoppelt, sodass Sie die Ausführung Ihrer Anwendung mithilfe eines Protokolls erfasster Problem Behandlungs Ereignisse verfolgen können.</span><span class="sxs-lookup"><span data-stu-id="189c3-105">The troubleshooting event classes are coupled to WMI event classes, such that you can track your application execution using a log of captured troubleshooting events.</span></span>

<span data-ttu-id="189c3-106">Die folgende Liste enthält Beispiele für Ereignis Klassen zur Problembehandlung:</span><span class="sxs-lookup"><span data-stu-id="189c3-106">The following list contains examples of troubleshooting event classes:</span></span>

-   [<span data-ttu-id="189c3-107">**MSFT \_ WMIProvider \_ execmethodasyncevent ( \_ Pre)**</span><span class="sxs-lookup"><span data-stu-id="189c3-107">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Pre**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    <span data-ttu-id="189c3-108">Wird ausgelöst, bevor WMI [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) für den Anbieter aufruft.</span><span class="sxs-lookup"><span data-stu-id="189c3-108">Raised before WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

-   [<span data-ttu-id="189c3-109">**MSFT \_ WMIProvider \_ execmethodasyncevent- \_ Beitrag**</span><span class="sxs-lookup"><span data-stu-id="189c3-109">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Post**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    <span data-ttu-id="189c3-110">Wird ausgelöst, nachdem WMI " [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) " für den Anbieter aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="189c3-110">Raised after WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

<span data-ttu-id="189c3-111">Das folgende Verfahren zeigt, wie Sie Probleme bei der Anwendungs Ausführung beheben.</span><span class="sxs-lookup"><span data-stu-id="189c3-111">The following procedure shows how to troubleshoot application execution.</span></span>

<span data-ttu-id="189c3-112">**So richten Sie die WMI-Problembehandlung ein**</span><span class="sxs-lookup"><span data-stu-id="189c3-112">**To set up WMI troubleshooting**</span></span>

1.  <span data-ttu-id="189c3-113">Erstellen und kompilieren Sie eine MOF-Datei, um den Consumer des WMI-Protokollierungs Ereignisses zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="189c3-113">Create and compile a MOF file to use the WMI logging event consumer.</span></span>
2.  <span data-ttu-id="189c3-114">Führen Sie Ihre Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="189c3-114">Run your client application.</span></span>
3.  <span data-ttu-id="189c3-115">Zeigen Sie die Protokolldatei zur Problembehandlung für alle Anbieter Vorgangs-und Fehlerereignisse an, und analysieren Sie das Protokoll, um die auftretenden Client Probleme zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="189c3-115">View the troubleshooting log file for all provider operation and failure events, and analyze the log to diagnose the client problems you are encountering.</span></span>

<span data-ttu-id="189c3-116">Ein weiterer Ansatz zur Problembehandlung besteht darin, die Liste der derzeit im Computer Cache gespeicherten Anbieter anzuzeigen, indem [**MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) im **root \\ CIMV2** -Namespace aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="189c3-116">Another troubleshooting approach is to view the list of providers currently in the computer cache, by enumerating [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="189c3-117">Es gibt Methoden in dieser Klasse, die es Ihnen ermöglichen, Anbieter zu debuggen oder zu Setup Zwecken zu laden und zu entladen.</span><span class="sxs-lookup"><span data-stu-id="189c3-117">There are methods in this class that enable you to load and unload providers for debugging or setup purposes.</span></span>

<span data-ttu-id="189c3-118">Im folgenden Codebeispiel wird der Consumer des WMI-Protokollierungs Ereignisses verwendet, um alle Ereignisse der übergeordneten Ereignisklasse aufzuzeichnen und so alle Ereignisse des Anbieter Vorgangs zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="189c3-118">The following code example uses the WMI logging event consumer to capture all events of the parent event class, thus capturing all provider operation events.</span></span>

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

<span data-ttu-id="189c3-119">Wenn Fehlermeldungen den Anbieter Ladefehler angeben, verwenden Sie den [**MSFT \_ WMIProvider \_ loadoperationfailureevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) , um zu ermitteln, welcher Anbieter den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="189c3-119">When error messages indicate provider load failure, use [**MSFT\_WmiProvider\_LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) to identify which provider caused the fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="189c3-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="189c3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="189c3-121">WMI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="189c3-121">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="189c3-122">WMI-Fehler Behebungs Klassen</span><span class="sxs-lookup"><span data-stu-id="189c3-122">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
