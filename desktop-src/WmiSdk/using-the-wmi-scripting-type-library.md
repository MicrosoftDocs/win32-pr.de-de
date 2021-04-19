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
# <a name="using-the-wmi-scripting-type-library"></a><span data-ttu-id="c4f7a-103">Verwenden der WMI-Skriptingtypbibliothek</span><span class="sxs-lookup"><span data-stu-id="c4f7a-103">Using the WMI Scripting Type Library</span></span>

<span data-ttu-id="c4f7a-104">Sie können die WMI-Skriptingtypbibliothek verwenden, um WMI-Skript-API-Methoden aus Microsoft Visual Studio und in Windows Script Host-WSF-Dateien aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-104">You can use the WMI scripting type library to call WMI Scripting API methods from Microsoft Visual Studio and in Windows Script Host WSF files.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a><span data-ttu-id="c4f7a-105">Verwenden der WMI-Skriptingtypbibliothek mit Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c4f7a-105">Using the WMI Scripting Type Library with Microsoft Visual Studio</span></span>

> [!Note]  
> <span data-ttu-id="c4f7a-106">Visual InterDev 6,0-Features wurden in [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx)integriert.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-106">Visual InterDev 6.0 features have been integrated into [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

 

<span data-ttu-id="c4f7a-107">Im folgenden Verfahren wird beschrieben, wie Sie die integrierte Entwicklungsumgebung (Integrated Development Environment, IDE) aktivieren, um die WbemScripting-Typbibliothek zu beachten.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-107">The following procedure describes how to enable the integrated development environment (IDE) to be aware of the WbemScripting type library.</span></span>

<span data-ttu-id="c4f7a-108">**So fügen Sie die WMI-Skriptingtypbibliothek zu den Projekt verweisen hinzu**</span><span class="sxs-lookup"><span data-stu-id="c4f7a-108">**To add the WMI Scripting type library to the project references**</span></span>

1.  <span data-ttu-id="c4f7a-109">Wählen Sie im Menü **Projekt** die Option **Verweise hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-109">Select **Add References** from the **Project** menu.</span></span>
2.  <span data-ttu-id="c4f7a-110">Wählen Sie auf der Registerkarte com im Feld **Verweis hinzufügen** die Option Microsoft WMI Scripting v 1.2 Library aus.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-110">In the COM tab of the **Add Reference** box, select Microsoft WMI Scripting V1.2 Library.</span></span>
3.  <span data-ttu-id="c4f7a-111">Wenn keine passende Option in der Verweis Liste angezeigt wird, fügen Sie Sie im Feld **Verweise** mithilfe von **Browse** hinzu.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-111">If no suitable option appears in the References list, add it by using **Browse** in the **References** box.</span></span> <span data-ttu-id="c4f7a-112">**Durch das Durchsuchen** wird ein Feld **Verweis hinzufügen** geöffnet, in dem Sie die WbemScripting-Typbibliothek suchen können.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-112">The **Browse** opens an **Add Reference** box that enables you to locate the WbemScripting type library.</span></span>

    <span data-ttu-id="c4f7a-113">Die WbemScripting-Typbibliothek befindet sich in der Datei wbemdisp. tlb im Verzeichnis% windir% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-113">The WbemScripting type library resides in the file Wbemdisp.tlb in the %windir%\\System32\\Wbem directory.</span></span>

4.  <span data-ttu-id="c4f7a-114">Wählen Sie die Datei aus, und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-114">Select the file and click **Open**.</span></span> <span data-ttu-id="c4f7a-115">Die Microsoft WMI Scripting v 1.2-Bibliothek wird in der Verweis Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-115">Microsoft WMI Scripting V1.2 Library appears on the references list.</span></span> <span data-ttu-id="c4f7a-116">Stellen Sie sicher, dass Sie das Kontrollkästchen neben diesem Element in der Liste aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-116">Ensure that you select the box next to this item in the list.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a><span data-ttu-id="c4f7a-117">Verwenden der WMI-Skripting-Typbibliothek mit Windows Script Host 2,0</span><span class="sxs-lookup"><span data-stu-id="c4f7a-117">Using the WMI Scripting Type Library with Windows Script Host 2.0</span></span>

<span data-ttu-id="c4f7a-118">Sie können den Verweis auf den **WbemScripting. WS-Locator** in eine Windows Script Host-WSF-Datei einschließen, im Gegensatz zu einem Skript, das in Visual Basic, Scripting Edition oder anderen Skriptsprachen geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-118">You can include the reference to the **WbemScripting.SWbemLocator** in a Windows Script Host WSF file, unlike a script written in Visual Basic, Scripting Edition or other scripting languages.</span></span> <span data-ttu-id="c4f7a-119">Dies ermöglicht es Ihnen, Konstante Namen anstelle von Werten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-119">This enables you to use constant names instead of values.</span></span> <span data-ttu-id="c4f7a-120">Verwenden Sie z. b. **wbemauthenticationlevelpktprivacy** anstelle des Werts 6, wenn Sie die Authentifizierung festlegen.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-120">For example, use **WbemAuthenticationLevelPktPrivacy** rather than the value 6 when setting authentication.</span></span>

<span data-ttu-id="c4f7a-121">Skripts können mithilfe der folgenden Methoden eine Verbindung mit der Skript-API für die WMI-Typbibliothek herstellen:</span><span class="sxs-lookup"><span data-stu-id="c4f7a-121">Scripts can connect with the Scripting API for WMI type library using the following methods:</span></span>

-   <span data-ttu-id="c4f7a-122">Angeben der WbemScripting-GUID in den VBScript-Methoden " [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) " und " [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)".</span><span class="sxs-lookup"><span data-stu-id="c4f7a-122">Specifying the WbemScripting GUID in the VBScript methods [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span></span>

    <span data-ttu-id="c4f7a-123">Dadurch wird der Windows Script Host zum Herstellen einer Verbindung mit dem WMI-Objekt Satz benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-123">This alerts Windows Script Host to connect to the WMI object set.</span></span>

    <span data-ttu-id="c4f7a-124">Im folgenden VBScript-Codebeispiel wird ein neues-Objekt vom Typ " [**Swap DateTime**](swbemdatetime.md) " erstellt.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-124">The following VBScript code example creates a new [**SWbemDateTime**](swbemdatetime.md) object.</span></span>

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   <span data-ttu-id="c4f7a-125">Verwenden der [Monikerzeichenfolge](constructing-a-moniker-string.md) "winmgmts:" beim Abrufen eines neuen oder vorhandenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-125">Using the [Moniker string](constructing-a-moniker-string.md) "winmgmts:" when obtaining a new or existing object.</span></span>

    <span data-ttu-id="c4f7a-126">Im folgenden VBScript-Codebeispiel wird der "winmgmts:"-Moniker verwendet, um die Instanz des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) mit einer **handle** -Eigenschaft von 0 (null) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-126">The following VBScript code example uses the "winmgmts:" moniker to get the instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) with a **Handle** property of 0 (zero).</span></span> <span data-ttu-id="c4f7a-127">**Handle** ist die Schlüsseleigenschaft für diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-127">**Handle** is the key property for this class.</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   <span data-ttu-id="c4f7a-128">Verweisen auf die WMI-Typbibliothek mit dem- <reference> Tag des WSH 2,0-XML-Datei Formats.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-128">Referencing the WMI type library using the <reference> tag of the WSH 2.0 XML file format.</span></span> <span data-ttu-id="c4f7a-129">Wenn Sie das- <reference> Tag verwenden, muss das-Tag entweder über ein **UUID** -Attribut verfügen, dessen Wert die **GUID** der WMI-Typbibliothek ist, oder (empfohlen) ein Objekt Attribut, dessen Wert die **ProgID** der WMI-Skript Objekte ist, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-129">If you use the <reference> tag, the tag must have either a **uuid** attribute whose value is the **GUID** of the WMI type library, or (recommended) an object attribute whose value is the **PROGID** of any of the WMI scripting objects you can create.</span></span>

    <span data-ttu-id="c4f7a-130">Im folgenden VBScript-Codebeispiel wird die ProgID von "WbemScripting" verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-130">The following VBScript code example uses the PROGID of "WbemScripting" .</span></span> <span data-ttu-id="c4f7a-131">Um das Skript auszuführen, speichern Sie den Text in einer Datei mit der Erweiterung. wsf.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-131">To run the script, save the text in a file with a .wsf extension.</span></span>

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

    

-   <span data-ttu-id="c4f7a-132">Verwenden eines <**Objekt**>-Tags, um ein WMI-Skript Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-132">Using an <**object**> tag to create a WMI scripting object.</span></span> <span data-ttu-id="c4f7a-133">Sie können das **ID** -Attribut mit dem Wert eines Namens angeben, der auf das zu erstellende WMI-Skript Objekt verweist, und das **ProgID** -Attribut, das der proid des WMI-Skript Objekts entspricht.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-133">You can specify the **id** attribute with the value of a name that references the WMI scripting object you want to create, and the **progid** attribute equal to the PROID of the WMI scripting object.</span></span>

    <span data-ttu-id="c4f7a-134">Das folgende WSH-Skript zeigt den Hostnamen und die Anzahl der Prozessoren auf dem lokalen Computer an.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-134">The following WSH script displays the hostname and the number of processors on the local computer.</span></span> <span data-ttu-id="c4f7a-135">Um das Skript auszuführen, speichern Sie den Text in einer Datei mit der Erweiterung. wsf.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-135">To run the script, save the text in a file with a .wsf extension.</span></span>

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

    

## <a name="related-topics"></a><span data-ttu-id="c4f7a-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4f7a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f7a-137">Skripterstellung in WMI</span><span class="sxs-lookup"><span data-stu-id="c4f7a-137">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[<span data-ttu-id="c4f7a-138">Skript-API für WMI</span><span class="sxs-lookup"><span data-stu-id="c4f7a-138">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
