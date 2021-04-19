---
description: Die Benutzerkontensteuerung (User Account Control, UAC) wirkt sich auf die WMI-Daten aus, die von einem Befehlszeilen Tool, Remote Zugriff und die Ausführung von Skripts zurückgegeben werden. Weitere Informationen zu UAC finden Sie unter Getting Started with User Account Control.
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
ms.openlocfilehash: 39d48abcffa537d886397092c6d4a7b558825021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363610"
---
# <a name="user-account-control-and-wmi"></a>Benutzerkontensteuerung und WMI

Die Benutzerkontensteuerung (User Account Control, UAC) wirkt sich auf die WMI-Daten aus, die von einem Befehlszeilen Tool, Remote Zugriff und die Ausführung von Skripts zurückgegeben werden. Weitere Informationen zu UAC finden Sie unter [Getting Started with User Account Control](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

In den folgenden Abschnitten werden die UAC-Funktionen beschrieben:

-   [Benutzerkontensteuerung](#user-account-control-and-wmi)
-   [Zum Ausführen von WMI-Command-Line Tools benötigtes Konto](#account-needed-to-run-wmi-command-line-tools)
-   [Behandeln von Remote Verbindungen unter UAC](#handling-remote-connections-under-uac)
-   [UAC-Auswirkung auf WMI-Daten, die an Skripte oder Anwendungen zurückgegeben werden](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Zugehörige Themen](#related-topics)

## <a name="user-account-control"></a>Benutzerkontensteuerung

Unter UAC verfügen Konten in der lokalen Gruppe "Administratoren" über zwei [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly), eine mit Standardbenutzer Berechtigungen und eine mit Administratorrechten. Aufgrund der UAC-Zugriffs Token-Filterung wird ein Skript normalerweise unter dem Standardbenutzer Token ausgeführt, es sei denn, es wird als Administrator im Modus mit erhöhten Rechten ausgeführt. Nicht für alle Skripts wurden Administratorrechte benötigt.

Skripts können nicht Programm gesteuert ermitteln, ob Sie unter einem Standardbenutzer-Sicherheits Token oder einem Administrator Token ausgeführt werden. Das Skript kann mit dem Fehler "Zugriff verweigert" fehlschlagen. Wenn das Skript Administratorrechte erfordert, muss es im Modus mit erhöhten Rechten ausgeführt werden. Der Zugriff auf WMI-Namespaces unterscheidet sich abhängig davon, ob das Skript im Modus mit erhöhten Rechten ausgeführt wird. Einige WMI-Vorgänge, wie z. b. das Anfordern von Daten oder das Ausführen der meisten Methoden, erfordern nicht, dass das Konto als Administrator ausgeführt wird. Weitere Informationen zu Standard Zugriffsberechtigungen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

Aufgrund der Benutzerkontensteuerung muss das Konto, unter dem das Skript ausgeführt wird, in der Gruppe "Administratoren" auf dem lokalen Computer enthalten sein, um mit erhöhten Rechten ausgeführt werden zu können.

Sie können ein Skript oder eine Anwendung mit erhöhten Rechten ausführen, indem Sie eine der folgenden Methoden ausführen:

**So führen Sie ein Skript im erweiterten Modus aus**

1.  Öffnen Sie ein Eingabe Aufforderungs Fenster, indem Sie im Startmenü mit der rechten Maustaste auf Eingabeaufforderung und dann auf **als Administrator ausführen** klicken.
2.  Planen Sie die Ausführung des Skripts mit erhöhten Rechten Taskplaner. Weitere Informationen finden Sie unter [Sicherheits Kontexte zum Ausführen von Tasks](/windows/desktop/TaskSchd/security-contexts-for-running-tasks).
3.  Führen Sie das Skript mit dem integrierten Administrator Konto aus.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Zum Ausführen von WMI-Command-Line Tools benötigtes Konto

Um die folgenden [WMI-Command-Line Tools](wmi-command-line-tools.md)auszuführen, muss Ihr Konto in der Gruppe "Administratoren" sein, und das Tool muss von einer Eingabeaufforderung mit erhöhten Rechten ausgeführt werden. Mit dem integrierten Administrator Konto können auch diese Tools ausgeführt werden.

-   [**Mofcomp**](mofcomp.md)

-   [**wmic**](wmic.md)

    Wenn Sie WMIC zum ersten Mal nach der Systeminstallation ausführen, muss Sie von einer Eingabeaufforderung mit erhöhten Rechten ausgeführt werden. Der Modus mit erhöhten Rechten ist möglicherweise für nachfolgende Ausführungen von WMIC nicht erforderlich, es sei denn, die WMI-Vorgänge erfordern Administratorrechte

-   [**WinMgmt**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

Um das [*WMI-Steuer*](gloss-w.md) Element (wmimgmt. msc) auszuführen und Änderungen an den Sicherheits-oder Überwachungs Einstellungen für WMI-Namespaces vorzunehmen, muss für Ihr Konto das Sicherheitsrecht bearbeiten explizit gewährt werden, oder es muss in der lokalen Gruppe Administratoren vorhanden sein. Das integrierte Administrator Konto kann auch die Sicherheit oder die Überwachung für einen Namespace ändern.

Wbemtest.exe: ein Befehlszeilen Tool, das nicht vom Microsoft-Kundendienst unterstützt wird, kann von Konten ausgeführt werden, die nicht in der lokalen Administrator Gruppe sind, es sei denn, für einen bestimmten Vorgang sind Berechtigungen erforderlich, die normalerweise Administrator Konten gewährt werden.

## <a name="handling-remote-connections-under-uac"></a>Behandeln von Remote Verbindungen unter UAC

Ob Sie eine Verbindung mit einem Remote Computer in einer Domäne oder in einer Arbeitsgruppe herstellen, legt fest, ob die UAC-Filterung stattfindet.

Wenn der Computer zu einer Domäne gehört, stellen Sie eine Verbindung mit dem Zielcomputer her, indem Sie ein Domänen Konto verwenden, das sich in der lokalen Gruppe "Administratoren" des Remote Computers befindet. Die UAC-Zugriffs Token-Filterung wirkt sich nicht auf die Domänen Konten in der lokalen Administratoren Gruppe aus. Verwenden Sie kein lokales, nicht-Domänen Konto auf dem Remote Computer, auch wenn das Konto der Gruppe "Administratoren" angehört.

In einer Arbeitsgruppe ist das Konto, das eine Verbindung mit dem Remote Computer herstellt, ein lokaler Benutzer auf diesem Computer. Auch wenn das Konto der Gruppe "Administratoren" angehört, bedeutet die UAC-Filterung, dass ein Skript als Standardbenutzer ausgeführt wird. Eine bewährte Vorgehensweise ist das Erstellen einer dedizierten lokalen Benutzergruppe oder eines Benutzerkontos auf dem Bereitstellungs Zielcomputer speziell für Remote Verbindungen.

Die Sicherheit muss angepasst werden, damit dieses Konto verwendet werden kann, da das Konto nie über Administratorrechte verfügt. Legen Sie dem lokalen Benutzer Folgendes:

-   Remote Start und Aktivieren von Rechten für den Zugriff auf DCOM. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).
-   Rechte für den Remote Zugriff auf den WMI-Namespace (Remote Aktivierung). Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md).
-   Das Recht, auf das spezifische Sicherungs fähige Objekt zuzugreifen, abhängig von der für das Objekt erforderlichen Sicherheit.

Wenn Sie ein lokales Konto verwenden, weil Sie sich entweder in einer Arbeitsgruppe befinden oder wenn es sich um ein lokales Computer Konto handelt, sind Sie möglicherweise gezwungen, bestimmte Aufgaben an einen lokalen Benutzer zu übergeben. Beispielsweise können Sie dem Benutzer die Berechtigung erteilen, einen bestimmten Dienst mithilfe des SC.exe-Befehls, der [**getsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) -Methode und der [**SETSECURITYDESCRIPTOR**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) -Methode des [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)oder über Gruppenrichtlinie mithilfe von "gpeer dit. msc" anzuhalten oder zu starten. Einige Sicherungs fähige Objekte erlauben es einem Standardbenutzer möglicherweise nicht, Aufgaben auszuführen, und bieten keine Möglichkeit, die Standard Sicherheit zu ändern. In diesem Fall müssen Sie ggf. die Benutzerkontensteuerung deaktivieren, damit das lokale Benutzerkonto nicht gefiltert wird, sondern zu einem vollständigen Administrator. Beachten Sie, dass die Deaktivierung der Benutzerkontensteuerung aus Sicherheitsgründen ein letztes Mittel sein sollte.

Das Deaktivieren der Remote-UAC durch Ändern des Registrierungs Eintrags, der die Remote-Benutzerkontensteuerung steuert, wird nicht empfohlen, kann aber in einer Arbeitsgruppe erforderlich sein. Der Registrierungs Eintrag lautet **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy**. Wenn der Wert dieses Eintrags NULL (0) ist, ist die Remote-UAC-Zugriffs Token-Filterung aktiviert. Wenn der Wert 1 ist, ist die Remote-UAC deaktiviert.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>UAC-Auswirkung auf WMI-Daten, die an Skripte oder Anwendungen zurückgegeben werden

Wenn ein Skript oder eine Anwendung unter einem Konto in der Gruppe "Administratoren" ausgeführt wird, aber nicht mit erhöhten Rechten ausgeführt wird, werden möglicherweise nicht alle zurückgegebenen Daten angezeigt, weil dieses Konto als Standardbenutzer ausgeführt wird. Die WMI- [*Anbieter*](gloss-p.md) für einige Klassen geben nicht alle Instanzen an ein Standardbenutzer Konto oder ein Administrator Konto zurück, das aufgrund der UAC-Filterung nicht als vollständiger Administrator ausgeführt wird.

Die folgenden Klassen geben nicht einige Instanzen zurück, wenn das Konto nach UAC gefiltert wird:

-   [**Win32- \_ Bus**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**Win32- \_ Komponenten Kategorie**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**Win32 \_ logicalprogramgroupitem**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**Win32 \_ logicalprogramgroup**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**Win32- \_ NetworkConnection**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**Win32- \_ Benutzerkonto**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**Win32- \_ PrinterDriver**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**Win32- \_ portresource**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**Win32 \_ devicememoryaddress**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

In den folgenden Klassen werden einige Eigenschaften nicht zurückgegeben, wenn das Konto nach UAC gefiltert wird:

-   [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**Win32- \_ dcomapplicationsetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**Win32- \_ dcomapplication**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**Win32- \_ Baseboard**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**Win32- \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**Win32- \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**Win32- \_ motherboardgerät**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**Win32- \_ diskdrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**Win32- \_ pnptity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**Win32- \_ Videocontroller**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**Win32- \_ Parallelport**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**Win32- \_ System Treiber**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**Win32-Webressource \_**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**Win32- \_ networkprotocol**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md)
</dt> <dt>

[Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
