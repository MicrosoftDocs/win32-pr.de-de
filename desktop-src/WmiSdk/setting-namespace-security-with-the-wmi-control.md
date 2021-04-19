---
description: Beim WMI-Steuerelement handelt es sich um ein MMC-Snap-in in der Systemsteuerung, das verwendet wird, um die WMI-Namespace Sicherheit manuell auf einem lokalen Computer festzulegen. Sie können auch den Standard Namespace für die Skripterstellung festlegen.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Festlegen der Namespace Sicherheit mit dem WMI-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351098"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>Festlegen der Namespace Sicherheit mit dem WMI-Steuerelement

Beim WMI-Steuerelement handelt es sich um ein MMC-Snap-in in der **Systemsteuerung** , das verwendet wird, um die WMI-Namespace Sicherheit manuell auf einem lokalen Computer festzulegen. Sie können auch den Standard Namespace für die Skripterstellung festlegen.


Im folgenden Verfahren wird beschrieben, wie Sie das WMI-Steuerelement finden.

**So suchen Sie das WMI-Steuerelement**

1.  Doppelklicken Sie in der **Systemsteuerung** auf **Verwaltung**.
2.  Doppelklicken Sie im Fenster **Verwaltung** auf **Computerverwaltung**.
3.  Erweitern Sie im Fenster **Computer Verwaltung** die Struktur **Dienste und Anwendungen** , und doppelklicken Sie auf das **WMI-Steuer** Element.
4.  Klicken Sie mit der rechten Maustaste auf das Symbol **WMI-Steuerung** , und wählen Sie **Eigenschaften**

Im folgenden Verfahren wird beschrieben, wie Sie das WMI-Steuerelement verwenden, um die Sicherheit für einen Namespace als Vorlage einzurichten. Anschließend können Sie die Sicherheitseinstellungen Programm gesteuert abrufen, um die Sicherheit für andere Namespaces festzulegen.

**So legen Sie die Namespace Sicherheit mit dem WMI-Steuerelement fest**

1.  Erstellen Sie einen neuen Namespace mit dem MOF-Code (Managed Object Format).
2.  Führen Sie das WMI-Steuerelement aus, um die Sicherheit für den neuen Namespace festzulegen. Klicken Sie im **Startmenü** auf **Ausführen** , und geben Sie **Wmimgmt. msc** ein, oder untersuchen Sie [das WMI-Steuer](#)Element.
3.  Klicken Sie im **WMI-Steuerungs** Bereich mit der rechten Maustaste auf **WMI-Steuerung**, wählen Sie **Eigenschaften** aus, und wählen Sie dann die Registerkarte **Sicherheit** aus.
4.  Navigieren Sie zum neuen Namespace, klicken Sie auf **Sicherheit**, und konfigurieren Sie dann Gruppen und Berechtigungen für den Namespace.

Sie können auch Windows-Verwaltungsinstrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) verwenden, um die Namespace Sicherheit festzulegen. Weitere Informationen finden Sie unter [**WMIC**](wmic.md).

## <a name="setting-the-default-namespace-for-scripts"></a>Festlegen des Standard Namespace für Skripts

Wenn ein Skript beim Herstellen einer Verbindung mit WMI nicht explizit eine Verbindung mit einem Namespace herstellt, verwendet WMI den Standard Namespace, der in diesem Steuerelement angegeben ist. Der Standardwert ist auch wie folgt im Registrierungs Eintrag zu finden:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

Da der Standard Namespace leicht geändert werden kann, entweder mit diesem Steuerelement oder Programm gesteuert durch Aufrufen von Methoden von [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), geben Sie den Namespace an, wenn Sie eine Verbindung mit WMI herstellen, indem Sie entweder über den [Moniker](constructing-a-moniker-string.md) oder Aufrufe an " [**Swap. ConnectServer**](swbemlocator-connectserver.md)" eine Verbindung mit WMI Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md) .

**So legen Sie den Standard Namespace für Skripts fest**

1.  Wählen Sie im Fenster **Eigenschaften von WMI-Steuerung** die Registerkarte **erweitert** aus.
2.  Klicken Sie auf die Schaltfläche **ändern** , und wählen Sie den Namespace aus, um die Standardeinstellung

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Namespace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
