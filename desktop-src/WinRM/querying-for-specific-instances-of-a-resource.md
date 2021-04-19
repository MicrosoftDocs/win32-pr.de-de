---
title: Abfragen für bestimmte Instanzen einer Ressource
description: Der aufzurufende "Session. Enumerate" verfügt über optionale Parameter, die die Enumeration in eine Abfrage eingrenzen.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342345"
---
# <a name="querying-for-specific-instances-of-a-resource"></a><span data-ttu-id="7319e-103">Abfragen für bestimmte Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="7319e-103">Querying for Specific Instances of a Resource</span></span>

<span data-ttu-id="7319e-104">Der aufzurufende " [**Session. Enumerate**](session-enumerate.md) " verfügt über optionale Parameter, die die Enumeration in eine Abfrage eingrenzen.</span><span class="sxs-lookup"><span data-stu-id="7319e-104">The call to [**Session.Enumerate**](session-enumerate.md) has optional parameters that narrow the enumeration into a query.</span></span> <span data-ttu-id="7319e-105">Da die [WinRM-Skript-API](winrm-scripting-api.md) und die [WinRM-C++-API](winrm-c---api.md) eng auf dem zugrunde liegenden WS-Management Protokoll modelliert sind, verwenden die Parameter dieselbe Terminologie für Abfragen wie das Protokoll –*Filter* und den *Filter Dialekt*.</span><span class="sxs-lookup"><span data-stu-id="7319e-105">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) are closely modeled on the underlying WS-Management protocol, the parameters use the same terminology for querying as the protocol—*filter* and *filter dialect*.</span></span>

<span data-ttu-id="7319e-106">Sie können entweder den Filter-und den Dialekt Parameter von [**Session. Enumerate**](session-enumerate.md) verwenden, oder Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt und die [**addselector**](resourcelocator-addselector.md) -Methode erstellen und bereitstellen, aber Sie können nicht beides tun.</span><span class="sxs-lookup"><span data-stu-id="7319e-106">You can either use the filter and dialect parameters of [**Session.Enumerate**](session-enumerate.md) or you can construct and supply a [**ResourceLocator**](resourcelocator.md) object and the [**AddSelector**](resourcelocator-addselector.md) method, but you cannot do both.</span></span>

<span data-ttu-id="7319e-107">Diese Prozedur führt eine Abfrage für Netzwerkadapter aus, bei denen TCP/IP gebunden und aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7319e-107">This procedure executes a query for network adapters that have TCP/IP bound and enabled.</span></span> <span data-ttu-id="7319e-108">Die Abfrage fordert alle Instanzen von [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) an, deren **ipabled** -Eigenschaft auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7319e-108">The query requests all the instances of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) that have the **IpEnabled** property set to **True**.</span></span> <span data-ttu-id="7319e-109">Die Abfrage wird wie eine einfache Enumeration behandelt, außer wenn Sie den *Filter* und den *Dialekt* hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7319e-109">Except for the addition of the *filter* and *dialect*, the query is handled like a simple enumeration.</span></span>

<span data-ttu-id="7319e-110">In diesem Beispiel wird der Ressourcen Name für die Ressourcen Konstante durch ein Sternchen "" dargestellt, \* da der Klassenname [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)bereits in der Zeichenfolge " *strinfilter* " erwähnt wird.</span><span class="sxs-lookup"><span data-stu-id="7319e-110">In this example, the resource name for the Resource constant is represented by an asterisk "\*" because the class name, [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), is already mentioned in the *strFilter* string.</span></span>

<span data-ttu-id="7319e-111">**So Fragen Sie bestimmte Instanzen einer Ressource ab**</span><span class="sxs-lookup"><span data-stu-id="7319e-111">**To query for specific instances of a resource**</span></span>

1.  <span data-ttu-id="7319e-112">Definieren Sie zum Vereinfachen des Lesens URIs als Konstanten.</span><span class="sxs-lookup"><span data-stu-id="7319e-112">For ease-of-reading, define URIs as constants.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  <span data-ttu-id="7319e-113">Erstellen Sie eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="7319e-113">Create a session.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  <span data-ttu-id="7319e-114">Erstellen Sie die Filter Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7319e-114">Construct the filter string.</span></span> <span data-ttu-id="7319e-115">Windows-Remoteverwaltung unterstützt [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) als Filter Dialekt.</span><span class="sxs-lookup"><span data-stu-id="7319e-115">Windows Remote Management supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as the filter dialect.</span></span>

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  <span data-ttu-id="7319e-116">Legen Sie alle erforderlichen [**Enumerationskonstanten**](enumeration-constants.md) im *Flags* -Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="7319e-116">Set any required [**enumeration constants**](enumeration-constants.md) in the *flags* parameter.</span></span>

    <span data-ttu-id="7319e-117">Beachten Sie, dass der WinRM-Dienst den Fehlercode Fehler zurückgibt, wenn die Flags die [**Enumerationskonstanten**](enumeration-constants.md) **wsmanflaghierarchydeepbasepropsonly** oder **wsmanflaghierarchyflache** enthalten **\_ \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="7319e-117">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then WinRM service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

5.  <span data-ttu-id="7319e-118">Ruft die [**Session. Enumerate**](session-enumerate.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="7319e-118">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="7319e-119">Dieser Befehl startet eine Enumeration.</span><span class="sxs-lookup"><span data-stu-id="7319e-119">This call starts an enumeration.</span></span> <span data-ttu-id="7319e-120">Die **Session. Enumerate** -Methode stellt einen WS-Management protokollenumerationskontext her, der im [**Enumeratorobjekt**](enumerator.md) verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="7319e-120">The **Session.Enumerate** method establishes a WS-Management protocol enumeration context, maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  <span data-ttu-id="7319e-121">Rufen Sie die [**Enumerator. ReadItem**](enumerator-readitem.md) -Methode auf, um das nächste Element der Ergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7319e-121">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="7319e-122">In WS-Management-Protokoll entspricht dies dem Pull-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7319e-122">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="7319e-123">Verwenden Sie die [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) -Methode als Steuerelement, um zu erfahren, wann der Lesevorgang beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7319e-123">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

<span data-ttu-id="7319e-124">Das folgende VBScript-Codebeispiel zeigt das komplette Skript.</span><span class="sxs-lookup"><span data-stu-id="7319e-124">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="7319e-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7319e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7319e-126">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="7319e-126">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="7319e-127">Auflisten oder Auflisten aller Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="7319e-127">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="7319e-128">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="7319e-128">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 