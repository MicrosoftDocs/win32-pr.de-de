---
title: Registrieren eines Rückrufs in Visual Basic
description: Das Hinzufügen eines Rückrufs in Visual Basic unterscheidet sich von der in VBScript verwendeten Methode.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa754235458820a3c16eea73eec247aed90a103f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102050"
---
# <a name="registering-a-callback-in-visual-basic"></a><span data-ttu-id="29083-103">Registrieren eines Rückrufs in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="29083-103">Registering a Callback in Visual Basic</span></span>

<span data-ttu-id="29083-104">Das Hinzufügen eines Rückrufs in Visual Basic unterscheidet sich von der in VBScript verwendeten Methode.</span><span class="sxs-lookup"><span data-stu-id="29083-104">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="29083-105">Die in VBScript verwendete **getref** -Funktion unterscheidet sich von der in Visual Basic verwendeten Funktion.</span><span class="sxs-lookup"><span data-stu-id="29083-105">The **GetRef** function used in VBScript is different than the one used in Visual Basic.</span></span> <span data-ttu-id="29083-106">Daher muss ein Entwickler ein [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Objekt erstellen, das über die Rückruffunktion als Standardmethode verfügt.</span><span class="sxs-lookup"><span data-stu-id="29083-106">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="29083-107">Dieses Thema enthält die erforderlichen Informationen für die Entwicklung von Visual Basic-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="29083-107">This topic provides the necessary information to develop Visual Basic applications.</span></span>

<span data-ttu-id="29083-108">**So implementieren Sie diesen Rückruf in einer Anwendung**</span><span class="sxs-lookup"><span data-stu-id="29083-108">**To implement this callback in an application**</span></span>

1.  <span data-ttu-id="29083-109">Fügen Sie Verweise auf zwei Objektbibliotheken hinzu: tlbtypes. olb und VboostTypes6. olb.</span><span class="sxs-lookup"><span data-stu-id="29083-109">Add references to two object libraries: TLBTypes.olb and VboostTypes6.olb.</span></span> <span data-ttu-id="29083-110">Diese Objektbibliotheken werden mit dem Steuerungspunkt-Beispielcode bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="29083-110">These object libraries are provided with the Control Point sample code.</span></span>
2.  <span data-ttu-id="29083-111">Fügen Sie einen Verweis auf "cbklib. tlb" hinzu.</span><span class="sxs-lookup"><span data-stu-id="29083-111">Add a reference to Cbklib.tlb.</span></span> <span data-ttu-id="29083-112">Diese Datei definiert die Struktur der Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="29083-112">This file defines the structure of the callback function.</span></span>

    <span data-ttu-id="29083-113">Der cbklib. tlb wird mithilfe der Datei cbklib. idl erstellt, die als Teil des Beispielcodes für den Steuerungspunkt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="29083-113">The cbklib.tlb is created using the cbklib.idl file that is included as part of the Control Point sample code.</span></span> <span data-ttu-id="29083-114">Es wird empfohlen, den Namen dieser Datei für Rückruf Funktionen zu ändern, die sich in der Struktur ihrer Parameter unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="29083-114">It is recommended that the name of this file change for callback functions that differ in the structure of their parameters.</span></span> <span data-ttu-id="29083-115">In diesem Beispiel wird die Typbibliotheks Datei mithilfe von "Mittel l" erstellt.</span><span class="sxs-lookup"><span data-stu-id="29083-115">This example uses MIDL to create the type library file.</span></span>

3.  <span data-ttu-id="29083-116">Schreiben Sie die Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="29083-116">Write the callback function.</span></span> <span data-ttu-id="29083-117">Die Parameter sind identisch mit denen im VBScript-Beispiel beim [Registrieren eines Rückrufs](registering-a-callback.md).</span><span class="sxs-lookup"><span data-stu-id="29083-117">The parameters are the same as in the VBScript example in [Registering a Callback](registering-a-callback.md).</span></span> <span data-ttu-id="29083-118">In diesem Beispiel wird eine Zeichenfolge ausgegeben, wenn ein Ereignis eintrifft.</span><span class="sxs-lookup"><span data-stu-id="29083-118">This example prints a string whenever an event arrives.</span></span>
    ```VB
    Function eventHandler(ByVal callbackType As Variant, _
    ByVal svcObj As Variant, ByVal varName As Variant, _
    ByVal value As Variant) As Long

        On Error GoTo Error
        'Write some interesting code to do actual work here

        MsgBox "Event Handler Called"
        Exit Function

    Error:
        With Err
            If .Number > 0 Then
                eventHandler = .Number Or &H800A0000
            Else
                eventHandler = .Number
            End If
        End With
    End Function
    ```

    

4.  <span data-ttu-id="29083-119">Fügen Sie die Rückruffunktion dem [**iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) -Objekt hinzu, wie im folgenden Beispiel gezeigt, oder in einem anderen Objekt, wie z. b. [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), mithilfe der entsprechenden Rückruf-Typbibliothek (cbklib. tbl).</span><span class="sxs-lookup"><span data-stu-id="29083-119">Add the callback function to the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object, as shown in the following example, or in another object such as [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), using the appropriate callback type library (cbklib.tbl).</span></span>
    ```VB
    Public Sub AddCbFunction(upnpSvc As UPnPService)

        Dim X As CallbackIUnknownLib.CallBackInterface
        Dim obj As Object
        Dim ptinfo As ITypeInfo
        Dim ptcomp As ITypeComp

        With LoadTypeLibEx(App.Path & "\cbklib.tlb", _
          REGKIND_NONE).GetTypeComp
            .BindType "CallBackInterface", 0, ptinfo, ptcomp
        End With

        'NewDelegator is defined in FunctionDelegator.bas
        Set X = NewDelegator(AddressOf eventHandler) 
        Set obj = CreateStdDispatch(Nothing, ObjPtr(X), ptinfo)
        upnpSvc.AddCallback obj
    End Sub
    ```

    

<span data-ttu-id="29083-120">Im folgenden Beispiel wird das [**iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) -Objekt an die Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="29083-120">In the following example, the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object is passed to the function.</span></span> <span data-ttu-id="29083-121">Die Rückruffunktion wird dann als-Parameter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="29083-121">The callback function is then added as the parameter.</span></span>


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a><span data-ttu-id="29083-122">Im Beispiel Code verwendete Objektbibliotheken</span><span class="sxs-lookup"><span data-stu-id="29083-122">Object Libraries Used in the Sample Code</span></span>

<span data-ttu-id="29083-123">In den vorherigen Beispielen und im Beispielcode für den Steuerungspunkt werden einige der folgenden Objektbibliotheken verwendet:</span><span class="sxs-lookup"><span data-stu-id="29083-123">The previous examples and the Control Point sample code use some of the following object libraries:</span></span>

1.  <span data-ttu-id="29083-124">Tlbtypes. olb – diese Bibliothek definiert einige der Typbibliotheks Typen und-Schnittstellen, die im Beispielcode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29083-124">TLBTypes.olb — This library defines some of the type library types and interfaces that are used in the sample code.</span></span> <span data-ttu-id="29083-125">Dabei werden einige der Funktionen definiert, die in Visual Basic verwendet werden sollen, z. b. [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), die bereits in C oder C++ verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="29083-125">It defines some of the functions to be used in Visual Basic, such as [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), that are already available in C or C++.</span></span>
2.  <span data-ttu-id="29083-126">VboostTypes6. olb – diese Bibliothek definiert einige Basis Typen, die in tlbtypes. olb und functiondelegator. Bas verwendet werden. Weitere Informationen zu tlbtypes finden Sie im Buch *Advanced Visual Basic 6: Power Techniken for Everyday programs*, Matthew currland (Addison-Wesley, July 2000, ISBN: 0-201-70712-8).</span><span class="sxs-lookup"><span data-stu-id="29083-126">VboostTypes6.olb — This library defines some base types which are used in TLBTypes.olb and FunctionDelegator.bas. Further information regarding TLBTypes can be found in the book *Advanced Visual Basic 6: Power Techniques for Everyday Programs*, by Matthew Curland (Addison-Wesley, July 2000, ISBN: 0-201-70712-8).</span></span> <span data-ttu-id="29083-127">(Dieses Buch ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="29083-127">(This book may not be available in some languages and countries.)</span></span>

<span data-ttu-id="29083-128">Der Beispielcode für den Steuerungspunkt und die folgenden Bibliotheken sind mit diesem Abschnitt verknüpft und sind zum Implementieren dieses Rückrufs erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29083-128">The Control Point sample code and the following libraries are related to this section and are needed to implement this callback.</span></span> <span data-ttu-id="29083-129">Sie finden Sie mit dem Beispielcode für den Steuerungspunkt:</span><span class="sxs-lookup"><span data-stu-id="29083-129">They can be found with the Control Point sample code:</span></span>

-   <span data-ttu-id="29083-130">Cbklib. idl</span><span class="sxs-lookup"><span data-stu-id="29083-130">Cbklib.idl</span></span>
-   <span data-ttu-id="29083-131">Cbklib. tlb</span><span class="sxs-lookup"><span data-stu-id="29083-131">Cbklib.tlb</span></span>
-   <span data-ttu-id="29083-132">VboostTypes6. olb</span><span class="sxs-lookup"><span data-stu-id="29083-132">VboostTypes6.olb</span></span>
-   <span data-ttu-id="29083-133">Tlbtypes. olb</span><span class="sxs-lookup"><span data-stu-id="29083-133">TLBTypes.olb</span></span>
-   <span data-ttu-id="29083-134">Functiondelegator. Bas</span><span class="sxs-lookup"><span data-stu-id="29083-134">FunctionDelegator.bas</span></span>

 

 