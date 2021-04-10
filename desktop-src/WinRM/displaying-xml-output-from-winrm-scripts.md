---
title: Anzeigen der XML-Ausgabe von WinRM-Skripts
description: Windows-Remoteverwaltung Skripts geben XML anstelle von-Objekten zurück. Der XML-Code ist nicht in einem lesbaren Format. Sie können die Methoden der MSXML-API und der vorinstallierten XSL-Datei verwenden, um die Daten in ein lesbares Format umzuwandeln.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039383"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Anzeigen der XML-Ausgabe von WinRM-Skripts

Windows-Remoteverwaltung Skripts geben XML anstelle von-Objekten zurück. Der XML-Code ist nicht in einem lesbaren Format. Sie können die Methoden der [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) -API und der vorinstallierten XSL-Datei verwenden, um die Daten in ein lesbares Format umzuwandeln.

Weitere Informationen zur WinRM-XML-Ausgabe und Beispiele für unformatierte und formatierte XML-Daten finden Sie unter [Scripting in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md).

Das **WinRM** -Befehlszeilen Tool enthält eine Transformations Datei mit dem Namen "WsmTxt. xsl", die die Ausgabe in tabellarischer Form anzeigt. Wenn Ihr Skript diese Datei den MSXML-Methoden bereitstellt, die tranforms ausführen, wird die Ausgabe mit der Ausgabe des **WinRM** -Tools angezeigt.

**So formatieren Sie XML-Rohdaten**

1.  Erstellen Sie das [**WSMAN**](wsman.md) -Objekt, und erstellen Sie eine Sitzung.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Erstellen Sie MSXML-Objekte, die die XML-Antwort Ausgabe und die XSL-Transformation darstellen.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Abrufen von Daten über [**Sitzungs**](session.md) Objektmethoden.

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Geben Sie die Antwort auf die "MSXML [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) "-Methode und die [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) -Methode zum Speichern der Transformations Datei an.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Verwenden Sie die MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) -Methode, um die Ausgabe anzuzeigen oder zu speichern.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

Das folgende VBScript-Codebeispiel zeigt das komplette Skript.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Hinzufügen einer portablen Unterroutine zum Transformieren von XML in Ihre Skripts

Sie können den Skripts, die die vorinstallierte XSL-Datei verwenden, eine Unterroutine hinzufügen, um die unformatierte XML-Ausgabe eines WinRM-Skripts in ein tabellarisches Formular zu konvertieren.

Die folgende Unterroutine verwendet Aufrufe der MSXML-Skript Methoden, um die Ausgabe an WsmTxt. xsl bereitzustellen.


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



Die folgende Unterroutine transformiert jede Zeile der Daten, wie im folgenden Beispiel gezeigt.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> </dl>

 

 