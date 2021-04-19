---
description: Temporäre und permanente Consumer verfügen über verschiedene Methoden zum Sichern der Ereignis Übermittlung.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Sicheres empfangen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27d156213553ee17a346d780cbea0ff82beca83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362337"
---
# <a name="receiving-events-securely"></a>Sicheres empfangen von Ereignissen

Temporäre und permanente Consumer verfügen über verschiedene Methoden zum Sichern der Ereignis Übermittlung.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Sichern von temporären Consumern](#securing-temporary-consumers)
-   [Sichern dauerhafter Consumer](#securing-permanent-consumers)
-   [Sichern des permanenten Abonnements](#securing-the-permanent-subscription)
-   [Festlegen einer Administrator-Only SD](#setting-an-administrator-only-sd)
-   [Identität der Identität des Ereignis Anbieters annehmen](#impersonating-the-event-provider-identity)
-   [SIDs und permanente Abonnements](#sids-and-permanent-subscriptions)
-   [Erstellen dauerhafter Abonnements mithilfe von Domänen Konten](#creating-permanent-subscriptions-using-domain-accounts)
-   [Zugehörige Themen](#related-topics)

## <a name="securing-temporary-consumers"></a>Sichern von temporären Consumern

[*Temporäre*](gloss-t.md) Consumer werden so lange ausgeführt, bis das System neu gestartet oder WMI beendet wird, aber nicht gestartet werden kann, wenn ein bestimmtes Ereignis ausgelöst wird. Beispielsweise erstellt ein Aufruf von [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md) einen temporären Consumer.

Mit den Aufrufen [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) oder [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) werden temporäre Ereignisconsumer erstellt. Temporäre Consumer können nicht steuern, wer Ereignisse für die von Ihnen erstellte Ereignis [*Senke*](gloss-s.md) bereitstellt.

Aufrufe der [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) -Methoden können synchron, [*halb synchron*](gloss-s.md)oder asynchron erfolgen. Beispielsweise ist [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) eine synchrone Methode, die in Abhängigkeit davon, wie der *IFlags* -Parameter festgelegt ist, SemiSynchron aufgerufen werden kann. [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md) ist ein asynchroner Aufruf.

Beachten Sie, dass der Rückruf der Senke für die asynchronen Versionen dieser Aufrufe möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Aufruf des Skripts zurückgegeben wird. Daher wird empfohlen, semisynchrone anstelle von asynchronen Aufrufen zu verwenden. Wenn Sie asynchrone Kommunikation benötigen, finden Sie weitere Informationen unter [Aufrufen einer Methode](calling-a-method.md) und [Festlegen der Sicherheit für einen asynchronen Aufruf](setting-security-on-an-asynchronous-call.md).

Skript Abonnenten können die Zugriffsrechte eines Ereignis Anbieters nicht überprüfen, um Ereignisse für die Senke bereitzustellen, die vom Skript erstellt wurde. Daher wird empfohlen, dass Aufrufe von [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) die semisynchrone Form des Aufrufs verwenden und bestimmte Sicherheitseinstellungen verwenden. Weitere Informationen finden Sie unter [Erstellen eines semisynchronen Aufrufes mit VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="securing-permanent-consumers"></a>Sichern dauerhafter Consumer

Ein [*dauerhafter*](gloss-p.md) Consumer verfügt über ein dauerhaftes Abonnement für Ereignisse eines Ereignis Anbieters, die nach dem Neustart des Betriebssystems persistent gespeichert werden. Ein Ereignis Anbieter, der permanente Consumer unterstützt, ist ein [*Ereignisconsumeranbieter*](gloss-e.md). Wenn der Ereignis Anbieter nicht ausgeführt wird, wenn ein Ereignis auftritt, startet WMI den Anbieter, wenn er Ereignisse übermitteln muss. WMI identifiziert den Consumeranbieter, an den die Ereignisse übermittelt werden sollen, basierend auf der [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) -Instanz, die die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz des consumeranbieters einer vom Consumeranbieter definierten [*logischen Consumerklasse*](gloss-l.md) zuordnet. Weitere Informationen zur Rolle von consumeranbietern finden Sie unter [Schreiben eines Ereignisconsumeranbieters](writing-an-event-consumer-provider.md).

Permanente Consumer können steuern, wer Sie an Ereignisse sendet, und Ereignis Anbieter können steuern, wer auf Ihre Ereignisse zugreift.

Client Skripts und Anwendungen erstellen Instanzen der logischen Consumerklasse als Teil eines Abonnements. Die Klasse logischer Consumer definiert, welche Informationen das Ereignis enthält, wie der Client mit dem Ereignis Vorgehen kann und wie das Ereignis übermittelt wird.

Die WMI- [standardconsumerklassen](standard-consumer-classes.md) stellen Beispiele für die Rolle logischer Consumerklassen bereit. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

## <a name="securing-the-permanent-subscription"></a>Sichern des permanenten Abonnements

Permanente Abonnements haben größere Möglichkeiten, Sicherheitsprobleme in WMI zu verursachen und müssen daher die folgenden Sicherheitsanforderungen erfüllen:

-   Die logische consumerinstanz, die [**\_ \_ EventFilter**](--eventfilter.md)-Instanz und die [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Instanz müssen in der Eigenschaft " **kreatorsid** " dieselbe individuelle Sicherheits-ID (SID) aufweisen. Weitere Informationen finden Sie unter [beibehalten der gleichen SID in allen Instanzen eines permanenten Abonnements](#sids-and-permanent-subscriptions).
-   Das Konto, mit dem das Abonnement erstellt wird, muss entweder ein Domänen Konto mit lokalen Administratorrechten oder das Konto der lokalen Administratoren Gruppe sein. Die Verwendung der Administratoren Gruppen-SID ermöglicht, dass das Abonnement weiterhin auf dem lokalen Computer funktioniert, auch wenn es vom Netzwerk getrennt ist. Die Verwendung eines Domänen Kontos ermöglicht die genaue Identifizierung des Benutzers.

    Wenn der Computer jedoch nicht verbunden ist und das erstellende Konto ein Domänen Konto ist, schlägt der Consumer fehl, da die Identität des Kontos von WMI nicht überprüft werden kann. Verwenden Sie zum Vermeiden eines Abonnement Fehlers, wenn der Computer nicht mit dem Netzwerk getrennt ist, die SID der Administratoren Gruppe für ein Abonnement. In diesem Fall sollten Sie sicherstellen, dass das LocalSystem-Konto auf Gruppen Mitgliedschafts Daten in der Domäne zugreifen kann. Einige Ereignisconsumeranbieter haben besonders hohe Sicherheitsanforderungen, da ein nicht autorisiertes Abonnement große Schäden verursachen kann. Beispiele hierfür sind die [**Standardconsumer activescripteventconsumer**](activescripteventconsumer.md) und [**commandlineeventconsumer**](commandlineeventconsumer.md).

-   Sie können das permanente Abonnement so konfigurieren, dass nur Ereignisse von bestimmten Ereignis Anbieter Identitäten akzeptiert werden. Legen Sie die Sicherheits Beschreibung in der **eventaccess** -Eigenschaft der [**\_ \_ EventFilter**](--eventfilter.md) -Instanz auf die Ereignis Anbieter Identitäten fest. WMI vergleicht die Identität des Ereignis Anbieters mit der Sicherheits Beschreibung, um zu bestimmen, ob der Anbieter über **WBEM \_ rechten \_ Veröffentlichungs** Zugriff verfügt. Weitere Informationen finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).

    Wenn der Filter den Zugriff auf die Identität des Ereignis Anbieters zulässt, vertraut Sie auch dem-Ereignis. Dadurch kann der Consumer, der das Ereignis empfangen hat, ein delegiertes Ereignis aufwecken.

    **Hinweis**  Der Standardwert für die Sicherheits Beschreibung in **eventaccess** ist **null**, was den Zugriff auf alle ermöglicht. Es wird empfohlen, den Zugriff auf die Abonnement Instanz von [**\_ \_ EventFilter**](--eventfilter.md) einzuschränken, um die Sicherheit zu verbessern.

## <a name="setting-an-administrator-only-sd"></a>Festlegen einer Administrator-Only SD

Im folgenden C++-Codebeispiel wird eine Sicherheits Beschreibung für den Administrator auf der [**\_ \_ EventFilter**](--eventfilter.md) -Instanz erstellt. In diesem Beispiel wird die Sicherheits Beschreibung mithilfe von SDDL ( [Security Deskriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ) erstellt. Weitere Informationen zum **\_ richtigen \_ Abonnieren von WBEM** finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



Für das vorherige Codebeispiel sind die folgenden Reference-und \# include-Anweisungen erforderlich.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Identität der Identität des Ereignis Anbieters annehmen

Ein dauerhafter Consumer muss möglicherweise die Identität des Ereignis Anbieters annehmen, um das Ereignis zu verarbeiten. Permanente Consumer können nur dann die Identität des Ereignis Anbieters annehmen, wenn die folgenden Bedingungen erfüllt sind:

-   Für die Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) ist die **wart SecurityContext** -Eigenschaft auf **true** festgelegt.
-   Ein Ereignis wird im gleichen Sicherheitskontext bereitgestellt, in dem sich der Anbieter beim Generieren des Ereignisses befand. Nur ein Consumer, der als DLL, ein Prozess interner Consumer, implementiert ist, kann Ereignisse im Sicherheitskontext des Anbieters empfangen. Weitere Informationen zur Sicherheit von in-Process-Anbietern und-Consumern finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).
-   Der Ereignis Anbieter wird in einem Prozess ausgeführt, der Identitätswechsel zulässt.

Das Konto, unter dem der consumerprozess ausgeführt wird, muss über **vollen \_ Schreib** Zugriff auf das WMI-Repository (auch als CIM-Repository bezeichnet) verfügen. Im Abonnement müssen die Instanzen [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md), [**\_ \_ eventconsumer**](--eventconsumer.md)und [**\_ \_ EventFilter**](--eventfilter.md) in der Eigenschaft " **kreatorsid** " denselben Wert für die individuelle Sicherheits-ID (SID) aufweisen. WMI speichert die sid für jede Instanz in der " **kreatorsid** ".

## <a name="sids-and-permanent-subscriptions"></a>SIDs und permanente Abonnements

Ein dauerhaftes Abonnement funktioniert nicht, wenn die Bindung, der Consumer und der Filter nicht durch denselben Benutzer erstellt werden, was bedeutet, dass [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md), [**\_ \_ eventconsumer**](--eventconsumer.md)und [**\_ \_ EventFilter**](--eventfilter.md) denselben Wert für die individuelle Sicherheits-ID (SID) in der Eigenschaft " **kreatorsid** " aufweisen müssen. Windows-Verwaltungsinstrumentation (WMI) speichert diesen Wert.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Erstellen dauerhafter Abonnements mithilfe von Domänen Konten

Bei der Verwendung von Domänen Konten zum Erstellen dauerhafter Abonnements müssen mehrere Probleme berücksichtigt werden. Alle permanenten Abonnements sollten immer noch funktionieren, wenn kein Benutzer angemeldet ist. Dies bedeutet, dass Sie unter dem integrierten LocalSystem-Konto funktionieren.

Wenn ein Domänen Benutzer der Ersteller eines permanenten Abonnements für sicherheitssensible Consumer ist ([**activescripteventconsumer**](activescripteventconsumer.md), [**commandlineeventconsumer**](commandlineeventconsumer.md)), überprüft WMI, ob die Eigenschaft " **kreatorsid** " der [**\_ \_ EventFilter**](--eventfilter.md) -Klasse, die [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Klasse und die consumerinstanzen zu einem Benutzer gehören, der Mitglied der lokalen Administrator Gruppe ist.

Im folgenden Codebeispiel wird gezeigt, wie Sie die Eigenschaft " **kreatorsid** " angeben können.

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

Fügen Sie für Domänen übergreifende Situationen der "Windows-Autorisierungs Zugriffs Gruppe" authentifizierte Benutzer hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> </dl>

 

 
