---
description: Sie können die folgenden Anweisungen verwenden, um COM+-Anwendungspoolingwerte für Ihre COM+-Anwendung zu konfigurieren.
ms.assetid: faba5cb7-745e-4fdf-a3e0-62132da4a843
title: Konfigurieren von COM+-Anwendungspoolingwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d3407cd644b68cfc3ef279a9e67603aa1dc2db85302b22dbf0c6ae7219fd3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128972"
---
# <a name="configuring-com-application-pooling-values"></a>Konfigurieren von COM+-Anwendungspoolingwerten

Sie können die folgenden Anweisungen verwenden, um COM+-Anwendungspoolingwerte für Ihre COM+-Anwendung zu konfigurieren.

> [!Note]  
> Bibliotheksanwendungen verfügen über die Wiederverwendungs- und Poolingeigenschaften ihres Hostprozesses.

 

## <a name="component-services-administrative-tool"></a>Verwaltungstool für Komponentendienste

Führen Sie zum Konfigurieren des COM+-Anwendungspoolings für eine COM+-Anwendung die folgenden Schritte aus:

1.  Klicken Sie in der Konsolenstruktur des Komponentendienste-Verwaltungstools mit der rechten Maustaste auf die COM+-Anwendung, die Sie in einen Pool einpoolen möchten, und klicken Sie dann auf **Eigenschaften.**

2.  Geben Sie auf der Registerkarte **Pooling &** Wiederverwendung unter **Anwendungspooling** einen Wert für **Poolgröße** ein, abhängig von der Anzahl der Instanzen Ihrer Anwendung, die ausgeführt werden soll.

3.  Klicken Sie auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Die folgende Funktion in Visual Basic veranschaulicht, wie Sie den COM+-Anwendungspoolingwert (dargestellt durch die ConcurrentApps-Eigenschaft) für jede com+-Serveranwendung festlegen können, die Sie auswählen. Fügen Sie einen Verweis auf die COM+-Administratortypbibliothek hinzu, um sie über Visual Basic verwenden zu können.


```VB
Function SetMyApplicationPooling( _
  strApplicationName As String, _
  lngPoolValue As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationPooling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate 
    For Each objApplication in objAppCollection
        If objApplication.Name = strApplicationName Then
            objApplication.Value("ConcurrentApps") = lngPoolValue
            MsgBox strApplicationName & _
              " pooling value set to " & lngPoolValue
            Exit For
        End If
    Next
    objAppCollection.SaveChanges

    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationPooling = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Um die Funktion zu verwenden, geben Sie einen Zeichenfolgenwert für den COM+-Serveranwendungsnamen und einen ganzzahligen Wert für die gewünschte Anwendungspooleinstellung an. Der folgende Visual Basic zeigt, wie Der Wert des Anwendungspoolings für die Anwendung mit dem Namen "MyApplication" auf 15 festgelegt wird:


```VB
Sub Main()
    If Not SetMyApplicationPooling("MyApplication", 15) Then
        MsgBox "SetMyApplicationPooling failed."
    End If
End Sub

```



## <a name="cc"></a>C/C++

Die folgende Funktion in C++ veranschaulicht, wie Sie den COM+-Anwendungspoolingwert (dargestellt durch die ConcurrentApps-Eigenschaft) für jede com+-Serveranwendung festlegen können, die Sie auswählen. Die ErrorDescription-Methode wird unter [Interpretieren von Fehlercodes beschrieben.](interpreting-error-codes.md)


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\Com\ComAdmin.dll"
#include "ComAdmin.h"
#include "StrSafe.h"  // For the StringCchLengthW function

BOOL SetMyApplicationPooling (OLECHAR* szMyApp, LONG lPool) {
    IUnknown * pUnknown = NULL;
    ICOMAdminCatalog * pCatalog = NULL;
    ICatalogCollection * pAppColl = NULL;
    ICatalogObject * pApplication = NULL;
    HRESULT hr = S_OK;
    BSTR bstrMyApp = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp
    LCID lLan = 1024;// Use the default language for comparing strings.

try {
    // Test the input pool value.
    if ((lPool < 1) || (lPool > 1048576)) throw(E_INVALIDARG);
    
    // Test the input szMyApp to make sure it's OK to use.
    hr = StringCchLengthW(szMyApp, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert szMyApp to a BSTR.
    bstrMyApp = SysAllocString(szMyApp);

    // Create a COMAdminCatalog object and get its IUnknown.
    hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);

    // Get the ICOMAdminCatalog interface.
   hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) throw(hr);

    // Get an interface to the Applications collection.
    hr = pCatalog->GetCollection(L"Applications", (IDispatch**)&pAppColl);
    if (FAILED (hr)) throw(hr);

    // Populate all of the Applications collection.
    hr = pAppColl->Populate();
    if (FAILED (hr)) throw(hr);

    // Get the number of applications in the collection.
    LONG lCount = -1;
    hr = pAppColl->get_Count(&lCount);
    if (FAILED (hr)) throw(hr);

    // Iterate through each application in the collection.
    VARIANT varName;
    VariantInit(&varName);
    for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
        hr = pAppColl->get_Item(lIdx, (IDispatch**)&pApplication);
        if (FAILED (hr)) throw(hr);

        // Get the Name value of each application.
       hr = pApplication->get_Name(&varName);
        if (FAILED (hr)) throw(hr);

        // Compare the application name to bstrMyApp.
        hr = VarBstrCmp(varName.bstrVal, bstrMyApp, lLan, NULL);
        if (FAILED (hr)) throw(hr);
        if (VARCMP_EQ == hr) {  // The strings are equal.
            // Set the new pooling value.
            VARIANT varPool;
            VariantInit(&varPool);
            varPool.vt = VT_I4;  // Tell the VARIANT it's holding a LONG.
            varPool.lVal = lPool;
            hr = pApplication->put_Value(L"ConcurrentApps", varPool);
            if (FAILED (hr)) throw(hr);
            printf("%S pooling value set to %ld.\n", bstrMyApp, lPool);
            break;
        }
    }
    LONG lNum;
    hr = pAppColl->SaveChanges(&lNum);
    if (FAILED (hr)) throw(hr);

    // Clean up.
    SysFreeString(bstrMyApp);
    pUnknown->Release();
    pUnknown = NULL;
    pApplication->Release();
    pApplication = NULL;
    pAppColl->Release();
    pAppColl = NULL;
    pCatalog->Release();
    pCatalog = NULL;
    return (TRUE);
}  // Try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrMyApp);
    if (NULL != pUnknown) pUnknown>Release();
    pUnknown = NULL;
    if (NULL != pApplication) pApplication->Release();
    pApplication = NULL;
    if (NULL != pAppColl) pAppColl->Release();
    pAppColl = NULL;
    if (NULL != pCatalog) pCatalog->Release();
    pCatalog = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}
}  // SetMyApplicationPooling

```



Um die Funktion zu verwenden, geben Sie einen Zeichenfolgenwert für den COM+-Serveranwendungsnamen und einen ganzzahligen Wert für die gewünschte Anwendungspooleinstellung an. Der folgende C++-Code zeigt, wie Der Wert des Anwendungspoolings für die Anwendung namens "MyApplication" auf 15 festgelegt wird:

``` syntax
#define _WIN32_DCOM  // To use CoInitializeEx()
void main() {
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! SetMyApplicationPooling (L"MyApplication", 15))
        printf("SetMyApplicationPooling failed.\n");
    CoUninitialize();
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Anwendungspoolingkonzepte](com--application-pooling-concepts.md)
</dt> </dl>

 

 



