---
title: Anzeigen der XML-Ausgabe von WinRM-Skripts
description: Windows Remoteverwaltungsskripts geben XML anstelle von Objekten zurück. Der XML-Code hat kein lesbares Format. Sie können die Methoden der MSXML-API und der vorinstallierten XSL-Datei verwenden, um die Daten in ein lesbares Format zu transformieren.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df5c27c1fe22ae87395357aeefe681af7c041420d32b7bccbf595fab38bb060b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680020"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Anzeigen der XML-Ausgabe von WinRM-Skripts

Windows Remoteverwaltungsskripts geben XML anstelle von Objekten zurück. Der XML-Code hat kein lesbares Format. Sie können die Methoden der [MSXML-API](/previous-versions/windows/desktop/ms763742(v=vs.85)) und der vorinstallierten XSL-Datei verwenden, um die Daten in ein lesbares Format zu transformieren.

Weitere Informationen zur WinRM-XML-Ausgabe und Beispiele für unformatiertes und formatiertes XML finden Sie unter [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).

Das  Winrm-Befehlszeilentool enthält eine Transformationsdatei mit dem Namen WsmTxt.xsl, die die Ausgabe in tabellarischer Form anzeigt. Wenn Ihr Skript diese Datei an die MSXML-Methoden zur Durchführung von Tranforms liefert, wird die Ausgabe wie die Ausgabe des **Winrm-Tools** angezeigt.

**So formatieren Sie unformatierte XML-Ausgabe**

1.  Erstellen Sie das [**WSMan-Objekt**](wsman.md) und eine Sitzung.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Erstellen MSXML,die die XML-Antwortausgabe und die XSL-Transformation darstellen.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Abrufen von Daten über [**Session-Objektmethoden.**](session.md)

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Geben Sie die Antwort an die MSXML [loadXML-Methode](/previous-versions/windows/desktop/ms754585(v=vs.85)) und die [Load-Methode](/previous-versions/windows/desktop/ms762722(v=vs.85)) zum Speichern der Transformationsdatei an.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Verwenden Sie die MSXML [transformNode-Methode,](/previous-versions/windows/desktop/ms761399(v=vs.85)) und zeigen Sie die Ausgabe an oder speichern Sie sie.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

Das folgende VBScript-Codebeispiel zeigt das vollständige Skript.


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



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Hinzufügen einer portablen Unterroutine zum Transformieren von XML zu Ihren Skripts

Sie können Ihren Skripts eine Unterroutine hinzufügen, die die vorinstallierte XSL-Datei verwendet, um die unformatierte XML-Ausgabe eines WinRM-Skripts in ein tabellarisches Format zu konvertieren.

Die folgende Unterroutine verwendet Aufrufe der MSXML Skriptmethoden, um die Ausgabe an WsmTxt.xsl zu liefern.


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



Die folgende Unterroutine transformiert jede Zeile Ihrer Daten, wie im folgenden Beispiel gezeigt.


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

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows Remoteverwaltungsreferenz](windows-remote-management-reference.md)
</dt> </dl>

 

 