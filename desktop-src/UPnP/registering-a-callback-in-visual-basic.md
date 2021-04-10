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
# <a name="registering-a-callback-in-visual-basic"></a>Registrieren eines Rückrufs in Visual Basic

Das Hinzufügen eines Rückrufs in Visual Basic unterscheidet sich von der in VBScript verwendeten Methode. Die in VBScript verwendete **getref** -Funktion unterscheidet sich von der in Visual Basic verwendeten Funktion. Daher muss ein Entwickler ein [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Objekt erstellen, das über die Rückruffunktion als Standardmethode verfügt. Dieses Thema enthält die erforderlichen Informationen für die Entwicklung von Visual Basic-Anwendungen.

**So implementieren Sie diesen Rückruf in einer Anwendung**

1.  Fügen Sie Verweise auf zwei Objektbibliotheken hinzu: tlbtypes. olb und VboostTypes6. olb. Diese Objektbibliotheken werden mit dem Steuerungspunkt-Beispielcode bereitgestellt.
2.  Fügen Sie einen Verweis auf "cbklib. tlb" hinzu. Diese Datei definiert die Struktur der Rückruffunktion.

    Der cbklib. tlb wird mithilfe der Datei cbklib. idl erstellt, die als Teil des Beispielcodes für den Steuerungspunkt enthalten ist. Es wird empfohlen, den Namen dieser Datei für Rückruf Funktionen zu ändern, die sich in der Struktur ihrer Parameter unterscheiden. In diesem Beispiel wird die Typbibliotheks Datei mithilfe von "Mittel l" erstellt.

3.  Schreiben Sie die Rückruffunktion. Die Parameter sind identisch mit denen im VBScript-Beispiel beim [Registrieren eines Rückrufs](registering-a-callback.md). In diesem Beispiel wird eine Zeichenfolge ausgegeben, wenn ein Ereignis eintrifft.
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

    

4.  Fügen Sie die Rückruffunktion dem [**iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) -Objekt hinzu, wie im folgenden Beispiel gezeigt, oder in einem anderen Objekt, wie z. b. [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), mithilfe der entsprechenden Rückruf-Typbibliothek (cbklib. tbl).
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

    

Im folgenden Beispiel wird das [**iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) -Objekt an die Funktion übergeben. Die Rückruffunktion wird dann als-Parameter hinzugefügt.


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a>Im Beispiel Code verwendete Objektbibliotheken

In den vorherigen Beispielen und im Beispielcode für den Steuerungspunkt werden einige der folgenden Objektbibliotheken verwendet:

1.  Tlbtypes. olb – diese Bibliothek definiert einige der Typbibliotheks Typen und-Schnittstellen, die im Beispielcode verwendet werden. Dabei werden einige der Funktionen definiert, die in Visual Basic verwendet werden sollen, z. b. [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), die bereits in C oder C++ verfügbar sind.
2.  VboostTypes6. olb – diese Bibliothek definiert einige Basis Typen, die in tlbtypes. olb und functiondelegator. Bas verwendet werden. Weitere Informationen zu tlbtypes finden Sie im Buch *Advanced Visual Basic 6: Power Techniken for Everyday programs*, Matthew currland (Addison-Wesley, July 2000, ISBN: 0-201-70712-8). (Dieses Buch ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)

Der Beispielcode für den Steuerungspunkt und die folgenden Bibliotheken sind mit diesem Abschnitt verknüpft und sind zum Implementieren dieses Rückrufs erforderlich. Sie finden Sie mit dem Beispielcode für den Steuerungspunkt:

-   Cbklib. idl
-   Cbklib. tlb
-   VboostTypes6. olb
-   Tlbtypes. olb
-   Functiondelegator. Bas

 

 