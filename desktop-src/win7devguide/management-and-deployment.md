---
title: Verwaltung und Bereitstellung
description: IT-Experten oder Entwickler, die sich für die Bereitstellung von Windows 7 vorbereiten, haben aufgrund von Verbesserungen bei den Abbild Erstellungs Features und-Tools ein höheres Maß an Vertrauen
ms.assetid: 217090c4-6385-4333-a380-f75f2c80e369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105b19ad01cb9208d05e77871be637fdadcb0532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948888"
---
# <a name="management-and-deployment"></a>Verwaltung und Bereitstellung

IT-Experten oder Entwickler, die sich für die Bereitstellung von Windows 7 vorbereiten, haben aufgrund von Verbesserungen bei den Abbild Erstellungs Features und-Tools ein höheres Maß an Vertrauen Hierzu gehören Unterstützung für die Verwaltung von Anwendungen, Treibern und Betriebssystemen in Offline Abbild Dateien. Außerdem sind die Image Erstellung und-Verwaltung einfacher und für eine größere Anzahl von IT-Organisationen verfügbar. Das Bereitstellen von Windows 7 auf Geschäftscomputern ist aufgrund neuer IT-Migrationstools und automatisierter Bereitstellungs Technologien auch einfacher und schneller.

## <a name="windows-powershell-20"></a>Windows PowerShell 2.0

PowerShell ist eine umfassende Microsoft .NET verwaltete Skriptsprache, die sowohl über eine interaktive Befehlszeilenshell als auch über eine grafische Integrated Scripting Environment (ISE) verfügt. Es unterstützt Verzweigungen, Schleifen, Funktionen, Debugging, Ausnahmebehandlung und Internationalisierung. PowerShell 2,0 ist Teil von Windows 7 und bietet zahlreiche Verbesserungen und einen wachsenden Satz von *Cmdlets* für die Windows-Diagnose, Microsoft Active Directory, Microsoft Internetinformationsdienste (IIS) und mehr.

Das PowerShell 2,0-Remoting-Feature ermöglicht Benutzern jetzt das Ausführen von Befehlen auf einem oder mehreren Remote Computern von einem einzelnen Computer aus, auf dem PowerShell ausgeführt wird. Entwickler können auch PowerShell auf IIS hosten, um auf Ihre Server zuzugreifen und diese zu verwalten.

PowerShell 2,0 unterstützt das Partitionieren und organisieren von PowerShell-Skripts mithilfe von Modulen, die als eigenständige, wiederverwendbare Einheiten verteilt und bereitgestellt werden können. Es umfasst auch die Unterstützung von Transaktionen in der PowerShell-Engine und APIs, was bedeutet, dass Entwickler mithilfe integrierter Transaktions- *Cmdlets* Transaktionen starten, ausführen und ein Rollback ausführen können. Außerdem bietet das PowerShell-Modul eine Ereignis-Unterstützung für das lauschen, weiterleiten und reagieren auf Verwaltungs-und Systemereignisse. PowerShell-Anwendungen können so geschrieben werden, dass bestimmte Ereignisse für die synchrone oder asynchrone Verarbeitung abonniert werden. (Siehe [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx).)

![Windows PowerShell ISE-Bildschirmfoto](images/windows7-devguide-solidfig1-powershell.jpg)

Abbildung 1. Windows PowerShell ist eine komplette, von .NET verwaltete Skriptsprache mit einer interaktiven Befehlszeilenshell und einer grafischen ISE.

## <a name="windows-installer"></a>Windows Installer

Windows Installer wurde aktualisiert, um die Effizienz der Entwickler zu steigern, indem die Menge an benutzerdefiniertem Code reduziert wird, der zum Erstellen eines Installationspakets und zum Erstellen von echten pro-Benutzer-Softwareinstallationen erforderlich ist.

Mit mehreren Paket Transaktionen können Entwickler eine einzelne Transaktion aus mehreren Paketen erstellen, indem Sie eine "Chainer" verwenden, um Pakete dynamisch in die Transaktion einzubeziehen. Wenn mindestens eines der Pakete nicht erwartungsgemäß installiert wird, führen Sie einfach ein Rollback der Installation aus.

Der eingebettete UI-Handler vereinfacht die Integration benutzerdefinierter Benutzeroberflächen, indem ein benutzerdefinierter Benutzeroberflächen Handler in das Windows Installer Paket eingebettet wird.

Das eingebettete Multiple Package Chainer ermöglicht Entwicklern das Aktivieren von Installations Ereignissen über mehrere Pakete. Beispielsweise können Sie Ereignisse für die Bedarfs gesteuerte Installation aktivieren, Ereignisse reparieren und Ereignisse in mehreren Paketen deinstallieren.

Neue Features ermöglichen auch die Erstellung von echten pro-Benutzer-Installationen, einschließlich der Unterstützung für benutzerspezifische Programmdateien und der Erweiterung "jetzt erhöhen". Außerdem bieten Sie Unterstützung für die Offline Software Inventur und patchanwendbarkeits Prüfungen durch Abbild Verwaltung für die Bereitstellung. (Weitere Informationen finden Sie [unter What es New in Windows Installer 5,0](../msi/what-s-new-in-windows-installer-5-0.md).)

 

 