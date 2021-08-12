---
description: Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) ist die Infrastruktur für Verwaltungsdaten und -vorgänge auf Windows-basierten Betriebssystemen.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Windows-Verwaltungsinstrumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b08c0301881b57c8132be9eead2e5b52cb64d4d3c4278985a573d5bff94f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553134"
---
# <a name="windows-management-instrumentation"></a>Windows-Verwaltungsinstrumentation

## <a name="purpose"></a>Zweck

Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) ist die Infrastruktur für Verwaltungsdaten und -vorgänge auf Windows-basierten Betriebssystemen. Sie können WMI-Skripts oder -Anwendungen schreiben, um administrative Aufgaben auf Remotecomputern zu automatisieren. WMI stellt jedoch auch Verwaltungsdaten für andere Teile des Betriebssystems und der Produkte bereit, z. B. System Center Operations Manager, ehemals Microsoft Operations Manager (MOM) oder Windows Remoteverwaltung ([WinRM](/windows/desktop/WinRM/portal)).

> [!Note]  
> Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren. Wenn Sie ein Endbenutzer sind, für den eine WMI-Fehlermeldung angezeigt wurde, sollten Sie [zu Microsoft-Support](https://support.microsoft.com/) wechseln und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird. Weitere Informationen zur Problembehandlung bei WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> WMI wird von Microsoft vollständig unterstützt. Die neueste Version der administrativen Skripterstellung und Steuerung ist jedoch über die Windows Management Infrastructure (MI) verfügbar. MI ist vollständig kompatibel mit früheren Versionen von WMI und bietet eine Vielzahl von Features und Vorteilen, die das Entwerfen und Entwickeln von Anbietern und Clients einfacher als je zuvor machen. Weitere Informationen finden Sie unter [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

 

## <a name="where-applicable"></a>Anwendungsbereich

WMI kann in allen Windows-basierten Anwendungen verwendet werden und eignet sich besonders für Unternehmensanwendungen und Administrative Skripts.

Systemadministratoren finden Informationen zur Verwendung von WMI im TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)und in verschiedenen Büchern zu WMI. Weitere Informationen finden Sie unter [Weitere Informationen.](further-information.md)

## <a name="developer-audience"></a>Entwicklergruppe

WMI ist für Programmierer konzipiert, die C/C++, die Microsoft Visual Basic-Anwendung oder eine Skriptsprache verwenden, die über eine Engine für Windows verfügt und Microsoft ActiveX-Objekte verarbeitet. Obwohl einige Vertrautheit mit der COM-Programmierung hilfreich ist, finden C++-Entwickler, die Anwendungen schreiben, gute Beispiele für die ersten Schritte unter [Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md).

Informationen zum Entwickeln von Anbietern oder Anwendungen für verwalteten Code in C# oder Visual Basic .NET mithilfe des .NET Framework finden Sie [unter WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Viele Administratoren und IT-Experten greifen über PowerShell auf WMI zu. Mit dem Cmdlet Get-WMI für PowerShell können Sie Informationen für ein lokales oder Remote-WMI-Repository abrufen. Daher enthalten eine Reihe von Themen und Klassen, insbesondere im Abschnitt [Erstellen von WMI-Clients,](creating-wmi-clients.md) PowerShell-Beispiele. Weitere Informationen zur Verwendung von PowerShell finden Sie unter [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) und [Skripterstellung mit Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Weitere Informationen dazu, welches Betriebssystem für die Verwendung eines bestimmten API-Elements oder einer WMI-Klasse erforderlich ist, finden Sie im Abschnitt Anforderungen jedes Themas in der WMI-Dokumentation.

Wenn eine erwartete Komponente zu fehlen scheint, finden Sie weitere Informationen unter [Betriebssystemverfügbarkeit von WMI-Komponenten.](operating-system-availability-of-wmi-components.md)

Sie müssen keine bestimmte Softwareentwicklung (SDK) herunterladen oder installieren, um Skripts oder Anwendungen für WMI zu erstellen. Es gibt jedoch einige WMI-Verwaltungstools, die Entwickler nützlich finden. Weitere Informationen finden Sie im Abschnitt Downloads unter [Weitere Informationen.](further-information.md)

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dd>

Allgemeine Informationen zu WMI.

</dd> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> <dd>

Informationen zum Entwickeln von Anwendungen für die Verwendung von WMI, einschließlich Informationen zu Tools.

</dd> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> <dd>

Dokumentation zu WMI-Klassen, WMI C++-Klassen, WMI COM-API, Skript-API und anderem WMI-Referenzmaterial.

</dd> </dl>

 

 
