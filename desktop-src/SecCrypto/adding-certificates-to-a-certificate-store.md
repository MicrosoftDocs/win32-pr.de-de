---
description: Zertifikate können Zertifikatspeichern hinzugefügt oder daraus entfernt werden, wenn der Speicher mit Lese-/Schreibberechtigung geöffnet wird.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Hinzufügen von Zertifikaten zu einem Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c4b2fafbcd11bf2d984dfd5b5a575f67dc4f6d3c70337de399ca6076029ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774035"
---
# <a name="adding-certificates-to-a-certificate-store"></a>Hinzufügen von Zertifikaten zu einem Store

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM.](alternatives-to-using-capicom.md)\]

[*Zertifikate*](../secgloss/c-gly.md) können [*Zertifikatspeichern*](../secgloss/c-gly.md) hinzugefügt oder daraus entfernt werden, wenn der Speicher mit Lese-/Schreibberechtigung geöffnet wird. Active Directory-Speichern wird keine Lese-/Schreibberechtigung erteilt. Obwohl Zertifikate zu Speicherspeichern hinzugefügt oder daraus entfernt werden können, werden Änderungen in Speicherspeichern nicht zwischen Sitzungen beibehalten.

Zertifikate können einem Zertifikatspeicher hinzugefügt werden, der mit Lese-/Schreibberechtigung mithilfe der **Add-Methode** geöffnet wird. Ein Zertifikat kann mithilfe der **Remove-Methode** aus einem Zertifikatspeicher entfernt werden, der mit Lese-/Schreibberechtigung geöffnet wird. Neue Speicher können im CAPICOM \_ CURRENT \_ USER STORE und \_ CAPICOM LOCAL MACHINE STORE erstellt und gespeichert \_ \_ \_ werden. Neu erstellte Speicher an einem dieser Speicherorte können mit Lese-/Schreibberechtigung geöffnet werden.

Im folgenden Beispiel werden zwei Zertifikatspeicher geöffnet. Zertifikate von Antragstellern mit Nachnamen, die mit F beginnen, werden aus dem Active Directory-Speicher abgerufen. Der CAPICOM \_ CURRENT USER STORE und der \_ \_ CAPICOM \_ CA \_ STORE-Speicher werden dann als Lese-/Schreibspeicher geöffnet, und das erste Zertifikat aus der Sammlung von Zertifikaten im Active Directory-Speicher wird den Zertifikaten im CAPICOM CA \_ STORE \_ hinzugefügt.

Zu Demonstrationszwecken zeigt das Beispiel das Öffnen von Filialen im CAPICOM \_ MEMORY \_ STORE, CAPICOM \_ CURRENT USER STORE und \_ \_ CAPICOM \_ LOCAL MACHINE \_ \_ STORE. Das Beispiel zeigt, wie alle Zertifikate aus einem geöffneten Speicher exportiert, die exportierten Zertifikate in eine Datei geschrieben, wieder eingelesen und in einen anderen Speicher importiert werden. Die neu importierten Zertifikate werden aufzählt und angezeigt.

Bei einem CAPICOM-Fehler wird ein negativer Dezimalwert von **Err.Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err.Number** finden Sie unter Winerror.h.

Das folgende Beispiel zeigt das Öffnen von Zertifikatspeichern mithilfe einer frühen Bindung in der **Deklaration** der Store-Objekten und beim Erstellen einer Instanz dieser Objekte.


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
