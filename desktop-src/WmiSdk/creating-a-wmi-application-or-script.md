---
description: Jede Skriptsprache, z. b. VBScript, die mit ActiveX-Objekten funktioniert, kann auf WMI-Daten zugreifen. Anwendungen können auf WMI in C++ mithilfe der com-API für WMI oder in Visual Basic zugreifen, mithilfe der wbemdisp. tlb-Typbibliothek und der Skript-API für WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Erstellen einer WMI-Anwendung oder eines Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349648"
---
# <a name="creating-a-wmi-application-or-script"></a>Erstellen einer WMI-Anwendung oder eines Skripts

Jede Skriptsprache, z. b. VBScript, die mit ActiveX-Objekten funktioniert, kann auf WMI-Daten zugreifen. Anwendungen können auf WMI in C++ mithilfe der [com-API für WMI](com-api-for-wmi.md) oder in Visual Basic zugreifen, mithilfe der wbemdisp. tlb- [Typbibliothek](using-the-wmi-scripting-type-library.md) und der [Skript-API für WMI](scripting-api-for-wmi.md). . Sie können Daten über WMI abrufen, indem Sie ein Skript, eine Active Server Seite (ASP) oder eine HTML-Anwendung (HTA) schreiben. Sie können auch Windows PowerShell verwenden, um Daten abzurufen oder Skripts zu schreiben. Weitere Informationen finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) und [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). Das technet scriptcenter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) enthält Hunderte von Skript Beispielen. Weitere Informationen zu Druck-und Online Ressourcen finden Sie unter [Weitere Informationen](further-information.md).

Im folgenden Verfahren wird beschrieben, wie eine Verbindung mit dem WMI-Dienst und dem Datenspeicher hergestellt wird.

**So stellen Sie eine Verbindung mit dem WMI-Dienst und Datenspeicher her**

1.  Suchen Sie den WMI-Dienst auf einem bestimmten Computer.
2.  Stellen Sie eine Verbindung mit einem oder mehreren WMI-Namespaces her.

Diese Vorgänge unterscheiden sich in C++, Visual Basic, .NET Framework Sprachen oder bei Verwendung eines Skripts. Skripts und Visual Basic Anwendungen müssen auf Klassen zugreifen, deren Instanzen von vorhandenen Anbietern mit Daten bereitgestellt werden. Anwendungen, die in C++ geschrieben wurden, können jedoch mehr tun. Beispielsweise kann eine in C++ geschriebene Anwendung Ereignisse senden, aber ein WMI-Skript kann nur Empfangs Ereignisse abonnieren.

Ein WMI-Anbieter kann nur in C++ oder mithilfe der .NET Framework geschrieben werden. Weitere Informationen zum Schreiben von Anwendungen in c# oder Visual Basic .net finden Sie unter [Übersicht über WMI .net](/previous-versions/bb404655(v=vs.90)).

Weitere Informationen zum Erstellen von Anwendungen und Skripts für WMI finden Sie unter:

-   [Erstellen einer WMI-Anwendung mithilfe von C++](creating-a-wmi-application-using-c-.md)
-   [Erstellen eines WMI-Skripts](creating-a-wmi-script.md)
-   [Erstellen eines verwalteten WMI-Clients](creating-a-managed-wmi-client.md)

Verwenden Sie die vorinstallierten [WMI-Klassen](wmi-classes.md), um die meisten Aufgaben auszuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 
