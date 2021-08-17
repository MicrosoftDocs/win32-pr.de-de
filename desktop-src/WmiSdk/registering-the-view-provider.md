---
description: WMI registriert die Ansichtsanbieter-DLL während der WMI-Installation automatisch. Sie müssen jedoch weiterhin den Ansichtsanbieter bei WMI für jeden Namespace registrieren, der Ansichtsklassen enthält.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registrieren des Ansichtsanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a119816d388e07f1f032557af1171bb2666ef02a63d959b843b99b7942a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992460"
---
# <a name="registering-the-view-provider"></a>Registrieren des Ansichtsanbieters

WMI registriert die Ansichtsanbieter-DLL während der WMI-Installation automatisch. Sie müssen jedoch weiterhin den Ansichtsanbieter bei WMI für jeden Namespace registrieren, der Ansichtsklassen enthält.

Im folgenden Verfahren wird beschrieben, wie Der Ansichtsanbieter registriert wird.

**So registrieren Sie den Ansichtsanbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) um die Implementierung des Ansichtsanbieters zu beschreiben.

    Die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) beschreibt den Namen des Anbieters und dessen Klassenbezeichner (CLSID) sowie die Standardsicherheitseinstellungen.

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

2.  Erstellen Sie eine Instanz der [**\_ \_ InstanceProviderRegistration-Klasse.**](--instanceproviderregistration.md)

    Das folgende Codebeispiel zeigt, wie Sie eine Instanz der **\_ \_ InstanceProviderRegistration-Klasse** erstellen.

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

3.  Erstellen Sie eine Instanz der [**\_ \_ MethodProviderRegistration-Klasse,**](--methodproviderregistration.md) wenn Sie über Unterstützungsmethoden für die Union-Ansichtsklasse verfügen möchten.

    Das folgende Codebeispiel zeigt, wie eine Instanz der **\_ \_ MethodProviderRegistration-Klasse** erstellt wird.

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Kompilieren Sie Ihren MOF-Code mithilfe des MOF-Compilers ([mofcomp](mofcomp.md)) oder der [**IMofCompiler-Schnittstelle.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

    Wenn Sie das zuvor aufgeführte MOF-Codebeispiel in einer Datei mit dem Namen Viewtest.mof speichern, laden Sie den MOF-Code mithilfe des Mofcomp-Befehls in den Zielnamespace. *NamespacePath* ist der Namespace, in dem Sie die Ansichtsklasseninstanz erstellen möchten.

    Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um den MOF-Code in den Zielnamespace zu laden.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

Weitere Informationen finden Sie unter [Registrieren eines Anbieters.](registering-a-provider.md)

 

 



