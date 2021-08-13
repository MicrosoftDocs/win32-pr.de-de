---
description: Jede Skriptsprache wie VBScript, die mit ActiveX-Objekten funktioniert, kann auf WMI-Daten zugreifen. Anwendungen können mithilfe der COM-API für WMI oder in Visual Basic mithilfe der Wbemdisp.tlb-Typbibliothek und der Skript-API für WMI auf WMI in C++ zugreifen. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Erstellen einer WMI-Anwendung oder eines WMI-Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddde26b2a8495126b4aa26c132adb49860627230d698431df5d713e653f1d874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412130"
---
# <a name="creating-a-wmi-application-or-script"></a>Erstellen einer WMI-Anwendung oder eines WMI-Skripts

Jede Skriptsprache wie VBScript, die mit ActiveX-Objekten funktioniert, kann auf WMI-Daten zugreifen. Anwendungen können mithilfe der [COM-API für WMI](com-api-for-wmi.md) oder in Visual Basic mithilfe der Wbemdisp.tlb-Typbibliothek und der [Skript-API für WMI](scripting-api-for-wmi.md)auf WMI in C++ zugreifen. [](using-the-wmi-scripting-type-library.md) . Sie können Daten über WMI abrufen, indem Sie ein Skript, eine Active Server Page (ASP) oder eine HTML-Anwendung (HTA) schreiben. Sie können auch Windows PowerShell verwenden, um Daten abzurufen oder Skripts zu schreiben. Weitere Informationen finden Sie unter [Skripterstellung in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) und [Erste Schritte mit Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). Das TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) enthält Hunderte von Skriptbeispielen. Weitere Informationen zu Druck- und Onlineressourcen finden Sie unter [Weitere Informationen.](further-information.md)

Im folgenden Verfahren wird beschrieben, wie Sie eine Verbindung mit dem WMI-Dienst und dem Datenspeicher herstellen.

**So stellen Sie eine Verbindung mit dem WMI-Dienst und dem Datenspeicher her**

1.  Suchen Sie den WMI-Dienst auf einem bestimmten Computer.
2.  Verbinden zu einem oder mehreren WMI-Namespaces.

Diese Vorgänge unterscheiden sich in C++, Visual Basic, .NET Framework Sprachen oder bei Verwendung eines Skripts. Skripts und Visual Basic Anwendungen müssen auf Klassen zugreifen, deren Instanzen von vorhandenen Anbietern mit Daten bereitgestellt werden. In C++ geschriebene Anwendungen können jedoch mehr erreichen. Beispielsweise kann eine in C++ geschriebene Anwendung Ereignisse senden, aber ein WMI-Skript kann nur das Empfangen von Ereignissen abonnieren.

Ein WMI-Anbieter kann nur in C++ oder mithilfe der .NET Framework geschrieben werden. Weitere Informationen zum Schreiben von Anwendungen in C# oder Visual Basic .NET finden Sie unter [WMI .NET Overview](/previous-versions/bb404655(v=vs.90)).

Weitere Informationen zum Erstellen von Anwendungen und Skripts für WMI finden Sie unter:

-   [Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md)
-   [Erstellen eines WMI-Skripts](creating-a-wmi-script.md)
-   [Erstellen eines verwalteten WMI-Clients](creating-a-managed-wmi-client.md)

Um die meisten Aufgaben auszuführen, verwenden Sie die vorinstallierten [WMI-Klassen](wmi-classes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 
