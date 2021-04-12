---
description: Sie können die folgenden Methoden verwenden, um Anwendungs Wiederverwendungs Werte für Ihre COM+-Anwendung zu konfigurieren.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Konfigurieren von com+-Anwendungs Wiederverwendungs Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127560"
---
# <a name="configuring-com-application-recycling-values"></a>Konfigurieren von com+-Anwendungs Wiederverwendungs Werten

Sie können die folgenden Methoden verwenden, um Anwendungs Wiederverwendungs Werte für Ihre COM+-Anwendung zu konfigurieren.

> [!Note]  
> Eine COM+-Anwendung, die für die Verwendung als Windows-Dienst konfiguriert wurde, kann nicht wieder verwendet werden. Außerdem verfügen Bibliotheksanwendungen über die Eigenschaften zum wieder verwenden und zum Pooling Ihres Host Prozesses.

 

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Führen Sie die folgenden Schritte aus, um die Anwendungs Wiederverwendung für eine COM+-Anwendung zu konfigurieren:

1.  Klicken Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die COM+-Serveranwendung, die wieder verwendet werden soll, und klicken Sie dann auf **Eigenschaften**.

2.  Geben Sie auf der Registerkarte **Pooling &** Wiederverwendung Werte für **Lebensdauer Limit (Minuten)**, Arbeits **Speicher Limit (KB)**, **Ablauf Timeout (Minuten)**, **Abruf Limit** und **Aktivierungs Limit** ein, abhängig von den Kriterien, die Sie verwenden möchten.

    -   **Lebensdauer Limit** gibt die maximale Anzahl von Minuten an, die ein Prozess ausgeführt werden kann, bevor er wieder verwendet wird. Der gültige Bereich liegt zwischen 0 und 30.240 Minuten (21 Tage). Die Standard Anzahl von Minuten ist 0 (null).
    -   Arbeits **Speicher Limit** gibt die maximale Menge an Prozess Speicherauslastung (in Kilobytes) an, bevor der Prozess wieder verwendet wird. Wenn die Speicherauslastung des Prozesses die angegebene Anzahl länger als eine Minute überschreitet, wird der Prozess wieder verwendet. Der gültige Bereich liegt zwischen 0 und 1.048.576 KB, und die Standardmenge der Speicherauslastung beträgt 0 KB.
    -   **Ablauf Timeout** gibt die Anzahl von Minuten an, die gewartet werden soll, bevor das Herunterfahren erzwungen wird, damit alle externen Verweise auf Objekte im Prozess freigegeben werden. Der gültige Bereich liegt zwischen 1 und 1440 Minuten (24 Stunden), und das Standard Ablauf Timeout beträgt 15 Minuten. Dieser Wert wird nur verwendet, wenn bereits festgestellt wurde, dass ein Prozess basierend auf den anderen Kriterien wieder verwendet wird.
    -   " **Aufruf Limit** " gibt die maximale Anzahl von Aufrufen an, die Anwendungs Objekte annehmen können, bevor der Prozess wieder verwendet wird. Der gültige Bereich liegt zwischen 0 und 1.048.576 aufrufen, und die Standard Anzahl von Aufrufen beträgt 0.
    -   **Aktivierungs Limit** gibt die maximale Anzahl von Anwendungs Objekt Aktivierungen an, die vor der Wiederverwendung des Prozesses akzeptiert werden sollen. Der gültige Bereich liegt zwischen 0 und 1.048.576 Aktivierungen, und die Standard Anzahl von Aktivierungen beträgt 0.

    > [!Note]  
    > Wenn die Einstellung für die **Lebensdauer**, das Arbeits **Speicherlimit**, das **Aufruflimit** oder der Wert für das **Aktivierungs Limit** auf 0 (Standardwert) festgelegt ist, wird die Anwendungs Wiederverwendung für dieses Kriterium deaktiviert. Wenn alle vier dieser Kriterien auf 0 festgelegt sind, wird die Anwendungs Wiederverwendung für die ausgewählte Anwendung deaktiviert.

     

3.  Klicken Sie auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Die folgende Funktion in Microsoft Visual Basic veranschaulicht, wie Sie die Werte für die Anwendungs Wiederverwendung für eine beliebige COM+-Serveranwendung festlegen können, die Sie auswählen. Um es aus Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu.


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



Um die-Funktion zu verwenden, geben Sie einen Zeichen folgen Wert für den Anwendungsnamen und ganzzahlige Werte für die Einstellungen der gewünschten Anwendungs Wiederverwendung an. Der folgende Visual Basic Code zeigt, wie der Wert für " **recyclelifetimelimit** " auf "5", den Wert " **recyclememorylimit** " auf "10", den Wert "RecycleCallLimit" auf 9, den Wert für " **recycleactivationlimit** " 100 auf "9" und den Wert " **recycleexpirationtimeout** " auf 15 


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der com+-Anwendungs Wiederverwendung](com--application-recycling-concepts.md)
</dt> </dl>

 

 



