---
description: Ein InParameters-Objekt enthält die Parameterliste zum Aufrufen von Anbieter Methoden, wenn ein ExecMethod-Aufgabentyp verwendet wird.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Erstellen von InParameters-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864035"
---
# <a name="constructing-inparameters-objects"></a><span data-ttu-id="5b589-103">Erstellen von InParameters-Objekten</span><span class="sxs-lookup"><span data-stu-id="5b589-103">Constructing InParameters Objects</span></span>

<span data-ttu-id="5b589-104">Ein [**InParameters**](swbemmethod-inparameters.md) -Objekt enthält die Parameterliste zum Aufrufen von Anbieter Methoden, wenn ein **ExecMethod** -Aufgabentyp verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b589-104">An [**InParameters**](swbemmethod-inparameters.md) object contains the parameter list for calling provider methods when using an **ExecMethod** type of call.</span></span> <span data-ttu-id="5b589-105">Die [**MethodenSWbemObject.Execmethod \_**](swbemobject-execmethod-.md), [**SWbemObject.Execmethodasync \_**](swbemobject-execmethodasync-.md), [**SWbemServices.Execmethod**](swbemservices-execmethod.md)und [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md) erfordern alle ein **InParameters** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5b589-105">The [**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods all require an **InParameters** object.</span></span>

<span data-ttu-id="5b589-106">Im folgenden Verfahren wird beschrieben, wie ein [**InParameters**](swbemmethod-inparameters.md) -Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5b589-106">The following procedure describes how to construct an [**InParameters**](swbemmethod-inparameters.md) object.</span></span>

<span data-ttu-id="5b589-107">**So erstellen Sie den *objwbeminparameams* -Parameter**</span><span class="sxs-lookup"><span data-stu-id="5b589-107">**To construct the *objwbemInParams* parameter**</span></span>

1.  <span data-ttu-id="5b589-108">Verbindung mit WMI herstellen.</span><span class="sxs-lookup"><span data-stu-id="5b589-108">Connect to WMI.</span></span>
2.  <span data-ttu-id="5b589-109">Rufen Sie die Definition der WMI-Klasse ab, die die Methode definiert, die Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="5b589-109">Obtain the definition of the WMI class that defines the method you want to execute.</span></span>
3.  <span data-ttu-id="5b589-110">Rufen Sie ein [**InParameters**](swbemmethod-inparameters.md) -Objekt für die WMI-Klassenmethode ab, die Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="5b589-110">Obtain an [**InParameters**](swbemmethod-inparameters.md) object specific to the WMI class method you want to execute.</span></span>

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  <span data-ttu-id="5b589-111">Legen Sie die Eigenschaften der-Instanz auf die geeigneten Werte fest.</span><span class="sxs-lookup"><span data-stu-id="5b589-111">Set the properties of the instance to whatever values are appropriate.</span></span> <span data-ttu-id="5b589-112">Stellen Sie sicher, dass Sie den Schlüsseleigenschaften in der WMI-Klasse Werte geben, die die auszuführende Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="5b589-112">Be sure to give values to the key properties in the WMI class that contains the method you want to execute.</span></span>

    <span data-ttu-id="5b589-113">Wenn Sie z. b. einen Eingabeparameter mit dem Namen myinputparam auf den Wert "ABC" in einer Instanz von [**InParameters**](swbemmethod-inparameters.md) namens "Inst" festlegen möchten, sieht der Code wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="5b589-113">For example, if you want to set an input parameter named myinputparam to the value "abc" in an instance of [**InParameters**](swbemmethod-inparameters.md) called "INST", the code would look like this.</span></span>

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  <span data-ttu-id="5b589-114">Führen Sie die-Methode aus, und rufen Sie den Rückgabestatus der Methode ab, die Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b589-114">Execute the method and obtain the return status of the method you are executing.</span></span>

<span data-ttu-id="5b589-115">Das folgende Codebeispiel veranschaulicht das Einrichten des [**InParameters**](swbemmethod-inparameters.md) -Objekts, um ein neues WMI-Objekt zu erstellen, das eine Freigabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b589-115">The following code example illustrates setting up the [**InParameters**](swbemmethod-inparameters.md) object to create a new WMI object that represents a share.</span></span> <span data-ttu-id="5b589-116">Weitere Informationen zum [**OutParameters**](swbemmethod-outparameters.md) -Objekt finden Sie unter "Überprüfen von [outparameter-Objekten](parsing-outparameters-objects.md)".</span><span class="sxs-lookup"><span data-stu-id="5b589-116">For more information about the [**OutParameters**](swbemmethod-outparameters.md) object, see [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="5b589-117">In diesem Beispiel wird ein erfolgreicher Rückgabewert (0) zurückgegeben, wenn ein Ordner mit dem Namen "Share" am Speicherort "C:/Share" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5b589-117">This example returns a successful return value (0) if there is a folder named "Share" at the location "C:/Share".</span></span> <span data-ttu-id="5b589-118">In diesem Beispiel kann dieser Ordner für andere Benutzer freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b589-118">This example enables this folder to be shared with other users.</span></span>


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 



