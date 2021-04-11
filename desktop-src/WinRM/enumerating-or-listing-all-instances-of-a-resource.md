---
title: Auflisten oder Auflisten aller Instanzen einer Ressource
description: Die Session. Enumerate-Methode ist der Windows-Remoteverwaltung Ansatz zum Abrufen aller Instanzen einer angegebenen Ressource.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209306"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a><span data-ttu-id="0b07f-103">Auflisten oder Auflisten aller Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="0b07f-103">Enumerating or Listing All Instances of a Resource</span></span>

<span data-ttu-id="0b07f-104">Die [**Session. Enumerate**](session-enumerate.md) -Methode ist der Windows-Remoteverwaltung Ansatz zum Abrufen aller Instanzen einer angegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="0b07f-104">The [**Session.Enumerate**](session-enumerate.md) method is the Windows Remote Management approach to obtaining all the instances of a specified resource.</span></span>

<span data-ttu-id="0b07f-105">Die [**Session. Enumerate**](session-enumerate.md) -Methode ruft keine Auflistung in einem [**errbewbjectset**](/windows/desktop/WmiSdk/swbemobjectset) -Objekt ab, wie z. b. ein [**SWbemService.Execquery**](/windows/desktop/WmiSdk/swbemservices-execquery) -Aufrufes mit einer [WMI-Abfrage](/windows/desktop/WmiSdk/querying-wmi) als Parameter (z `ExecQuery("SELECT * from Win32_LogicalDisk")` . b.) oder ein Aufrufen einer Methode wie z. b. " [**errbemubject. Instance \_**](/windows/desktop/WmiSdk/swbemobject-instances-)".</span><span class="sxs-lookup"><span data-stu-id="0b07f-105">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in a [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) object like a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) call with a [WMI query](/windows/desktop/WmiSdk/querying-wmi) as a parameter (for example, `ExecQuery("SELECT * from Win32_LogicalDisk")`), or a call to a method like [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span> <span data-ttu-id="0b07f-106">**Session. Enumerate** und die [**enumeratorobjektmethoden**](enumerator.md) ähneln dem Vorgang des [Textstream](/previous-versions//312a5kbt(v=vs.85)) -Skript Objekts, das zum Lesen von Dateien als Datenstrom verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b07f-106">**Session.Enumerate** and the [**Enumerator**](enumerator.md) object methods are much more similar to the operation of the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object that is used for reading files as a stream.</span></span>

<span data-ttu-id="0b07f-107">Um Dateien als Textstream zu lesen, müssen Sie das Skript- [Textstream](/previous-versions//312a5kbt(v=vs.85)) -Objekt erstellen und die [Textstream. read line](/previous-versions//h7se9d4f(v=vs.85)) -Methode zum Lesen der einzelnen Zeilen der Datei aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b07f-107">To read files as a text stream, you must create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="0b07f-108">Auf ähnliche Weise können Sie die [**Session. Enumerate**](session-enumerate.md) -Methode zum Abrufen eines [**Enumeratorobjekts**](enumerator.md) und zum Abrufen der [**Enumerator. ReadItem**](enumerator-readitem.md) -Methode zum Abrufen des nächsten Elements aufruft.</span><span class="sxs-lookup"><span data-stu-id="0b07f-108">In a similar way, you can call the [**Session.Enumerate**](session-enumerate.md) method to obtain an [**Enumerator**](enumerator.md) object and call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to get the next item.</span></span> <span data-ttu-id="0b07f-109">Wie beim Lesen aus der Textdatei können Sie auch die [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) -Eigenschaft aufzurufen, um zu überprüfen, ob Sie das Ende der Datenelemente erreicht haben.</span><span class="sxs-lookup"><span data-stu-id="0b07f-109">As is the case when reading from the text file, you can call the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

<span data-ttu-id="0b07f-110">**So zählen Sie eine Ressource auf**</span><span class="sxs-lookup"><span data-stu-id="0b07f-110">**To enumerate a resource**</span></span>

1.  <span data-ttu-id="0b07f-111">Erstellen Sie eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0b07f-111">Create a session.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  <span data-ttu-id="0b07f-112">Erstellen Sie den URI, um die Ressource zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0b07f-112">Construct the URI to identify the resource.</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  <span data-ttu-id="0b07f-113">Ruft die [**Session. Enumerate**](session-enumerate.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="0b07f-113">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="0b07f-114">Dieser Befehl startet eine Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0b07f-114">This call starts an enumeration.</span></span> <span data-ttu-id="0b07f-115">In WinRM erhält ein Enumerationsvorgang eine Auflistung nicht auf dieselbe Weise wie WMI.</span><span class="sxs-lookup"><span data-stu-id="0b07f-115">In WinRM, an enumeration operation does not obtain a collection in the same way that WMI does.</span></span> <span data-ttu-id="0b07f-116">Stattdessen stellt die **Session. Enumerate** -Methode einen WS-Management protokollenumerationskontext her, der im [**Enumeratorobjekt**](enumerator.md) verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="0b07f-116">Instead, the **Session.Enumerate** method establishes a WS-Management protocol enumeration context that is maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  <span data-ttu-id="0b07f-117">Rufen Sie die [**Enumerator. ReadItem**](enumerator-readitem.md) -Methode auf, um das nächste Element der Ergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b07f-117">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="0b07f-118">In WS-Management-Protokoll entspricht dies dem Pull-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0b07f-118">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="0b07f-119">Verwenden Sie die [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) -Methode als Steuerelement, um zu erfahren, wann der Lesevorgang beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b07f-119">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

<span data-ttu-id="0b07f-120">Das folgende VBScript-Codebeispiel zeigt das komplette Skript.</span><span class="sxs-lookup"><span data-stu-id="0b07f-120">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="0b07f-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b07f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b07f-122">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="0b07f-122">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="0b07f-123">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="0b07f-123">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="0b07f-124">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="0b07f-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 