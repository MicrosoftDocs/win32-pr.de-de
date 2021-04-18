---
description: WMI registriert die Ansichts Anbieter-DLL während des WMI-Installationsvorgangs automatisch. Allerdings müssen Sie den Ansichts Anbieter für jeden Namespace, der Ansichts Klassen enthalten soll, bei WMI registrieren.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Der Ansichts Anbieter wird registriert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352739"
---
# <a name="registering-the-view-provider"></a>Der Ansichts Anbieter wird registriert.

WMI registriert die Ansichts Anbieter-DLL während des WMI-Installationsvorgangs automatisch. Allerdings müssen Sie den Ansichts Anbieter für jeden Namespace, der Ansichts Klassen enthalten soll, bei WMI registrieren.

Im folgenden Verfahren wird beschrieben, wie der Ansichts Anbieter registriert wird.

**So registrieren Sie den Ansichts Anbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, um die Implementierung des Ansichts Anbieters zu beschreiben.

    Die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz beschreibt den Namen des Anbieters und dessen Klassen Bezeichner (CLSID) sowie die Standard Sicherheitseinstellungen.

    Im folgenden Codebeispiel wird eine Implementierung von [**\_ \_ Win32Provider**](--win32provider.md)beschrieben.

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  Erstellen Sie eine Instanz der [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse.

    Im folgenden Codebeispiel wird gezeigt, wie eine Instanz der **\_ \_ instanceproviderregistration** -Klasse erstellt wird.

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  Erstellen Sie eine Instanz der [**\_ \_ methodproviderregistration**](--methodproviderregistration.md) -Klasse, wenn Sie die Unterstützung von Methoden der Union-Ansichts Klasse benötigen.

    Im folgenden Codebeispiel wird gezeigt, wie eine Instanz der **\_ \_ methodproviderregistration** -Klasse erstellt wird.

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Kompilieren Sie den MOF-Code mit dem MOF-[Compiler ("](mofcomp.md)MOF") oder der [**imuscompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Schnittstelle.

    Wenn Sie das zuvor aufgeführte MOF-Codebeispiel in einer Datei namens viewtest. MOF speichern, verwenden Sie den Befehl "mufcomp", um den MOF-Code in den Ziel Namespace zu laden. *NamespacePath* ist der Namespace, in dem Sie die Ansichts Klasseninstanz erstellen möchten.

    Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um den MOF-Code in den Ziel Namespace zu laden.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).

 

 



