---
description: Zeigt, wie die VSS-Schnittstellen zum Erstellen eines VSS-Hardware Anbieters verwendet werden.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Vsssampleprovider-Tool und-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345729"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Vsssampleprovider-Tool und-Beispiel

Zeigt, wie die VSS- [Schnittstellen](volume-shadow-copy-api-interfaces.md) zum Erstellen eines VSS-Hardware Anbieters verwendet werden.

> [!Note]  
> Das vsssampleprovider-Tool und-Beispiel sind im Microsoft Windows Software Development Kit (SDK) enthalten. Sie können den Windows SDK aus dem [Windows Software Development Kit (SDK) für Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)herunterladen.

 

In der Windows SDK-Installation befindet sich das Tool vsssampleprovider in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).

> [!Note]  
> Hardware Anbieter werden nur auf Windows Server-Betriebssystemen unterstützt. Unter einem Windows-Client Betriebssystem können Sie das vsssampleprovider-Beispiel kompilieren, aber Sie können es nicht als Hardware Anbieter registrieren.

 

Das Tool vsssampleprovider besteht aus den folgenden Dateien:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

Das vsssampleprovider-Beispiel enthält die folgenden Installations-und deinstalstallations Skripts:

-   Install-SampleProvider. cmd
-   Uninstall-SampleProvider. cmd
-   \_app.vbs registrieren

**So installieren und verwenden Sie das vsssampleprovider-Beispiel**

1.  Navigieren Sie zum Verzeichnis `Program Files (x86)\Windows Kits\8.0\bin\`. Dieses Verzeichnis enthält virtualstoragevss.sys und vstorcontrol.exe.
2.  Öffnen Sie ein Eingabe Aufforderungs Fenster im angegebenen Verzeichnis.
3.  Geben Sie zum Installieren des virtuellen Speicher Treibers im Eingabe Aufforderungs Fenster den folgenden Befehl ein:

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  Geben Sie zum Installieren des VSS-Beispiel Anbieters im Eingabe Aufforderungs Fenster den folgenden Befehl ein:

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  Gehen Sie folgendermaßen vor, um eine virtuelle LUN zu erstellen.

    1.  Geben Sie im Fenster der Eingabeaufforderung folgenden Befehl ein:

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        Dieser Befehl erstellt eine virtuelle LUN, deren Speicher Bezeichner **VSS-Beispiel-HW-Anbieter** ist. Um zusätzliche virtuelle LUNs zu erstellen, wiederholen Sie diesen Schritt.

        Der VSS-Beispiel Anbieter erkennt eine LUN nur, wenn der **VSS-Beispiel-HW-Anbieter** Teil des Speicher Bezeichners ist. Weitere Informationen zur Speicher Kennung finden Sie im folgenden Blogbeitrag.

        [LUN-Resync mit DiskShadow und virtuellem Speicher](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  Verwenden Sie im Eingabe Aufforderungs Fenster diskpart.exe, um den virtuellen Datenträger zu formatieren, und weisen Sie ihm einen Laufwerk Buchstaben zu.

        Hier ist ein Beispielskript, das an der DiskPart-Eingabeaufforderung ausgeführt wird.

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  Geben Sie zum Ausführen des Beispiel Anbieters im Eingabe Aufforderungs Fenster den folgenden Befehl ein:

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    *<drive>* stellt den Laufwerk Buchstaben der virtuellen LUN dar.

7.  Um den VSS-Beispiel Anbieter zu deinstallieren, geben Sie im Eingabe Aufforderungs Fenster den folgenden Befehl ein:

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Um den virtuellen Speicher Treiber zu deinstallieren, geben Sie im Eingabe Aufforderungs Fenster den folgenden Befehl ein:

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



