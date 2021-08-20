---
title: Registrieren eines Rückrufs in Visual Basic
description: Das Hinzufügen eines Rückrufs in Visual Basic sich von der in VBScript verwendeten Methode ab.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7145a6c6ef80ede3ea2fdb1fd62a2661142fb6f0a85454389fe1c09c117e5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126223"
---
# <a name="registering-a-callback-in-visual-basic"></a>Registrieren eines Rückrufs in Visual Basic

Das Hinzufügen eines Rückrufs in Visual Basic sich von der in VBScript verwendeten Methode ab. Die in VBScript verwendete **GetRef-Funktion** ist anders als die in Visual Basic. Daher muss ein Entwickler ein [**IDispatch-Objekt**](/windows/win32/api/oaidl/nn-oaidl-idispatch) erstellen, das über die Rückruffunktion als Standardmethode verfügt. Dieses Thema enthält die erforderlichen Informationen zum Entwickeln Visual Basic Anwendungen.

**So implementieren Sie diesen Rückruf in einer Anwendung**

1.  Fügen Sie Verweise auf zwei Objektbibliotheken hinzu: TLBTypes.olb und VboostTypes6.olb. Diese Objektbibliotheken werden mit dem Control Point-Beispielcode bereitgestellt.
2.  Fügen Sie einen Verweis auf Cbklib.tlb hinzu. Diese Datei definiert die Struktur der Rückruffunktion.

    Die Datei cbklib.tlb wird mithilfe der Datei cbklib.idl erstellt, die als Teil des Beispielcodes des Kontrollpunkts enthalten ist. Es wird empfohlen, den Namen dieser Datei für Rückruffunktionen zu ändern, die sich in der Struktur ihrer Parameter unterscheiden. In diesem Beispiel wird MIDL verwendet, um die Typbibliotheksdatei zu erstellen.

3.  Schreiben Sie die Rückruffunktion. Die Parameter sind identisch mit im VBScript-Beispiel unter [Registrieren eines Rückrufs.](registering-a-callback.md) In diesem Beispiel wird immer dann eine Zeichenfolge gedruckt, wenn ein Ereignis eintrifft.
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

    

4.  Fügen Sie die Rückruffunktion dem [**IUPnPService-Objekt**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) hinzu, wie im folgenden Beispiel gezeigt, oder in einem anderen Objekt wie [**IUPnPDevice Dateityp**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)mithilfe der entsprechenden Rückruftypbibliothek (cbklib.tbl).
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

    

Im folgenden Beispiel wird das [**IUPnPService-Objekt**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) an die Funktion übergeben. Die Rückruffunktion wird dann als Parameter hinzugefügt.


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a>Im Beispielcode verwendete Objektbibliotheken

In den vorherigen Beispielen und im Beispielcode des Kontrollpunkts werden einige der folgenden Objektbibliotheken verwendet:

1.  TLBTypes.olb: Diese Bibliothek definiert einige der Typbibliothekstypen und Schnittstellen, die im Beispielcode verwendet werden. Sie definiert einige der Funktionen, die in Visual Basic verwendet werden sollen, z. B. [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), die bereits in C oder C++ verfügbar sind.
2.  VboostTypes6.olb: Diese Bibliothek definiert einige Basistypen, die in TLBTypes.olb und FunctionDelegator.bas verwendet werden. Weitere Informationen zu TLBTypes finden Sie im Buch *Advanced Visual Basic 6: Power Techniques for Everyday Programs* von Curland (Addison-Wesley, Juli 2000, ISBN: 0-201-70712-8). (Dieses Buch ist in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

Der Beispielcode für den Kontrollpunkt und die folgenden Bibliotheken stehen in Zusammenhang mit diesem Abschnitt und werden benötigt, um diesen Rückruf zu implementieren. Sie finden sie mit dem Control Point-Beispielcode:

-   Cbklib.idl
-   Cbklib.tlb
-   VboostTypes6.olb
-   TLBTypes.olb
-   FunctionDelegator.bas

 

 