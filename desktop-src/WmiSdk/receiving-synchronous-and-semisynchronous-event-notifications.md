---
description: Verwenden Sie SWbemServices.Execquery, um alle vorhandenen Ereignisse anzufordern.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Empfangen synchroner und semisynchroner Ereignis Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347681"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>Empfangen synchroner und semisynchroner Ereignis Benachrichtigungen

Verwenden Sie [**SWbemServices.Execquery**](swbemservices-execquery.md) , um alle vorhandenen Ereignisse anzufordern.

Im folgenden Codebeispiel wird gezeigt, wie die Ereignisse in einem Protokoll abgefragt werden.

`Select * from Win32_NTLogEvent`

Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md), [empfangen von Ereignis Benachrichtigungen](receiving-event-notifications.md)und [WQL (SQL für WMI)](wql-sql-for-wmi.md).

Der Standard Aufruf von [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) verwendet die semisynchrone Kommunikation. Der *IFlags* -Parameter verfügt über die standardmäßig festgelegten **wbemFlagForwardOnly** -und **wbemFlagReturnImmediately** -Flags. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Im folgenden Verfahren wird beschrieben, wie die semisynchrone Ereignis Benachrichtigung mithilfe von VBScript empfangen wird.

**So empfangen Sie eine semisynchrone Ereignis Benachrichtigung in VBScript**

1.  Erstellen Sie eine Abfrage für den Ereignistyp, den Sie empfangen möchten. Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

2.  Wenn Sie einen Ereignistyp des Ereignisses (z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md)) anfordern, geben Sie in der Abfrage einen Typ der Ziel Instanz an, z. b. [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).

3.  Geben Sie ggf. eine Instanz an, z. b. den Namen eines Namespace, wenn Sie zukünftige [**\_ \_ namespacemodificationevent**](--namespacemodificationevent.md) -Instanzen für einen bestimmten Namespace anfordern.

4.  Geben Sie ein Abruf Intervall für Windows-Verwaltungsinstrumentation (WMI) in einer Abfrage an, z. b. "innerhalb 10" –, um alle 10 Sekunden eine Abfrage durchzusetzen. Weitere Informationen finden Sie unter [within-Klausel](within-clause.md).

5.  Ruft [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) mithilfe der Abfrage auf.

6.  Durchlaufen Sie die Auflistung, die Sie erhalten.

Im folgenden Beispiel wird gezeigt, wie Sie das Einfügen und Entfernen von Datenträgern von einem Diskettenlaufwerk auf einem lokalen Computer überwachen. Das Skript fordert \_ [**\_ \_ instancemodificationevent**](--instancemodificationevent.md) -Instanzen für die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Instanz des Disketten Laufwerks an und fragt alle 10 Sekunden nach neuen Instanzen ab. Dieses Skript ist ein Beispiel für einen temporären Ereignisconsumer und wird weiter ausgeführt, bis er im Task-Manager angehalten oder das System neu gestartet wird. Weitere Informationen finden Sie unter [empfangen von Ereignissen für die Dauer Ihrer Anwendung](receiving-events-for-the-duration-of-your-application.md).


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



Im folgenden Verfahren wird beschrieben, wie Sie mit C++ semisynchrone Ereignis Benachrichtigungen empfangen.

**So empfangen Sie eine semisynchrone Ereignis Benachrichtigung in C++**

1.  Richten Sie die Anwendung mit Aufrufen der Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ein.

    Da WMI auf com basiert, ist der Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ein erforderlicher Schritt für eine WMI-Anwendung. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).

2.  Bestimmen Sie die Art der Ereignisse, die Sie empfangen möchten.

    WMI unterstützt systeminterne und extrinsische Ereignisse. Ein System internes Ereignis ist ein von WMI vordefiniertes Ereignis. Ein System externe-Ereignis ist ein Ereignis, das von einem Drittanbieter definiert wird. Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

3.  Registrieren Sie sich, um eine bestimmte Ereignisklasse mit einem Aufruf der [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) -Methode zu empfangen.

    Stellen Sie jede Abfrage sehr spezifisch dar. Das Ziel der Registrierung besteht darin, sich zu registrieren, um nur die erforderlichen Benachrichtigungen zu empfangen. Benachrichtigungen, bei denen die Verarbeitungs-und Übermittlungs Zeit nicht erforderlich ist.

    Sie können einen Ereignisconsumer so entwerfen, dass er mehrere Ereignisse empfängt. Beispielsweise kann ein Consumer eine Benachrichtigung über instanzänderungsereignisse für eine bestimmte Klasse von Geräte-und Sicherheits Verletzungs Ereignissen anfordern. In diesem Fall unterscheiden sich die Tasks, die ein Consumer beim Empfang eines instanzänderungsereignisses ausführt, für die beiden Ereignisse. Folglich sollte der Consumer einen Aufruf von [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) durchführen, um sich für instanzänderungsereignisse zu registrieren, und einen weiteren Aufruf von **ExecNotificationQuery** , um sich für Sicherheits Verletzungs Ereignisse zu registrieren.

    Legen Sie im Aufruf von [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)den *lFlags* -Parameter auf das **WBEM- \_ Flag \_ \_ sofort zurück** , und verwenden Sie das **WBEM- \_ Flag \_ \_ nur vorwärts**. Das **WBEM- \_ Flag \_ gibt \_ sofort** die semisynchrone Verarbeitung von Flags zurück, und das Flag für das **WBEM-Flag " \_ \_ Vorwärts \_** " fordert einen vorwärts-Enumerator an. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md). Die **ExecNotificationQuery** -Funktion gibt einen Zeiger auf eine [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Schnittstelle zurück.

4.  Abrufen registrierter Ereignis Benachrichtigungen durch wiederholte Aufrufe der [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) -Methode.
5.  Wenn Sie fertig sind, geben Sie den Enumerator frei, der auf das [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Objekt zeigt.

    Sie können den [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger freigeben, der der Registrierung zugeordnet ist. Das Freigeben des **IWbemServices** -Zeigers bewirkt, dass WMI keine Ereignisse mehr an alle zugeordneten temporären Consumer übergibt.

 

 
