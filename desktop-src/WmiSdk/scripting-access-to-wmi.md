---
description: Skripts können auf alle WMI-Klassen für Hardware-und Software Objekte zugreifen.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Skripterstellung für den WMI-Zugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215335"
---
# <a name="scripting-access-to-wmi"></a>Skripterstellung für den WMI-Zugriff

Skripts können auf alle WMI-Klassen für Hardware-und Software Objekte zugreifen. WSH-Skripts (Windows Script Host) können Vorgänge für Dateisystem Objekte, zum Bearbeiten von Netzwerkdruckern oder zum Ändern von Umgebungsvariablen ausführen. Sie finden eine Vielzahl von Administrator Aufgaben und eine kurze Anleitung dazu, wie Sie diese in WMI unter [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)ausführen. Weitere Informationen und Beispiele finden Sie im technet scriptcenter [Script-Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).

Wenn Sie mit der Skripterstellung oder WMI-spezifischer Skripterstellung noch nicht vertraut sind, lesen Sie den Abschnitt [zu](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx)den ersten Schritten im technet scriptcenter.

Mit der [Skript-API für WMI](scripting-api-for-wmi.md)können Sie schnelle, einfache Skripts oder komplexe Anwendungen entwickeln. Mithilfe der Skripterstellung erhalten Sie die gleichen Möglichkeiten, Informationen zu erhalten oder die meisten Objekte in einem Unternehmen zu konfigurieren, wie Sie dies über eine C++-oder c#-Anwendung tun würden. Weitere Informationen finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Ein [*WMI-Anbieter*](gloss-p.md) kann nicht in ein Skript geschrieben werden. Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).

WMI-Skripts können in jeder Skriptsprache geschrieben werden, die mit ActiveX-Objekten interagieren kann.

Windows PowerShell stellt eine einfache Umgebung für die WMI-Administration und-Skripterstellung bereit. Weitere Informationen zu PowerShell finden Sie unter [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).

Active Directory Service Interfaces (ADSI)-Skripts ermöglichen den Zugriff auf Active Directory Domain Services Objekte (AD DS). Sowohl WSH-als auch ADSI-Skripts greifen auf Objekte und Zulassungs Prozeduren zu

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[Skript-API für WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
