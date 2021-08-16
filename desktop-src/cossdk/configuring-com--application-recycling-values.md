---
description: Sie können die folgenden Methoden verwenden, um Werte für die Wiederverwendung von Anwendungen für Ihre COM+-Anwendung zu konfigurieren.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Konfigurieren von COM+-Werten für die Wiederverwendung von Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2613fb6f063a49d53baa90fad6f7dac862b848c6abf95fddcc36ace25e3d6b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548641"
---
# <a name="configuring-com-application-recycling-values"></a>Konfigurieren von COM+-Werten für die Wiederverwendung von Anwendungen

Sie können die folgenden Methoden verwenden, um Werte für die Wiederverwendung von Anwendungen für Ihre COM+-Anwendung zu konfigurieren.

> [!Note]  
> Sie können keine COM+-Anwendung wiederverwerten, die für die Ausführung als Windows wurde. Darüber hinaus verfügen Bibliotheksanwendungen über die Wiederverwendungs- und Poolingeigenschaften ihres Hostprozesses.

 

## <a name="component-services-administrative-tool"></a>Verwaltungstool für Komponentendienste

Führen Sie die folgenden Schritte aus, um die Wiederverwendung von Anwendungen für eine COM+-Anwendung zu konfigurieren:

1.  Klicken Sie in der Konsolenstruktur des Komponentendienste-Verwaltungstools mit der rechten Maustaste auf die COM+-Serveranwendung, die wiederverwendet werden soll, und klicken Sie dann auf **Eigenschaften.**

2.  Geben Sie auf der Registerkarte  **Pooling & Recycling** Werte für Lebensdauerlimit **(Minuten),** Arbeitsspeicherlimit **(KB),** Ablaufzeitlimit **(Minuten),** Aufruflimit und Aktivierungslimit ein, je nach den Kriterien, die Sie verwenden möchten. 

    -   **Lebensdauerlimit** gibt die maximale Anzahl von Minuten an, die ein Prozess ausgeführt werden kann, bevor er wiederverwendet wird. Der gültige Bereich beträgt 0 bis 30.240 Minuten (21 Tage). Die Standardanzahl von Minuten ist 0.
    -   **Arbeitsspeicherlimit** gibt die maximale Prozessspeicherauslastung (in Kilobyte) an, bevor der Prozess wiederverwertet wird. Wenn die Speicherauslastung des Prozesses länger als eine Minute die angegebene Anzahl überschreitet, wird der Prozess wiederverwendet. Der gültige Bereich beträgt 0 bis 1.048.576 KB, und die Standardmenge der Speicherauslastung beträgt 0 KB.
    -   **Ablaufzeitüberschreitung gibt** die Anzahl der Minuten an, die gewartet werden soll, bevor er zum Herunterfahren auf die Freigabe aller externen Verweise auf Objekte im Prozess gewartet wird. Der gültige Bereich beträgt 1 bis 1440 Minuten (24 Stunden), und das Standardablauf-Time out beträgt 15 Minuten. Dieser Wert wird nur verwendet, wenn bereits bestimmt wurde, dass ein Prozess basierend auf den anderen Kriterien wiederverwendet wird.
    -   **Aufruflimit gibt** die maximale Anzahl von Aufrufen an, die Anwendungsobjekte akzeptieren können, bevor der Prozess wiederverwertet wird. Der gültige Bereich ist 0 bis 1.048.576 Aufrufe, und die Standardanzahl der Aufrufe ist 0.
    -   **Aktivierungslimit** gibt die maximale Anzahl von Anwendungsobjektaktivierungen an, die vor der Wiederverwendung des Prozesses akzeptiert werden. Der gültige Bereich liegt zwischen 0 und 1.048.576 Aktivierungen, und die Standardanzahl der Aktivierungen ist 0.

    > [!Note]  
    > Wenn der **Wert für Lebensdauerlimit,** **Arbeitsspeicherlimit,** **Aufruflimit** oder **Aktivierungslimit** auf 0 (Standardwert) festgelegt ist, wird die Wiederverwendung von Anwendungen für dieses Kriterium deaktiviert. Wenn alle vier Kriterien auf 0 festgelegt sind, wird die Wiederverwendung von Anwendungen für die ausgewählte Anwendung deaktiviert.

     

3.  Klicken Sie auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Die folgende Funktion in Microsoft Visual Basic veranschaulicht, wie Sie die Werte für die Wiederverwendung von Anwendungen für eine beliebige COM+-Serveranwendung festlegen können. Fügen Sie einen Verweis auf Visual Basic COM+-Administratortypbibliothek hinzu, um sie aus der Datei zu verwenden.


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



Um die Funktion zu verwenden, geben Sie einen Zeichenfolgenwert für den Anwendungsnamen und ganzzahlige Werte für die gewünschten Einstellungen für die Wiederverwendung von Anwendungen an. Der folgende Visual Basic-Code zeigt, wie Sie den **RecycleLifetimeLimit-Wert** auf 5, den **RecycleMemoryLimit-Wert** auf 10, den **RecycleCallLimit-Wert** auf 9, den **RecycleActivationLimit-Wert** auf 100 und den **RecycleExpirationTimeout-Wert** auf 15 festlegen.


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Konzepte für die Wiederverwendung von Anwendungen](com--application-recycling-concepts.md)
</dt> </dl>

 

 



