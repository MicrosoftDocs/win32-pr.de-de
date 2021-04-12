---
description: Enumerationen verwenden tendenziell eine beträchtliche Menge an Systemressourcen.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Verbessern der enumerationsleistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217123"
---
# <a name="improving-enumeration-performance"></a>Verbessern der enumerationsleistung

Enumerationen verwenden tendenziell eine beträchtliche Menge an Systemressourcen. Daher sollten Sie versuchen, den WMI-enumerationsprozess zu optimieren, wenn Sie in einer großen Gruppe Enumerationen ausführen möchten. Skripts können auch eine Abfrage verwenden, um Leistungseinbußen in "for each.... Next"-Vorgängen mit einer großen Menge zu vermeiden. Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).

Im folgenden Verfahren wird beschrieben, wie die enumerationsleistung verbessert wird.

**So verbessern Sie die Enumeration**

1.  Legen Sie den *lFlags* -Parameter fest, um die semisynchrone Rückgabe der Daten mit einem Enumerator zuzulassen, der jedes Element bei der Übermittlung aus WMI verwirft. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

    Im folgenden C++-Codebeispiel wird gezeigt, wie das **WBEM- \_ Flag " \_ \_ immediate Return** " und das **WBEM-Flag " \_ \_ Forward \_ only** " verwendet wird.

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    Verwenden Sie in VBScript oder Visual Basic die skriptingflags **wbemFlagReturnImmediately** und **wbemFlagForwardOnly** aus [wbemflagenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum). Der kombinierte Wert dieser Flags ist Decimal 48.

    Die Skripting-und Parameterflags bewirken folgendes Verhalten:

    -   Das **WBEM- \_ Flag \_ gibt das \_ unmittelbare** oder **wbemFlagReturnImmediately** -Flag zurück, das semisynchrone Verhalten anfordert. Der-Befehl zum Erstellen des Enumerators wird sofort zurückgegeben. Sie können dann beginnen, den Objekt Satz zu durchlaufen, den Sie erhalten.
    -   Das Flag " **WBEM- \_ Flag \_ weiterleiten \_** " oder das Flag " **wbemFlagForwardOnly** " fordert einen Enumerator an, den Sie nicht zurückspulen können. Das heißt, dass WMI ein Objekt freigeben kann, nachdem Sie das Objekt angezeigt haben.

    In Situationen, in denen die Enumeration groß ist und die Anwendung sehr schnell ist, ermöglicht die Verwendung von vorwärts-Enumeratoren mit semisynchroner Verarbeitung, dass WMI viel weniger Objekte speichert, wodurch die Reaktionszeit und die Arbeitsspeicher Leistung erheblich erhöht werden.

    Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie mithilfe der kombinierten **wbemFlagReturnImmediately** -und **wbemFlagForwardOnly** -Flags eine Auflistung von Ereignissen aus einem Ereignisprotokoll abrufen.

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  Vermeiden Sie nach Möglichkeit die Verwendung von "" in "C++" oder " [**slibemservices. InstancesOf**](swbemservices-instancesof.md)" mit der Verwendung von "" [**. verwenden Sie**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) stattdessen " **ExecQuery**".

    Von der **ExecQuery** -Methode wird WMI mithilfe von Datenbanktechnologien abgefragt, während mit "" von "" "" "" "," "," [**"und"**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) [**slibemservices. InstancesOf**](swbemservices-instancesof.md) " Insbesondere kann **ExecQuery** bestimmte Teilmengen von Daten anfordern, die von den enumeringmethoden nicht möglich sind.

    Da einige Anbieter keine Abfragefunktionen haben, bietet WMI eine Funktion für den Post-Filter, die es WMI ermöglicht, Instanzen zu verwerfen, die die Spezifikationen einer Abfrage nicht erfüllen. Ob ein bestimmter Anbieter dieses Feature nutzt, ist der Autor des Anbieters.

3.  Experimentieren Sie mit verschiedenen Abfragen, um zu bestimmen, was Ihnen die beste Leistung bietet.

    WMI verarbeitet z. b. nur selten Abfragen mit **Where** -Klauseln der Form Eigenschaft PROP1 < "x". Im Gegensatz dazu verarbeitet WMI in der Regel effizient Abfragen der Form KeyProp1 = "x".

Weitere Informationen finden Sie unter Auflisten von [WMI](enumerating-wmi.md).

 

 



