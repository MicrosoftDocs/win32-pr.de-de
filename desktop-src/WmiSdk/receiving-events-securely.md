---
description: Temporäre und permanente Consumers verfügen über unterschiedliche Methoden zum Sichern der Ereignisbereitstellung.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Sicheres Empfangen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64db5b0289abd9a43caee6ddb3b68da94a9560b0ea8f591d95ee472cf900b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316527"
---
# <a name="receiving-events-securely"></a>Sicheres Empfangen von Ereignissen

Temporäre und permanente Consumers verfügen über unterschiedliche Methoden zum Sichern der Ereignisbereitstellung.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Sichern temporärer Verbraucher](#securing-temporary-consumers)
-   [Sichern permanenter Verbraucher](#securing-permanent-consumers)
-   [Sichern des permanenten Abonnements](#securing-the-permanent-subscription)
-   [Festlegen einer Administrator-Only SD](#setting-an-administrator-only-sd)
-   [Identitätswechsel der Ereignisanbieteridentität](#impersonating-the-event-provider-identity)
-   [SIDs und permanente Abonnements](#sids-and-permanent-subscriptions)
-   [Erstellen von permanenten Abonnements mit Domänenkonten](#creating-permanent-subscriptions-using-domain-accounts)
-   [Zugehörige Themen](#related-topics)

## <a name="securing-temporary-consumers"></a>Sichern temporärer Verbraucher

Ein [*temporärer Consumers*](gloss-t.md) wird ausgeführt, bis das System neu gestartet oder WMI beendet, aber nicht gestartet werden kann, wenn ein bestimmtes Ereignis ausgelöst wird. Beispielsweise wird durch einen Aufruf von [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) ein temporärer Consumer erstellt.

Die [**AufrufeSWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) oder [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) erstellen temporäre Ereignisverbraucher. Temporäre Benutzer können nicht steuern, wer Ereignisse für die von ihnen [*erstellten*](gloss-s.md) Ereignissenke zur Verfügung stellt.

Aufrufe [**von ExecNotificationQuery-Methoden**](swbemservices-execnotificationquery.md) können synchron, [*halbsynchron oder*](gloss-s.md)asynchron erfolgen. Beispielsweise ist [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) eine synchrone Methode, die halbsynchron aufgerufen werden kann, je nachdem, wie der *iflags-Parameter* festgelegt ist. [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) ist ein asynchroner Aufruf.

Beachten Sie, dass der Rückruf an die Senke für die asynchronen Versionen dieser Aufrufe möglicherweise nicht auf der gleichen Authentifizierungsebene wie der Aufruf des Skripts zurückgegeben wird. Daher wird empfohlen, anstelle von asynchronen Aufrufen semisynchrone Aufrufe zu verwenden. Wenn Sie asynchrone Kommunikation benötigen, finden Sie weitere Informationen unter [Aufrufen einer Methode](calling-a-method.md) und Festlegen der Sicherheit für einen [asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

Skriptabonnenten können die Zugriffsrechte eines Ereignisanbieters nicht überprüfen, um Ereignisse für die vom Skript erstellte Senke zur Verfügung zu stellen. Daher wird empfohlen, dass Aufrufe von [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) die semisynchrone Form des Aufrufs verwenden und bestimmte Sicherheitseinstellungen verwenden. Weitere Informationen finden Sie unter [Erstellen eines semisynchronen Aufrufs mit VBScript.](making-a-semisynchronous-call-with-vbscript.md)

## <a name="securing-permanent-consumers"></a>Sichern permanenter Verbraucher

Ein [*permanenter Consumers*](gloss-p.md) verfügt über ein dauerhaftes Abonnement für Ereignisse eines Ereignisanbieters, die nach dem Neustart des Betriebssystems beibehalten werden. Ein Ereignisanbieter, der permanente Consumer unterstützt, ist ein [*Ereignisverbraucheranbieter.*](gloss-e.md) Wenn der Ereignisanbieter nicht ausgeführt wird, wenn ein Ereignis auftritt, startet WMI den Anbieter, wenn Ereignisse übermittelt werden müssen. WMI identifiziert basierend auf der [**\_ \_ EventConsumerProviderRegistration-Instanz,**](--eventconsumerproviderregistration.md) die die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) des Consumeranbieters [](gloss-l.md) einer vom Consumeranbieter definierten logischen Consumerklasse zuleiten soll, an welchen Consumeranbieter die Ereignisse übermittelt werden sollen. Weitere Informationen zur Rolle von Consumeranbietern finden Sie unter [Schreiben eines Ereignisverbraucheranbieters.](writing-an-event-consumer-provider.md)

Permanente Benutzer können steuern, wer ihnen Ereignisse sendet, und Ereignisanbieter können steuern, wer auf ihre Ereignisse zutritt.

Clientskripts und Anwendungen erstellen Instanzen der logischen Consumerklasse als Teil eines Abonnements. Die logische Consumerklasse definiert, welche Informationen das Ereignis enthält, was der Client mit dem Ereignis tun kann und wie das Ereignis übermittelt wird.

Die [WMI-Standardverbraucherklassen](standard-consumer-classes.md) enthalten Beispiele für die Rolle logischer Consumerklassen. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="securing-the-permanent-subscription"></a>Sichern des permanenten Abonnements

Dauerhafte Abonnements haben ein größeres Potenzial, Sicherheitsprobleme in WMI zu verursachen, und es gelten daher die folgenden Sicherheitsanforderungen:

-   Die logische Consumerinstanz, [**\_ \_ EventFilter**](--eventfilter.md)und [**\_ \_ die FilterToConsumerBinding-Instanzen**](--filtertoconsumerbinding.md) müssen dieselbe individuelle Sicherheits-ID (SID) in der **CreatorSID-Eigenschaft** aufweisen. Weitere Informationen finden Sie unter [Behalten der gleichen SID in allen Instanzen eines permanenten Abonnements.](#sids-and-permanent-subscriptions)
-   Das Konto, mit dem das Abonnement erstellt wird, muss entweder ein Domänenkonto mit lokalen Administratorrechten oder das lokale Administratorgruppenkonto sein. Mithilfe der Gruppen-SID "Administratoren" kann das Abonnement auch dann weiterhin auf dem lokalen Computer funktionieren, wenn es vom Netzwerk getrennt ist. Die Verwendung eines Domänenkontos ermöglicht die genaue Identifizierung des Benutzers.

    Wenn der Computer jedoch nicht verbunden ist und das erstellende Konto ein Domänenkonto ist, schlägt der Consumer fehl, da WMI die Identität des Kontos nicht überprüfen kann. Um Abonnementfehler zu vermeiden, wenn der Computer vom Netzwerk getrennt ist, verwenden Sie die Gruppen-SID "Administratoren" für ein Abonnement. In diesem Fall sollten Sie sicherstellen, dass das LocalSystem-Konto auf Gruppenmitgliedschaftsdaten in der Domäne zugreifen kann. Einige Ereignisverbraucheranbieter haben besonders hohe Sicherheitsanforderungen, da ein nicht autorisiertes Abonnement großen Schaden an verursachen kann. Beispiele hierfür sind die Standardconsumer [**ActiveScriptEventConsumer**](activescripteventconsumer.md) und [**CommandLineEventConsumer.**](commandlineeventconsumer.md)

-   Sie können das permanente Abonnement so konfigurieren, dass nur Ereignisse von bestimmten Ereignisanbieteridentitäten akzeptiert werden. Legen Sie den Sicherheitsdeskriptor in der **EventAccess-Eigenschaft** der [**\_ \_ EventFilter-Instanz**](--eventfilter.md) auf die Ereignisanbieteridentitäten fest. WMI vergleicht die Identität des Ereignisanbieters mit dem Sicherheitsdeskriptor, um zu ermitteln, ob der Anbieter **über WBEM \_ RIGHT \_ PUBLISH-Zugriff** verfügt. Weitere Informationen finden Sie unter [WMI-Sicherheitskonst konstanten](wmi-security-constants.md).

    Wenn der Filter den Zugriff auf die Ereignisanbieteridentität zulässt, vertraut er auch dem Ereignis. Dadurch kann der Consumer, der das Ereignis empfangen hat, ein delegiertes Ereignis aus.

    **Hinweis:**  Die Standardeinstellung für den Sicherheitsdeskriptor in **EventAccess** ist **NULL,** wodurch der Zugriff für alle Benutzer möglich ist. Es wird empfohlen, den Zugriff in der [**\_ \_ Abonnementinstanz von EventFilter zu**](--eventfilter.md) beschränken, um die Ereignissicherheit zu verbessern.

## <a name="setting-an-administrator-only-sd"></a>Festlegen einer Administrator-Only SD

Im folgenden C++-Codebeispiel wird ein Nur-Administrator-Sicherheitsdeskriptor für die [**\_ \_ EventFilter-Instanz**](--eventfilter.md) erstellt. In diesem Beispiel wird der Sicherheitsdeskriptor [mithilfe der Sicherheitsbeschreibungsdefinitionssprache (Security Descriptor Definition Language,](/windows/desktop/SecAuthZ/security-descriptor-definition-language) SDDL) erstellt. Weitere Informationen zu **WBEM \_ RIGHT SUBSCRIBE \_ finden** Sie unter [WMI-Sicherheitskonst constants](wmi-security-constants.md).


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



Das vorherige Codebeispiel erfordert den folgenden Verweis und \# include-Anweisungen.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Identitätswechsel der Ereignisanbieteridentität

Ein permanenter Consumer muss möglicherweise die Identität des Ereignisanbieters für die Verarbeitung des Ereignisses imitieren. Permanente Benutzer können die Identität des Ereignisanbieters nur dann imitieren, wenn die folgenden Bedingungen erfüllt sind:

-   Für die Instanz von [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) ist die **MaintainSecurityContext-Eigenschaft** auf **True festgelegt.**
-   Ein Ereignis wird in demselben Sicherheitskontext übermittelt, in dem sich der Anbieter beim Generierten des Ereignisses befindet. Nur ein als DLL implementierter Consumer, ein In-Process-Consumer, kann Ereignisse im Sicherheitskontext des Anbieters empfangen. Weitere Informationen zur Sicherheit von In-Process-Anbietern und -Consumers finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)
-   Der Ereignisanbieter wird in einem Prozess ausgeführt, der Identitätswechsel zulässt.

Das Konto, unter dem der Consumerprozess ausgeführt wird, muss **über \_ VOLLSTÄNDIGEN SCHREIBzugriff** auf das WMI-Repository (auch als CIM-Repository bekannt) verfügen. Im Abonnement müssen die [**\_ \_ Instanzen FilterToConsumerBinding,**](--filtertoconsumerbinding.md) [**\_ \_ EventConsumer**](--eventconsumer.md)und [**\_ \_ EventFilter**](--eventfilter.md) in der **CreatorSID-Eigenschaft** denselben wert für die einzelne Sicherheits-ID (SID) aufweisen. WMI speichert die SID in der **CreatorSID** für jede Instanz.

## <a name="sids-and-permanent-subscriptions"></a>SIDs und permanente Abonnements

Ein dauerhaftes Abonnement funktioniert nicht, wenn die Bindung, der Consumer und der Filter nicht vom gleichen Benutzer erstellt werden. Dies bedeutet, dass [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) [**\_ \_ EventConsumer**](--eventconsumer.md)und [**\_ \_ EventFilter**](--eventfilter.md) den gleichen wert für die einzelne Sicherheits-ID (SID) in der **CreatorSID-Eigenschaft** aufweisen müssen. Windows Dieser Wert wird von der Verwaltungsinstrumentation (Management Instrumentation, WMI) gespeichert.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Erstellen von permanenten Abonnements mit Domänenkonten

Bei der Verwendung von Domänenkonten zum Erstellen dauerhafter Abonnements müssen mehrere Probleme berücksichtigt werden. Jedes permanente Abonnement sollte weiterhin funktionieren, wenn kein Benutzer angemeldet ist, was bedeutet, dass er unter dem integrierten LocalSystem-Konto funktioniert.

Wenn ein Domänenbenutzer der Ersteller eines permanenten Abonnements für sicherheitssensible Consumer ist ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), überprüft WMI, ob die **CreatorSID-Eigenschaft** der [**\_ \_ EventFilter-Klasse,**](--eventfilter.md) [**\_ \_ FilterToConsumerBinding-Klasse**](--filtertoconsumerbinding.md) und die Consumerinstanzen zu einem Benutzer gehören, der Mitglied der lokalen Administratorgruppe ist.

Das folgende Codebeispiel zeigt, wie Sie die **CreatorSID-Eigenschaft angeben** können.

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

Fügen Sie authentifizierte Benutzer in domänenübergreifenden Situationen der "Windows Authorization Access Group" hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> </dl>

 

 
