---
description: Veranschaulicht die Verwendung der VSS-Schnittstellen zum Erstellen eines VSS-Hardwareanbieters.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: VssSampleProvider-Tool und -Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd84288f6dc878c103f639aa0c015a3e5e95bde
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884412"
---
# <a name="vsssampleprovider-tool-and-sample"></a>VssSampleProvider-Tool und -Beispiel

Veranschaulicht die Verwendung der VSS-Schnittstellen [zum](volume-shadow-copy-api-interfaces.md) Erstellen eines VSS-Hardwareanbieters.

> [!Note]  
> Das VssSampleProvider-Tool und das Beispiel sind im Microsoft Windows Software Development Kit (SDK) enthalten. Sie können das Windows SDK aus Windows [Software Development Kit (SDK) für Windows 8.](https://developer.microsoft.com/windows/downloads/windows-8-sdk)

 

In der Windows SDK-Installation finden Sie das VssSampleProvider-Tool unter `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).

> [!Note]  
> Hardwareanbieter werden nur unter Windows Serverbetriebssystemen unterstützt. Auf einem Windows Client-Betriebssystem können Sie das VssSampleProvider-Beispiel kompilieren, aber nicht als Hardwareanbieter registrieren.

 

Das VssSampleProvider-Tool besteht aus den folgenden Dateien:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

Das VssSampleProvider-Beispiel enthält die folgenden Installations- und Deinstallationsskripts:

-   Install-sampleprovider.cmd
-   Uninstall-sampleprovider.cmd
-   Registrieren \_app.vbs

**So installieren und verwenden Sie das VssSampleProvider-Beispiel**

1.  Navigieren Sie zum Verzeichnis `Program Files (x86)\Windows Kits\8.0\bin\`. Dieses Verzeichnis enthält virtualstoragevss.sys und vstorcontrol.exe.
2.  Öffnen Sie ein Eingabeaufforderungsfenster im angegebenen Verzeichnis.
3.  Geben Sie zum Installieren des virtuellen Speichertreibers im Eingabeaufforderungsfenster den folgenden Befehl ein:

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  Geben Sie zum Installieren des VSS-Beispielanbieters im Eingabeaufforderungsfenster den folgenden Befehl ein:

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  Gehen Sie wie folgt vor, um eine virtuelle LUN zu erstellen.

    1.  Geben Sie im Fenster der Eingabeaufforderung folgenden Befehl ein:

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        Mit diesem Befehl wird eine virtuelle LUN erstellt, deren Speicherbezeichner **VSS Sample HW Provider ist.** Wiederholen Sie diesen Schritt, um zusätzliche virtuelle LUNs zu erstellen.

        Der VSS-Beispielanbieter erkennt eine LUN nur, wenn der **VSS-Beispiel-HW-Anbieter** Teil des Speicherbezeichners ist. Weitere Informationen zur Speicher-ID finden Sie im folgenden Blogbeitrag.

        [LUN: Erneutes Synchronisieren mit Diskshadow und virtual Storage](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  Verwenden Sie im Eingabeaufforderungsfenster diskpart.exe, um den virtuellen Datenträger zu formatieren und ihm einen Laufwerkbuchstaben zu zuweisen.

        Hier sehen Sie ein Beispielskript, das an der Diskpart-Eingabeaufforderung ausgeführt werden soll.

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  Geben Sie zum Ausführen des Beispielanbieters im Eingabeaufforderungsfenster den folgenden Befehl ein:

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    *&lt; Laufwerk &gt;* stellt den Laufwerkbuchstaben der virtuellen LUN dar.

7.  Geben Sie zum Deinstallieren des VSS-Beispielanbieters im Eingabeaufforderungsfenster den folgenden Befehl ein:

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Geben Sie zum Deinstallieren des virtuellen Speichertreibers im Eingabeaufforderungsfenster den folgenden Befehl ein:

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



