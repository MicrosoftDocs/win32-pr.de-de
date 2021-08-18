---
description: Das WMI-Steuerelement ist ein MMC-Snap-In im Systemsteuerung und wird verwendet, um die WMI-Namespacesicherheit manuell auf einem lokalen Computer festzulegen. Sie können auch den Standardnamespace für die Skripterstellung festlegen.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Festlegen der Namespacesicherheit mit dem WMI-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97971e09897f8fa744f72d5ad0da59dc2292ebe7ceb88f6500e3c30e124db0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992350"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>Festlegen der Namespacesicherheit mit dem WMI-Steuerelement

Das WMI-Steuerelement ist ein MMC-Snap-In im **Systemsteuerung** und wird verwendet, um die WMI-Namespacesicherheit manuell auf einem lokalen Computer festzulegen. Sie können auch den Standardnamespace für die Skripterstellung festlegen.


Im folgenden Verfahren wird beschrieben, wie Sie das WMI-Steuerelement suchen.

**So suchen Sie das WMI-Steuerelement**

1.  Doppelklicken Sie **im Systemsteuerung** auf **Verwaltung.**
2.  Doppelklicken Sie im Fenster **Verwaltung** auf **Computerverwaltung**.
3.  Erweitern Sie im Fenster **Computerverwaltung** die Struktur **Dienste und Anwendungen,** und doppelklicken Sie auf das **WMI-Steuerelement**.
4.  Klicken Sie mit der rechten Maustaste auf das **WMI-Steuerelementsymbol,** und wählen Sie **Eigenschaften** aus.

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe des WMI-Steuerelements die Sicherheit für einen Namespace als Vorlage einrichten und dann programmgesteuert die Sicherheitseinstellungen abrufen, um die Sicherheit für andere Namespaces festzulegen.

**So legen Sie die Namespacesicherheit mit dem WMI-Steuerelement fest**

1.  Erstellen Sie einen neuen Namespace mithilfe von mof-Code (Managed Object Format).
2.  Führen Sie das WMI-Steuerelement aus, um die Sicherheit für den neuen Namespace festzulegen. Klicken Sie im **Menü Start** auf **Ausführen,** und geben Sie **wmimgmt.msc** ein. Weitere Informationen finden Sie unter [Suchen des WMI-Steuerelements.](#)
3.  Klicken Sie im **Bereich WMI-Steuerung** mit der rechten Maustaste auf **WMI-Steuerelement,** wählen Sie **Eigenschaften** und dann die Registerkarte **Sicherheit** aus.
4.  Navigieren Sie zum neuen Namespace, klicken Sie auf **Sicherheit**, und konfigurieren Sie dann Gruppen und Berechtigungen für den Namespace.

Sie können auch Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) verwenden, um die Namespacesicherheit festzulegen. Weitere Informationen finden Sie unter [**wmic**](wmic.md).

## <a name="setting-the-default-namespace-for-scripts"></a>Festlegen des Standardnamespace für Skripts

Wenn ein Skript beim Herstellen einer Verbindung mit WMI nicht explizit eine Verbindung mit einem Namespace herstellt, verwendet WMI den in diesem Steuerelement angegebenen Standardnamespace. Der Standardwert befindet sich auch im Registrierungseintrag wie folgt:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

Da der Standardnamespace einfach geändert werden kann, entweder mit diesem Steuerelement oder programmgesteuert durch Aufrufen von Methoden von [**StdRegProv,**](/previous-versions/windows/desktop/regprov/stdregprov)geben Sie den Namespace an, wenn eine Verbindung mit WMI entweder über den [Moniker](constructing-a-moniker-string.md) oder durch Aufrufe von [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md)hergestellt wird. Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts.](creating-a-wmi-script.md)

**So legen Sie den Standardnamespace für Skripts fest**

1.  Wählen Sie im Fenster **WMI-Steuerelementeigenschaften** die Registerkarte **Erweitert** aus.
2.  Klicken Sie auf die Schaltfläche **Ändern,** und wählen Sie den Namespace aus, um den Standardwert zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Namespacesicherheitsdeskriptoren](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
