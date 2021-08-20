---
description: Skripts können auf alle WMI-Klassen für Hardware- und Softwareobjekte zugreifen.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Skripterstellung für den Zugriff auf WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0169da5b2d7d9d542d7fe686ae34f5bf2aeb3c4fdfff1e268dc3ca2bfdddd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992390"
---
# <a name="scripting-access-to-wmi"></a>Skripterstellung für den Zugriff auf WMI

Skripts können auf alle WMI-Klassen für Hardware- und Softwareobjekte zugreifen. Windows Skripthostskripts (WSH) können Vorgänge für Dateisystemobjekte ausführen, Netzwerkdrucker bearbeiten oder Umgebungsvariablen ändern. Eine Vielzahl von Administratoraufgaben und eine kurze Anleitung dazu finden Sie unter WMI Tasks [for Scripts and Applications (WMI-Aufgaben für Skripts und Anwendungen).](wmi-tasks-for-scripts-and-applications.md) Weitere Informationen und Beispiele finden Sie im TechNet ScriptCenter [Script Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).

Wenn Sie noch nicht mit Skripts oder WMI-spezifischen Skripts arbeiten, lesen Sie den TechNet ScriptCenter-Abschnitt [Erste Schritte.](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx)

Mit der [Skripterstellungs-API für WMI](scripting-api-for-wmi.md)können Sie schnelle, einfache Skripts oder komplexe Anwendungen entwickeln. Die Skripterstellung bietet Ihnen die gleiche Möglichkeit, Informationen zu erhalten oder die meisten Objekte in einem Unternehmen zu konfigurieren, die Sie auch über eine C++- oder C#-Anwendung haben würden. Weitere Informationen finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Sie können keinen [*WMI-Anbieter im*](gloss-p.md) Skript schreiben. Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI.](providing-data-to-wmi.md)

WMI-Skripts können in jeder Skriptsprache geschrieben werden, die mit ActiveX interagieren kann.

Windows PowerShell bietet eine einfache Umgebung für die WMI-Verwaltung und -Skripterstellung. Weitere Informationen zu PowerShell finden Sie unter Erste Schritte [mit Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).

ADSI-Skripts (Active Directory Service Interfaces) bieten Zugriff auf Active Directory Domain Services -Objekte (AD DS). Sowohl WSH- als auch ADSI-Skripts greifen auf Objekte zu und lassen Prozeduren zu, die nicht über Batchdateien verfügbar sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[Skripterstellungs-API für WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
