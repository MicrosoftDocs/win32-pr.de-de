---
description: Im folgenden Beispiel werden Aspekte beim Arbeiten mit dem Store-Objekt veranschaulicht. Es zeigt öffnende Filialen im CAPICOM \_ -Speicher Speicher \_ , im \_ aktuellen CAPICOM \_ \_ -Benutzerspeicher und im lokalen CAPICOM- \_ Computerspeicher \_ \_ .
ms.assetid: bfb7ff48-1d6b-404f-9dd4-6de1898354b7
title: Verwenden von speichern an unterschiedlichen Standorten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e22fa4d4eca4748d6c4652a8b33d22a1db492a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753440"
---
# <a name="using-stores-in-different-locations"></a>Verwenden von speichern an unterschiedlichen Standorten

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Im folgenden Beispiel werden Aspekte beim Arbeiten mit dem [**Store**](store.md) -Objekt veranschaulicht. Es zeigt öffnende Filialen im CAPICOM \_ -Speicher Speicher \_ , im \_ aktuellen CAPICOM \_ \_ -Benutzerspeicher und im lokalen CAPICOM- \_ Computerspeicher \_ \_ .

Das Beispiel zeigt das Exportieren von [*Zertifikaten*](../secgloss/c-gly.md) aus einem geöffneten [*Speicher*](../secgloss/c-gly.md), das Schreiben der exportierten Zertifikate in eine Datei, das zurück lesen und Importieren in einen anderen Speicher. Die neu importierten Zertifikate werden dann aufgezählt und angezeigt.

Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.


```VB
Sub OpenStores()

    On Error GoTo ErrorHandler

    'Open Memory, current user, and local machine stores
    Dim MemoryStore As New Store
    Dim CurrentUserStore As New Store
    Dim LocalMachineStore As New Store
    Dim NumCerts As Integer

    MemoryStore.Open(CAPICOM_MEMORY_STORE, "MemStore", _
        CAPICOM_STORE_OPEN_READ_WRITE)
    CurrentUserStore.Open(CAPICOM_CURRENT_USER_STORE, _
        CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_ONLY)
    LocalMachineStore.Open(CAPICOM_LOCAL_MACHINE_STORE, _
        CAPICOM_CA_STORE, CAPICOM_STORE_OPEN_READ_ONLY)

    ' Check the number of certificates in the stores.
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the memory store. ")
    NumCerts = CurrentUserStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the current user store. ")
    NumCerts = LocalMachineStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the local machine store. ")


    '  Export the certificates in the current user MY store
    '  to a file.
    Dim ExportString As String
    ExportString = CurrentUserStore.Export
Open "Exportcerts.txt" For Output As #1
Write #1, ExportString
Close #1

    ' Read the store the file.
    Dim importString As String
Open "exportcerts.txt" For Input As #2
Input #2, importString
Close #2
    MemoryStore.Import(importString)

    ' Check the number of certificates in the memory store after 
    ' import()
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates now in the memory store. ")

    ' Enumerate the certificates in the memory store and display each
    ' certificate
    Dim i As Long
    For i = 1 To NumCerts
        MemoryStore.Certificates.Item(i).Display()
    Next i

    ' Release the store objects
    MemoryStore = Nothing
    CurrentUserStore = Nothing
    LocalMachineStore = Nothing
    Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found: " & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
