---
description: Sie können die WMI-Skripttypbibliothek verwenden, um WMI-Skripterstellungs-API-Methoden aus Microsoft Visual Studio und in Windows Skripthost-WSF-Dateien aufrufen.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Verwenden der WMI-Skripttypbibliothek
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d53f74db0ff4b744077c4e208be52dd749c2f4f150d867c3cfc7214c0e66ae2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120770"
---
# <a name="using-the-wmi-scripting-type-library"></a>Verwenden der WMI-Skripttypbibliothek

Sie können die WMI-Skripttypbibliothek verwenden, um WMI-Skripterstellungs-API-Methoden aus Microsoft Visual Studio und in Windows Skripthost-WSF-Dateien aufrufen.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Verwenden der WMI-Skripttypbibliothek mit Microsoft Visual Studio

> [!Note]  
> Visual InterDev 6.0-Features wurden in Microsoft Visual Studio [.NET integriert.](https://msdn.microsoft.com/vstudio/default.aspx)

 

Im folgenden Verfahren wird beschrieben, wie Sie der integrierten Entwicklungsumgebung (IDE) ermöglichen, die WbemScripting-Typbibliothek zu kennen.

**So fügen Sie den Projektverweisen die WMI-Skripttypbibliothek hinzu**

1.  Wählen **Sie im Menü "Verweise** **hinzufügen Project** aus.
2.  Wählen Sie auf der Registerkarte COM des **Felds Verweis** hinzufügen die Option Microsoft WMI Scripting V1.2 Library (Microsoft WMI Scripting V1.2-Bibliothek) aus.
3.  Wenn in der Liste Verweise keine geeignete Option angezeigt wird, fügen Sie sie mithilfe von **Durchsuchen** im **Feld Verweise** hinzu. Das **Feld Verweis** hinzufügen wird geöffnet, mit dem Sie die WbemScripting-Typbibliothek suchen können. 

    Die WbemScripting-Typbibliothek befindet sich in der Datei Wbemdisp.tlb im Verzeichnis %windir% \\ System32 \\ Wbem.

4.  Wählen Sie die Datei aus, und klicken Sie auf **Öffnen**. Die Microsoft WMI Scripting V1.2-Bibliothek wird in der Liste der Verweise angezeigt. Stellen Sie sicher, dass Sie das Kontrollkästchen neben diesem Element in der Liste aktivieren.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>Verwenden der WMI-Skripttypbibliothek mit Windows Script Host 2.0

Sie können den Verweis auf **"WbemScripting.SWbemLocator"** in eine WSF-Datei des Windows-Skripthosts im Gegensatz zu einem Skript, das in Visual Basic, Scripting Edition oder anderen Skriptsprachen geschrieben wurde, enthalten. Dadurch können Sie konstante Namen anstelle von Werten verwenden. Verwenden Sie beispielsweise **WbemAuthenticationLevelPktPrivacy** anstelle des Werts 6, wenn Sie die Authentifizierung festlegen.

Skripts können mithilfe der folgenden Methoden eine Verbindung mit der Skript-API für die WMI-Typbibliothek herstellen:

-   Angeben der WbemScripting-GUID in den VBScript-Methoden [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) und [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).

    Diese Warnung Windows Skripthost, um eine Verbindung mit dem WMI-Objektsatz herzustellen.

    Im folgenden VBScript-Codebeispiel wird ein neues [**SWbemDateTime-Objekt**](swbemdatetime.md) erstellt.

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Verwenden der [Monikerzeichenfolge](constructing-a-moniker-string.md) "winmgmts:" beim Abrufen eines neuen oder vorhandenen Objekts.

    Im folgenden VBScript-Codebeispiel wird der Moniker "winmgmts:" verwendet, um die Instanz von [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) mit der **Handle-Eigenschaft** 0 (null) zu erhalten. **Handle** ist die Schlüsseleigenschaft für diese Klasse.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Verweisen auf die WMI-Typbibliothek mithilfe des <reference> -Tags des WSH 2.0-XML-Dateiformats. Wenn Sie das -Tag verwenden, muss das Tag entweder ein <reference> **uuid-Attribut** haben, dessen Wert die **GUID** der WMI-Typbibliothek ist, oder (empfohlen) ein Objektattribut, dessen Wert die **PROGID** eines der WMI-Skriptobjekte ist, die Sie erstellen können.

    Im folgenden VBScript-Codebeispiel wird die PROGID von "WbemScripting" verwendet. Um das Skript auszuführen, speichern Sie den Text in einer Datei mit der Erweiterung WSF.

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

    

-   Verwenden eines **<->-Tags** zum Erstellen eines WMI-Skriptobjekts. Sie können das **attribut id** mit dem Wert eines Namens angeben, der auf das zu erstellende WMI-Skriptobjekt verweist, und das **attribut progid** gleich der PROID des WMI-Skriptobjekts.

    Das folgende WSH-Skript zeigt den Hostnamen und die Anzahl der Prozessoren auf dem lokalen Computer an. Um das Skript auszuführen, speichern Sie den Text in einer Datei mit der Erweiterung WSF.

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

[Skripterstellungs-API für WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
