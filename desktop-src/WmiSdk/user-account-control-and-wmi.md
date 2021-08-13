---
description: Die Benutzerkontensteuerung (User Account Control, UAC) wirkt sich auf die WMI-Daten aus, die von einem Befehlszeilentool zurückgegeben werden, den Remotezugriff und die Ausführung von Skripts. Weitere Informationen zur Benutzerkontensteuerung finden Sie unter Erste Schritte Benutzerkontensteuerung.
ms.assetid: f6840aaa-834b-42c8-b641-01c570078fcb
ms.tgt_platform: multiple
title: Benutzerkontensteuerung und WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2da001117fa75ccef737647038d3e58b942f666ba40e1fd14ec98cb4ebdd44af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553316"
---
# <a name="user-account-control-and-wmi"></a>Benutzerkontensteuerung und WMI

Die Benutzerkontensteuerung (User Account Control, UAC) wirkt sich auf die WMI-Daten aus, die von einem Befehlszeilentool zurückgegeben werden, den Remotezugriff und die Ausführung von Skripts. Weitere Informationen zur Benutzerkontensteuerung finden Sie unter Erste Schritte [benutzerkontensteuerung.](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)

In den folgenden Abschnitten wird die UAC-Funktionalität beschrieben:

-   [Benutzerkontensteuerung](#user-account-control-and-wmi)
-   [Konto, das zum Ausführen von WMI-Command-Line Tools erforderlich ist](#account-needed-to-run-wmi-command-line-tools)
-   [Behandeln von Remoteverbindungen unter UAC](#handling-remote-connections-under-uac)
-   [UAC-Auswirkung auf WMI-Daten, die an Skripts oder Anwendungen zurückgegeben werden](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Zugehörige Themen](#related-topics)

## <a name="user-account-control"></a>Benutzerkontensteuerung

Unter UAC verfügen Konten in der [](/windows/desktop/SecGloss/a-gly)lokalen Administratorgruppe über zwei Zugriffstoken, eines mit Standardbenutzerberechtigungen und eines mit Administratorrechten. Aufgrund der UAC-Zugriffstokenfilterung wird ein Skript normalerweise unter dem Standardbenutzertoken ausgeführt, es sei denn, es wird "als Administrator" im Modus mit erhöhten Rechten ausgeführt. Nicht alle Skripts benötigten Administratorrechte.

Skripts können nicht programmgesteuert bestimmen, ob sie unter einem Standardbenutzersicherheitstoken oder einem Administratortoken ausgeführt werden. Für das Skript tritt möglicherweise ein Fehler mit dem Fehler "Zugriff verweigert" auf. Wenn das Skript Administratorrechte erfordert, muss es im Modus mit erhöhten Rechten ausgeführt werden. Der Zugriff auf WMI-Namespaces unterscheidet sich je nachdem, ob das Skript im Modus mit erhöhten Rechten ausgeführt wird. Einige WMI-Vorgänge, z. B. das Abrufen von Daten oder das Ausführen der meisten Methoden, erfordern nicht, dass das Konto als Administrator ausgeführt wird. Weitere Informationen zu Standardzugriffsberechtigungen finden Sie unter [Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md) und [Ausführen privilegierter Vorgänge.](executing-privileged-operations.md)

Aufgrund der Benutzerkontensteuerung muss sich das Konto, unter dem das Skript ausgeführt wird, in der Gruppe Administratoren auf dem lokalen Computer sein, damit es mit erhöhten Rechten ausgeführt werden kann.

Sie können ein Skript oder eine Anwendung mit erhöhten Rechten ausführen, indem Sie eine der folgenden Methoden ausführen:

**So führen Sie ein Skript im Modus mit erhöhten Rechten aus**

1.  Öffnen Sie ein Eingabeaufforderungsfenster, indem Sie mit der rechten Maustaste auf die Eingabeaufforderung im Startmenü und dann **auf Als Administrator ausführen klicken.**
2.  Planen Sie die Ausführung des Skripts mit erhöhten Rechten mit Taskplaner. Weitere Informationen finden Sie unter [Sicherheitskontexte für ausgeführte Tasks.](/windows/desktop/TaskSchd/security-contexts-for-running-tasks)
3.  Führen Sie das Skript mit dem integrierten Administratorkonto aus.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Konto, das zum Ausführen von WMI-Command-Line Tools erforderlich ist

Um die folgenden [WMI-Command-Line Tools](wmi-command-line-tools.md)auszuführen, muss sich Ihr Konto in der Gruppe Administratoren und das Tool über eine Eingabeaufforderung mit erhöhten Rechten ausführen. Das integrierte Administratorkonto kann diese Tools auch ausführen.

-   [**mofcomp**](mofcomp.md)

-   [**wmic**](wmic.md)

    Wenn Sie Wmic nach der Systeminstallation zum ersten Mal ausführen, muss es über eine Eingabeaufforderung mit erhöhten Rechten ausgeführt werden. Der Modus mit erhöhten Rechten ist möglicherweise nicht für nachfolgende Ausführungen von Wmic erforderlich, es sei denn, die WMI-Vorgänge erfordern Administratorrechte.

-   [**winmgmt**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

Um das [*WMI-Steuerelement*](gloss-w.md) (Wmimgmt.msc) ausführen und Änderungen an den Sicherheits- oder Überwachungseinstellungen des WMI-Namespace vornehmen zu können, muss Ihrem Konto das Recht Sicherheit bearbeiten explizit erteilt worden sein oder sich in der lokalen Administratorgruppe befinden. Das integrierte Administratorkonto kann auch die Sicherheit oder Überwachung für einen Namespace ändern.

Wbemtest.exe, ein Befehlszeilentool, das nicht von Microsoft-Kundendienstdiensten unterstützt wird, kann von Konten ausgeführt werden, die sich nicht in der lokalen Administratorgruppe befinden, es sei denn, ein bestimmter Vorgang erfordert Berechtigungen, die normalerweise Administratorkonten gewährt werden.

## <a name="handling-remote-connections-under-uac"></a>Behandeln von Remoteverbindungen unter UAC

Ob Sie eine Verbindung mit einem Remotecomputer in einer Domäne oder in einer Arbeitsgruppe herstellen, bestimmt, ob UAC-Filterung erfolgt.

Wenn Ihr Computer Teil einer Domäne ist, stellen Sie mithilfe eines Domänenkontos, das sich in der lokalen Administratorgruppe des Remotecomputers befindet, eine Verbindung mit dem Zielcomputer herstellen. Die UAC-Zugriffstokenfilterung wirkt sich dann nicht auf die Domänenkonten in der lokalen Gruppe Administratoren aus. Verwenden Sie kein lokales Nichtdomänenkonto auf dem Remotecomputer, auch wenn sich das Konto in der Gruppe Administratoren befindet.

In einer Arbeitsgruppe ist das Konto, das eine Verbindung mit dem Remotecomputer herstellen, ein lokaler Benutzer auf diesem Computer. Auch wenn sich das Konto in der Gruppe Administratoren befindet, bedeutet die UAC-Filterung, dass ein Skript als Standardbenutzer ausgeführt wird. Eine bewährte Methode besteht im Erstellen einer dedizierten lokalen Benutzergruppe oder eines dedizierten Benutzerkontos auf dem Zielcomputer speziell für Remoteverbindungen.

Die Sicherheit muss angepasst werden, damit dieses Konto verwendet werden kann, da das Konto nie über Administratorrechte verfügt hat. Geben Sie dem lokalen Benutzer:

-   Remotestart- und -aktivierungsrechte für den Zugriff auf DCOM. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)
-   Rechte für den Remotezugriff auf den WMI-Namespace (Remoteaktivieren). Weitere Informationen finden Sie unter [Zugriff auf WMI-Namespaces.](access-to-wmi-namespaces.md)
-   Das Recht, auf das spezifische sicherungsfähige Objekt zu zugreifen, abhängig von der sicherheit, die für das Objekt erforderlich ist.

Wenn Sie ein lokales Konto verwenden, weil Sie sich in einer Arbeitsgruppe befinden oder es sich um ein lokales Computerkonto handelt, werden Sie möglicherweise gezwungen, einem lokalen Benutzer bestimmte Aufgaben zu geben. Beispielsweise können Sie dem Benutzer das Recht gewähren, einen bestimmten Dienst über den SC.exe-Befehl, die [**Methoden GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) und [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) des [**\_ Win32-Diensts**](/windows/desktop/CIMWin32Prov/win32-service)oder über Gruppenrichtlinie mithilfe von Gpedit.msc zu beenden oder zu starten. Einige sicherungsfähige Objekte erlauben einem Standardbenutzer möglicherweise nicht das Ausführen von Aufgaben und bieten keine Möglichkeit, die Standardsicherheit zu ändern. In diesem Fall müssen Sie UAC möglicherweise deaktivieren, damit das lokale Benutzerkonto nicht gefiltert wird und stattdessen ein Volladministrator wird. Beachten Sie, dass das Deaktivieren der UAC aus Sicherheitsgründen ein letztes Mittel sein sollte.

Das Deaktivieren der Remote-UAC durch Ändern des Registrierungseintrags, der die Remote-UAC steuert, wird nicht empfohlen, kann aber in einer Arbeitsgruppe erforderlich sein. Der Registrierungseintrag ist **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\  \\ **Policies-System** \\ **LocalAccountTokenFilterPolicy**. Wenn der Wert dieses Eintrags 0 (null) ist, wird die Remote-UAC-Zugriffstokenfilterung aktiviert. Wenn der Wert 1 ist, ist die Remote-UAC deaktiviert.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>UAC-Auswirkung auf WMI-Daten, die an Skripts oder Anwendungen zurückgegeben werden

Wenn ein Skript oder eine Anwendung unter einem Konto in der Gruppe Administratoren ausgeführt wird, aber nicht mit erhöhten Rechten ausgeführt wird, werden möglicherweise nicht alle Daten zurückgegeben, da dieses Konto als Standardbenutzer ausgeführt wird. Die [*WMI-Anbieter*](gloss-p.md) für einige Klassen geben nicht alle Instanzen an ein Standardbenutzerkonto oder ein Administratorkonto zurück, das aufgrund der UAC-Filterung nicht als Volladministrator ausgeführt wird.

Die folgenden Klassen geben einige -Instanzen nicht zurück, wenn das Konto nach UAC gefiltert wird:

-   [**Win32 \_ Bus**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**Win32-Drucker \_**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**Win32 \_ ComponentCategory**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**Win32 \_ LogicalProgramGroupItem**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**Win32 \_ LogicalProgramGroup**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**Win32 \_ NetworkConnection**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**Win32 \_ UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**Win32 \_ PrinterDriver**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**Win32 \_ PortResource**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**Win32 \_ DeviceMemoryAddress**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

Die folgenden Klassen geben einige Eigenschaften nicht zurück, wenn das Konto nach UAC gefiltert wird:

-   [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**Win32 \_ DCOMApplication**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**Win32 \_ Baseboard**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**\_Win32-HauptplatineGeräte**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**Win32 \_ VideoController**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**Win32 \_ ParallelPort**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**Win32 \_ IRQResource**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**Win32 \_ NetworkProtocol**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[Zugriff auf sicherungsfähige WMI-Objekte](access-to-wmi-securable-objects.md)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
