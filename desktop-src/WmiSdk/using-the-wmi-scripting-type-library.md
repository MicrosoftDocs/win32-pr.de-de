---
description: Sie können die WMI-Skriptingtypbibliothek verwenden, um WMI-Skript-API-Methoden aus Microsoft Visual Studio und in Windows Script Host-WSF-Dateien aufzurufen.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Verwenden der WMI-Skriptingtypbibliothek
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360692"
---
# <a name="using-the-wmi-scripting-type-library"></a>Verwenden der WMI-Skriptingtypbibliothek

Sie können die WMI-Skriptingtypbibliothek verwenden, um WMI-Skript-API-Methoden aus Microsoft Visual Studio und in Windows Script Host-WSF-Dateien aufzurufen.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Verwenden der WMI-Skriptingtypbibliothek mit Microsoft Visual Studio

> [!Note]  
> Visual InterDev 6,0-Features wurden in [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx)integriert.

 

Im folgenden Verfahren wird beschrieben, wie Sie die integrierte Entwicklungsumgebung (Integrated Development Environment, IDE) aktivieren, um die WbemScripting-Typbibliothek zu beachten.

**So fügen Sie die WMI-Skriptingtypbibliothek zu den Projekt verweisen hinzu**

1.  Wählen Sie im Menü **Projekt** die Option **Verweise hinzufügen** aus.
2.  Wählen Sie auf der Registerkarte com im Feld **Verweis hinzufügen** die Option Microsoft WMI Scripting v 1.2 Library aus.
3.  Wenn keine passende Option in der Verweis Liste angezeigt wird, fügen Sie Sie im Feld **Verweise** mithilfe von **Browse** hinzu. **Durch das Durchsuchen** wird ein Feld **Verweis hinzufügen** geöffnet, in dem Sie die WbemScripting-Typbibliothek suchen können.

    Die WbemScripting-Typbibliothek befindet sich in der Datei wbemdisp. tlb im Verzeichnis% windir% \\ system32 \\ WBEM.

4.  Wählen Sie die Datei aus, und klicken Sie auf **Öffnen**. Die Microsoft WMI Scripting v 1.2-Bibliothek wird in der Verweis Liste angezeigt. Stellen Sie sicher, dass Sie das Kontrollkästchen neben diesem Element in der Liste aktivieren.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>Verwenden der WMI-Skripting-Typbibliothek mit Windows Script Host 2,0

Sie können den Verweis auf den **WbemScripting. WS-Locator** in eine Windows Script Host-WSF-Datei einschließen, im Gegensatz zu einem Skript, das in Visual Basic, Scripting Edition oder anderen Skriptsprachen geschrieben ist. Dies ermöglicht es Ihnen, Konstante Namen anstelle von Werten zu verwenden. Verwenden Sie z. b. **wbemauthenticationlevelpktprivacy** anstelle des Werts 6, wenn Sie die Authentifizierung festlegen.

Skripts können mithilfe der folgenden Methoden eine Verbindung mit der Skript-API für die WMI-Typbibliothek herstellen:

-   Angeben der WbemScripting-GUID in den VBScript-Methoden " [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) " und " [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)".

    Dadurch wird der Windows Script Host zum Herstellen einer Verbindung mit dem WMI-Objekt Satz benachrichtigt.

    Im folgenden VBScript-Codebeispiel wird ein neues-Objekt vom Typ " [**Swap DateTime**](swbemdatetime.md) " erstellt.

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Verwenden der [Monikerzeichenfolge](constructing-a-moniker-string.md) "winmgmts:" beim Abrufen eines neuen oder vorhandenen Objekts.

    Im folgenden VBScript-Codebeispiel wird der "winmgmts:"-Moniker verwendet, um die Instanz des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) mit einer **handle** -Eigenschaft von 0 (null) zu erhalten. **Handle** ist die Schlüsseleigenschaft für diese Klasse.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Verweisen auf die WMI-Typbibliothek mit dem- <reference> Tag des WSH 2,0-XML-Datei Formats. Wenn Sie das- <reference> Tag verwenden, muss das-Tag entweder über ein **UUID** -Attribut verfügen, dessen Wert die **GUID** der WMI-Typbibliothek ist, oder (empfohlen) ein Objekt Attribut, dessen Wert die **ProgID** der WMI-Skript Objekte ist, die Sie erstellen können.

    Im folgenden VBScript-Codebeispiel wird die ProgID von "WbemScripting" verwendet. Um das Skript auszuführen, speichern Sie den Text in einer Datei mit der Erweiterung. wsf.

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   Verwenden eines <**Objekt**>-Tags, um ein WMI-Skript Objekt zu erstellen. Sie können das **ID** -Attribut mit dem Wert eines Namens angeben, der auf das zu erstellende WMI-Skript Objekt verweist, und das **ProgID** -Attribut, das der proid des WMI-Skript Objekts entspricht.

    Das folgende WSH-Skript zeigt den Hostnamen und die Anzahl der Prozessoren auf dem lokalen Computer an. Um das Skript auszuführen, speichern Sie den Text in einer Datei mit der Erweiterung. wsf.

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[Skript-API für WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
