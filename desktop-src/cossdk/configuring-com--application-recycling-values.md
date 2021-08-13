---
description: Sie können die folgenden Methoden verwenden, um Anwendungswiederverwendungswerte für Ihre COM+-Anwendung zu konfigurieren.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Konfigurieren von COM+-Anwendungswiederverwendungswerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2613fb6f063a49d53baa90fad6f7dac862b848c6abf95fddcc36ace25e3d6b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548641"
---
# <a name="configuring-com-application-recycling-values"></a>Konfigurieren von COM+-Anwendungswiederverwendungswerten

Sie können die folgenden Methoden verwenden, um Anwendungswiederverwendungswerte für Ihre COM+-Anwendung zu konfigurieren.

> [!Note]  
> Sie können keine COM+-Anwendung wiederverwenden, die für die Ausführung als Windows Dienst konfiguriert wurde. Darüber hinaus verfügen Bibliotheksanwendungen über die Wiederverwendungs- und Poolingeigenschaften ihres Hostprozesses.

 

## <a name="component-services-administrative-tool"></a>Verwaltungstool "Komponentendienste"

Um die Anwendungswiederverwendung für eine COM+-Anwendung zu konfigurieren, verwenden Sie die folgenden Schritte:

1.  Klicken Sie in der Konsolenstruktur des Component Services-Verwaltungstools mit der rechten Maustaste auf die COM+-Serveranwendung, die Sie wiederverwenden möchten, und klicken Sie dann auf **Eigenschaften.**

2.  Geben Sie auf der Registerkarte **& Wiederverwendung** werte für **Lebensdauerlimit (Minuten)**, **Arbeitsspeicherlimit (KB)**, **Ablaufzeitlimit (Minuten)**, **Aufruflimit** und **Aktivierungslimit** ein. Dies hängt von den Kriterien ab, die Sie verwenden möchten.

    -   **Lebensdauerlimit** gibt die maximale Anzahl von Minuten an, die ein Prozess ausgeführt werden kann, bevor er wiederverwendet wird. Der gültige Bereich beträgt 0 bis 30.240 Minuten (21 Tage). Die Standardanzahl von Minuten ist 0.
    -   **Arbeitsspeicherlimit** gibt die maximale Speicherauslastung des Prozesses (in Kilobyte) an, bevor der Prozess wiederverwendet wird. Wenn die Arbeitsspeicherauslastung des Prozesses die angegebene Anzahl länger als eine Minute überschreitet, wird der Prozess wiederverwendet. Der gültige Bereich liegt zwischen 0 und 1.048.576 KB, und die Standardspeicherauslastung beträgt 0 KB.
    -   **Das Ablauftimeout** gibt die Anzahl der Minuten an, die auf die Freigabe aller externen Verweise auf Objekte im Prozess gewartet werden soll, bevor sie zum Herunterfahren aufgefordert werden. Der gültige Bereich beträgt 1 bis 1.440 Minuten (24 Stunden), und das Standardablauftime out beträgt 15 Minuten. Dieser Wert wird nur verwendet, wenn bereits bestimmt ist, dass ein Prozess basierend auf den anderen Kriterien wiederverwendet wird.
    -   **Aufruflimit** gibt die maximale Anzahl von Aufrufen an, die Anwendungsobjekte akzeptieren können, bevor der Prozess wiederverwendet wird. Der gültige Bereich beträgt 0 bis 1.048.576 Aufrufe, und die Standardanzahl der Aufrufe ist 0.
    -   **Aktivierungslimit** gibt die maximale Anzahl von Anwendungsobjektaktivierungen an, die vor dem Wiederverwenden des Prozesses akzeptiert werden sollen. Der gültige Bereich beträgt 0 bis 1.048.576 Aktivierungen, und die Standardanzahl der Aktivierungen ist 0.

    > [!Note]  
    > Wenn der Wert **für Lebensdauerlimit,** **Arbeitsspeicherlimit,** **Aufruflimit** oder **Aktivierungslimit** auf 0 (Standardwert) festgelegt ist, wird die Anwendungswiederverwendung für dieses Kriterium deaktiviert. Wenn alle vier Kriterien auf 0 festgelegt sind, wird die Anwendungswiederverwendung für die ausgewählte Anwendung deaktiviert.

     

3.  Klicken Sie auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Die folgende Funktion in Microsoft Visual Basic veranschaulicht, wie Sie die Wiederverwendeungswerte der Anwendung für eine beliebige COM+-Serveranwendung festlegen können. Um es über Visual Basic zu verwenden, fügen Sie einen Verweis auf die COM+-Administratortypbibliothek hinzu.


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Um die Funktion zu verwenden, geben Sie einen Zeichenfolgenwert für den Anwendungsnamen und ganzzahlige Werte für die gewünschten Anwendungswiederverwendungseinstellungen an. Der folgende Visual Basic Code zeigt, wie der **RecycleLifetimeLimit-Wert** auf 5, der **RecycleMemoryLimit-Wert** auf 10, der **RecycleCallLimit-Wert** auf 9, der **RecycleActivationLimit-Wert** auf 100 und der **RecycleExpirationTimeout-Wert** auf 15 festgelegt werden.


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KONZEPTE DER COM+-Anwendungswiederverwendung](com--application-recycling-concepts.md)
</dt> </dl>

 

 



