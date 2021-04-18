---
description: Windows-Verwaltungsinstrumentation (WMI) ist die Infrastruktur für Verwaltungsdaten und Vorgänge auf Windows-basierten Betriebssystemen.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Windows-Verwaltungsinstrumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347913"
---
# <a name="windows-management-instrumentation"></a>Windows-Verwaltungsinstrumentation

## <a name="purpose"></a>Zweck

Windows-Verwaltungsinstrumentation (WMI) ist die Infrastruktur für Verwaltungsdaten und Vorgänge auf Windows-basierten Betriebssystemen. Sie können WMI-Skripts oder-Anwendungen schreiben, um administrative Aufgaben auf Remote Computern zu automatisieren, aber WMI stellt auch Verwaltungsdaten für andere Teile des Betriebssystems und der Produkte bereit, z. b. System Center Operations Manager, früher Microsoft Operations Manager (MOM) oder Windows-Remoteverwaltung ([WinRM](/windows/desktop/WinRM/portal)).

> [!Note]  
> Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren. Wenn Sie ein Endbenutzer sind, bei dem eine Fehlermeldung zu WMI aufgetreten ist, sollten Sie [Microsoft-Support](https://support.microsoft.com/) aufrufen und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird. Weitere Informationen zur Behebung von Problemen mit WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI funktioniert nicht!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> WMI wird von Microsoft vollständig unterstützt. die neueste Version von administrativer Skripterstellung und-Steuerung ist jedoch über die Windows-Verwaltungsinfrastruktur (Mi) verfügbar. Mi ist vollständig kompatibel mit früheren Versionen von WMI und bietet eine Reihe von Features und Vorteilen, mit denen das Entwerfen und entwickeln von Anbietern und Clients einfacher als je zuvor ist. Weitere Informationen finden Sie unter [Windows Management Infrastructure (Mi)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

 

## <a name="where-applicable"></a>Anwendungsbereich

WMI kann in allen Windows-basierten Anwendungen verwendet werden und ist am nützlichsten in Unternehmensanwendungen und administrativen Skripts.

System Administratoren finden Informationen zur Verwendung von WMI im TechNet [scriptcenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)und in verschiedenen Büchern zu WMI. Weitere Informationen finden Sie unter [Weitere Informationen](further-information.md).

## <a name="developer-audience"></a>Entwicklergruppe

WMI ist für Programmierer konzipiert, die C/C++, die Microsoft Visual Basic-Anwendung oder eine Skriptsprache verwenden, die über eine Engine unter Windows verfügt und Microsoft ActiveX-Objekte verarbeitet. Obwohl eine gewisse Vertrautheit mit der com-Programmierung hilfreich ist, können C++-Entwickler, die Anwendungen schreiben, gute Beispiele für den Einstieg in die [Erstellung einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md)finden.

Informationen zum Entwickeln von verwalteten Code Anbietern oder-Anwendungen in c# oder Visual Basic .NET mithilfe der .NET Framework finden Sie unter [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Viele Administratoren und IT-Spezialisten greifen über PowerShell auf WMI zu. Mit dem Cmdlet "Get-WMI" für PowerShell können Sie Informationen für ein lokales oder Remote-WMI-Repository abrufen. Eine Reihe von Themen und Klassen, insbesondere im Abschnitt [Erstellen von WMI-Clients](creating-wmi-clients.md) , enthalten beispielsweise PowerShell-Beispiele. Weitere Informationen zur Verwendung von PowerShell finden Sie unter [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) und [Skripterstellung mit Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Weitere Informationen über das Betriebssystem, das für die Verwendung eines bestimmten API-Elements oder einer WMI-Klasse erforderlich ist, finden Sie im Abschnitt "Anforderungen" jedes Themas in der WMI-Dokumentation.

Wenn eine erwartete Komponente fehlt, finden Sie weitere Informationen unter [Betriebs System Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).

Sie müssen keine bestimmte Softwareentwicklung (SDK) herunterladen oder installieren, um Skripts oder Anwendungen für WMI zu erstellen. Es gibt jedoch einige WMI-Verwaltungs Tools, die Entwickler nützlich finden. Weitere Informationen finden Sie im Abschnitt "Downloads" unter [Weitere Informationen](further-information.md).

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dd>

Allgemeine Informationen zu WMI.

</dd> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> <dd>

Informationen zum Entwickeln von Anwendungen für die Verwendung von WMI, einschließlich Informationen zu-Tools.

</dd> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> <dd>

Dokumentation zu den WMI-Klassen, WMI-C++-Klassen, WMI-com-API, Skript-API und anderem WMI-Referenzmaterial.

</dd> </dl>

 

 
