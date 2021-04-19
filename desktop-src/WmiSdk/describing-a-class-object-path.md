---
description: Ein Klassenobjekt Pfad beschreibt den Speicherort einer Klasse innerhalb eines Namespace.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Beschreiben eines Klassenobjekt Pfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362381"
---
# <a name="describing-a-class-object-path"></a>Beschreiben eines Klassenobjekt Pfads

Ein Klassenobjekt Pfad beschreibt den Speicherort einer Klasse innerhalb eines Namespace.

Mit den folgenden Methoden können Sie einen Objekt Pfad angeben:

-   Ein vollständiger Objekt Pfad zu einer Klasse fügt den Klassennamen an einen Namespace Pfad an.

    Im folgenden Beispiel wird der Speicherort der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse im \\ root \\ CIMV2-Namespace auf dem Server mit dem Namen admin gezeigt.

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   Ein relativer Objekt Pfad stellt eine Klasse dar, die sich im aktuellen Namespace befindet. Ein relativer Objekt Pfad zu einer Klasse enthält nur den Klassennamen.

    Das folgende Beispiel zeigt den relativen Pfad zur [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse.

    ``` syntax
    Win32_LogicalDisk
    ```

Wenn Sie einen Klassennamen Abfragen, aber keine Instanzen angeben, gibt WMI die Klassendefinition zurück. Im folgenden Verfahren wird beschrieben, wie eine Klassendefinition in VBScript abgerufen wird.

**So rufen Sie eine Klassendefinition in VBScript ab**

-   Sie können die monikerverbindung entweder mit einer Abfrage oder einem [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx)-Objekt verwenden. Sie können auch " [**Swap Services. Get**](swbemservices-get.md)" verwenden.

    Im folgenden Beispiel wird gezeigt, wie [GetObject](/previous-versions//kdccchxa(v=vs.85)) verwendet wird, um eine Klassendefinition zu erhalten.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    Im folgenden Beispiel wird gezeigt, wie eine-Klassendefinition abgefragt wird.

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

-   Aufrufen der Funktionen [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    Im folgenden Beispiel wird gezeigt, wie die [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Funktion aufgerufen wird.

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    Das vorherige Codebeispiel erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
