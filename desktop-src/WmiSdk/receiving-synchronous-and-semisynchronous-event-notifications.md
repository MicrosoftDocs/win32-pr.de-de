---
description: Verwenden Sie SWbemServices.ExecQuery, um alle vorhandenen Ereignisse anzufordern.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Empfangen von synchronen und semisynchronen Ereignisbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8657767150012124c3ccb0df8d95896f51b36ef47fa00998cf786df9beddf977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817259"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>Empfangen von synchronen und semisynchronen Ereignisbenachrichtigungen

Verwenden Sie [**SWbemServices.ExecQuery,**](swbemservices-execquery.md) um alle vorhandenen Ereignisse anzufordern.

Das folgende Codebeispiel zeigt, wie Die Ereignisse in einem Protokoll abgefragt werden.

`Select * from Win32_NTLogEvent`

Weitere Informationen finden Sie unter [Bestimmen des Typs des zu empfangenden Ereignisses,](determining-the-type-of-event-to-receive.md)Empfangen von [Ereignisbenachrichtigungen](receiving-event-notifications.md)und [WQL (SQL für WMI).](wql-sql-for-wmi.md)

Der Standardaufruf von [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) verwendet semisynchrone Kommunikation. Für *den iflags-Parameter* sind die Flags **wbemFlagForwardOnly** und **wbemFlagReturnImmediately** standardmäßig festgelegt. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von VBScript semisynchrone Ereignisbenachrichtigungen empfangen.

**So empfangen Sie semisynchrone Ereignisbenachrichtigungen in VBScript**

1.  Erstellen Sie eine Abfrage für den Ereignistyp, den Sie empfangen möchten. Weitere Informationen finden Sie unter [Bestimmen des Typs des zu empfangenden Ereignisses.](determining-the-type-of-event-to-receive.md)

2.  Wenn Sie einen Instanztyp von Ereignis wie [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)anfordern, geben Sie in der Abfrage einen Typ der Zielinstanz an, z. B. [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).

3.  Geben Sie bei Bedarf eine -Instanz an, z. B. den Namen eines Namespace, wenn Sie zukünftige [**\_ \_ NamespaceModificationEvent-Instanzen**](--namespacemodificationevent.md) für einen bestimmten Namespace anfordern.

4.  Geben Sie ein Abrufintervall für Windows Management Instrumentation (WMI) in einer Abfrage an, z.B. "WITHIN 10", um alle 10 Sekunden abzufragen. Weitere Informationen finden Sie unter [WITHIN-Klausel.](within-clause.md)

5.  Rufen Sie [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) mithilfe der Abfrage auf.

6.  Durchlaufen Sie die sammlung, die Sie erhalten.

Das folgende Beispiel zeigt, wie Sie das Einfügen und Entfernen von Datenträgern von einem Diskettenlaufwerk auf einem lokalen Computer überwachen. Das Skript fordert \_ [**\_ \_ InstanceModificationEvent-Instanzen**](--instancemodificationevent.md) für die [**Win32 \_ LogicalDisk-Instanz**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) des Diskettenlaufwerks an und fragt alle 10 Sekunden nach neuen Instanzen ab. Dieses Skript ist ein Beispiel für einen temporären Ereignisverbraucher und wird weiter ausgeführt, bis es in Task-Manager beendet oder das System neu gestartet wird. Weitere Informationen finden Sie unter [Empfangen von Ereignissen für die Dauer Ihrer Anwendung.](receiving-events-for-the-duration-of-your-application.md)


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



Im folgenden Verfahren wird beschrieben, wie Sie mit C++ semisynchrone Ereignisbenachrichtigungen empfangen.

**So empfangen Sie semisynchrone Ereignisbenachrichtigungen in C++**

1.  Richten Sie die Anwendung mit Aufrufen der Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ein.

    Da WMI AUF COM basiert, ist der Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ein erforderlicher Schritt für eine WMI-Anwendung. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts.](creating-a-wmi-application-or-script.md)

2.  Bestimmen Sie die Art der Ereignisse, die Sie empfangen möchten.

    WMI unterstützt systeminterne und extrinsische Ereignisse. Ein systeminternes Ereignis ist ein von WMI vordefiniertes Ereignis. Ein extrinsisches Ereignis ist ein Ereignis, das von einem Drittanbieter definiert wird. Weitere Informationen finden Sie unter [Bestimmen des Typs des zu empfangenden Ereignisses.](determining-the-type-of-event-to-receive.md)

3.  Registrieren Sie sich, um eine bestimmte Klasse von Ereignissen mit einem Aufruf der [**IWbemServices::ExecNotificationQuery-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) zu empfangen.

    Machen Sie jede Abfrage sehr spezifisch. Das Ziel der Registrierung ist die Registrierung, um nur die erforderlichen Benachrichtigungen zu erhalten. Benachrichtigungen, die keine Verarbeitungs- und Übermittlungszeit für Verschwendung erfordern.

    Sie können einen Ereignisverbraucher so entwerfen, dass er mehrere Ereignisse empfängt. Beispielsweise kann ein Consumer eine Benachrichtigung über Instanzänderungsereignisse für eine bestimmte Klasse von Geräte- und Sicherheitsverletzungsereignissen erfordern. In diesem Fall unterscheiden sich die Aufgaben, die ein Consumer beim Empfangen eines Instanzänderungsereignisses ausführt, für die beiden Ereignisse. Daher sollte der Consumer einen Aufruf von [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) durchführen, um sich für Instanzänderungsereignisse zu registrieren, und einen anderen Aufruf von **ExecNotificationQuery,** um sich für Sicherheitsverletzungsereignisse zu registrieren.

    Legen Sie im Aufruf von [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)den *lFlags-Parameter* auf **WBEM \_ FLAG RETURN \_ \_ IMMEDIATELY** und **WBEM \_ FLAG FORWARD \_ \_ ONLY** fest. Das **Flag WBEM \_ FLAG RETURN \_ \_ IMMEDIATELY** fordert eine semisynchrone Verarbeitung an, und das **Flag WBEM \_ FLAG FORWARD \_ \_ ONLY** fordert einen vorwärts gerichteten Enumerator an. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md) Die **ExecNotificationQuery-Funktion** gibt einen Zeiger auf eine [**IEnumWbemClassObject-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) zurück.

4.  Rufen Sie registrierte Ereignisbenachrichtigungen ab, indem Sie wiederholte Aufrufe an die [**IEnumWbemClassObject::Next-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) senden.
5.  Geben Sie abschließend den Enumerator frei, der auf das [**IEnumWbemClassObject-Objekt**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) verweist.

    Sie können den [**IWbemServices-Zeiger**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) freigeben, der der Registrierung zugeordnet ist. Das Freigeben des **IWbemServices-Zeigers** bewirkt, dass WMI die Übermittlung von Ereignissen an alle zugeordneten temporären Consumer beendet.

 

 
