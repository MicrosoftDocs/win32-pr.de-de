---
description: Ein Klassenobjektpfad beschreibt den Speicherort einer Klasse innerhalb eines Namespace.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Beschreiben eines Klassenobjektpfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6801d91c4236a7892d7db121dc02c73d93640b7dbc4969c86db55a8789b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244400"
---
# <a name="describing-a-class-object-path"></a>Beschreiben eines Klassenobjektpfads

Ein Klassenobjektpfad beschreibt den Speicherort einer Klasse innerhalb eines Namespace.

Sie können die folgenden Methoden verwenden, um einen Objektpfad anzugeben:

-   Ein vollständiger Objektpfad zu einer Klasse fügt den Klassennamen an einen Namespacepfad an.

    Das folgende Beispiel zeigt den Speicherort der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) im \\ Cimv2-Stammnamespace auf \\ dem Server mit dem Namen Admin.

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   Ein relativer Objektpfad stellt eine Klasse dar, die sich im aktuellen Namespace befindet. Ein relativer Objektpfad zu einer Klasse enthält nur den Klassennamen.

    Das folgende Beispiel zeigt den relativen Pfad zur [**Win32 \_ LogicalDisk-Klasse.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)

    ``` syntax
    Win32_LogicalDisk
    ```

Wenn Sie einen Klassennamen abfragen, aber keine Instanzen angeben, gibt WMI die Klassendefinition zurück. Im folgenden Verfahren wird beschrieben, wie eine Klassendefinition in VBScript abgerufen wird.

**So rufen Sie eine Klassendefinition in VBScript ab**

-   Sie können die Monikerverbindung entweder mit einer Abfrage oder [**mit GetObject verwenden.**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) Sie können auch [**SWbemServices.Get verwenden.**](swbemservices-get.md)

    Das folgende Beispiel zeigt, wie [GetObject verwendet](/previous-versions//kdccchxa(v=vs.85)) wird, um eine Klassendefinition zu erhalten.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    Das folgende Beispiel zeigt, wie eine Klassendefinition abfragen kann.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

Sie können eine Klassendefinition in C++ abrufen, indem Sie nur den Klassennamen und keinen Pfad zu einer bestimmten Instanz angeben. Im folgenden Verfahren wird beschrieben, wie eine Klassendefinition in C++ abgerufen wird.

**So rufen Sie eine Klassendefinition in C++ ab**

-   Rufen Sie die [**Funktionen IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) auf.

    Das folgende Beispiel zeigt, wie sie die [**IWbemServices::GetObject-Funktion**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) aufruft.

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    Für das vorherige Codebeispiel ist die folgende \# include-Anweisung erforderlich, um ordnungsgemäß zu kompilieren.

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
