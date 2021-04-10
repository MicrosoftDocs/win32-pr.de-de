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
# <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="4c84a-105">Anzeigen der XML-Ausgabe von WinRM-Skripts</span><span class="sxs-lookup"><span data-stu-id="4c84a-105">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="4c84a-106">Windows-Remoteverwaltung Skripts geben XML anstelle von-Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="4c84a-106">Windows Remote Management scripts return XML rather than objects.</span></span> <span data-ttu-id="4c84a-107">Der XML-Code ist nicht in einem lesbaren Format.</span><span class="sxs-lookup"><span data-stu-id="4c84a-107">The XML is not in a human-readable format.</span></span> <span data-ttu-id="4c84a-108">Sie können die Methoden der [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) -API und der vorinstallierten XSL-Datei verwenden, um die Daten in ein lesbares Format umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="4c84a-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API and the preinstalled XSL file to transform the data into human-readable format.</span></span>

<span data-ttu-id="4c84a-109">Weitere Informationen zur WinRM-XML-Ausgabe und Beispiele für unformatierte und formatierte XML-Daten finden Sie unter [Scripting in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="4c84a-109">For more information about WinRM XML output and examples of raw and formatted XML, see [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="4c84a-110">Das **WinRM** -Befehlszeilen Tool enthält eine Transformations Datei mit dem Namen "WsmTxt. xsl", die die Ausgabe in tabellarischer Form anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4c84a-110">The **Winrm** command-line tool comes with a transform file named WsmTxt.xsl that displays output in a tabular form.</span></span> <span data-ttu-id="4c84a-111">Wenn Ihr Skript diese Datei den MSXML-Methoden bereitstellt, die tranforms ausführen, wird die Ausgabe mit der Ausgabe des **WinRM** -Tools angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c84a-111">If your script supplies this file to the MSXML methods that perform tranforms, the output appears the same as the output from the **Winrm** tool.</span></span>

<span data-ttu-id="4c84a-112">**So formatieren Sie XML-Rohdaten**</span><span class="sxs-lookup"><span data-stu-id="4c84a-112">**To format raw XML output**</span></span>

1.  <span data-ttu-id="4c84a-113">Erstellen Sie das [**WSMAN**](wsman.md) -Objekt, und erstellen Sie eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4c84a-113">Create the [**WSMan**](wsman.md) object and create a session.</span></span>

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  <span data-ttu-id="4c84a-114">Erstellen Sie MSXML-Objekte, die die XML-Antwort Ausgabe und die XSL-Transformation darstellen.</span><span class="sxs-lookup"><span data-stu-id="4c84a-114">Create MSXML objects that represent the XML response output and the XSL transform.</span></span>

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  <span data-ttu-id="4c84a-115">Abrufen von Daten über [**Sitzungs**](session.md) Objektmethoden.</span><span class="sxs-lookup"><span data-stu-id="4c84a-115">Obtain data through [**Session**](session.md) object methods.</span></span>

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  <span data-ttu-id="4c84a-116">Geben Sie die Antwort auf die "MSXML [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) "-Methode und die [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) -Methode zum Speichern der Transformations Datei an.</span><span class="sxs-lookup"><span data-stu-id="4c84a-116">Supply the response to the MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) method and the [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) method to store the transform file.</span></span>

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  <span data-ttu-id="4c84a-117">Verwenden Sie die MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) -Methode, um die Ausgabe anzuzeigen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4c84a-117">Use the MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) method and display or save the output.</span></span>

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

<span data-ttu-id="4c84a-118">Das folgende VBScript-Codebeispiel zeigt das komplette Skript.</span><span class="sxs-lookup"><span data-stu-id="4c84a-118">The following VBScript code example shows the complete script.</span></span>


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



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a><span data-ttu-id="4c84a-119">Hinzufügen einer portablen Unterroutine zum Transformieren von XML in Ihre Skripts</span><span class="sxs-lookup"><span data-stu-id="4c84a-119">Adding a Portable Subroutine to Transform XML to Your Scripts</span></span>

<span data-ttu-id="4c84a-120">Sie können den Skripts, die die vorinstallierte XSL-Datei verwenden, eine Unterroutine hinzufügen, um die unformatierte XML-Ausgabe eines WinRM-Skripts in ein tabellarisches Formular zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="4c84a-120">You can add a subroutine to your scripts that uses the preinstalled XSL file to convert the raw XML output from a WinRM script to a tabular form.</span></span>

<span data-ttu-id="4c84a-121">Die folgende Unterroutine verwendet Aufrufe der MSXML-Skript Methoden, um die Ausgabe an WsmTxt. xsl bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4c84a-121">The following subroutine uses calls to the MSXML scripting methods to supply the output to WsmTxt.xsl.</span></span>


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



<span data-ttu-id="4c84a-122">Die folgende Unterroutine transformiert jede Zeile der Daten, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c84a-122">The following subroutine transforms each line of your data as shown in the following example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4c84a-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c84a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c84a-124">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="4c84a-124">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="4c84a-125">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="4c84a-125">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="4c84a-126">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="4c84a-126">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 