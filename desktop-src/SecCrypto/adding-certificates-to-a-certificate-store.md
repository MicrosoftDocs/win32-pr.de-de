---
description: Zertifikate können dem Zertifikat Speicher hinzugefügt oder daraus entfernt werden, wenn der Speicher mit Lese-/Schreibberechtigungen geöffnet ist.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Hinzufügen von Zertifikaten zu einem Zertifikat Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529234"
---
# <a name="adding-certificates-to-a-certificate-store"></a>Hinzufügen von Zertifikaten zu einem Zertifikat Speicher

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

[*Zertifikate*](../secgloss/c-gly.md) können dem [*Zertifikat Speicher*](../secgloss/c-gly.md) hinzugefügt oder daraus entfernt werden, wenn der Speicher mit Lese-/Schreibberechtigungen geöffnet ist. Die Lese-/Schreibberechtigung wird Active Directory speichern nicht erteilt. Während Zertifikate hinzugefügt oder aus dem Speicher Speicher entfernt werden können, werden Änderungen in Speicher speichern zwischen den Sitzungen nicht beibehalten.

Zertifikate können einem Zertifikat Speicher hinzugefügt werden, der mit der Lese-/Schreibberechtigung mithilfe der **Add** -Methode geöffnet wird. Ein Zertifikat kann mithilfe der **Remove** -Methode aus einem Zertifikat Speicher entfernt werden, der mit der Lese-/Schreibberechtigung geöffnet wurde. Neue Filialen können erstellt und im aktuellen CAPICOM \_ \_ \_ -Benutzerspeicher und CAPICOM- \_ \_ Speicherorten für lokale Computer \_ gespeichert werden. Neu erstellte Filialen an einem dieser Speicherorte können mit Lese-/Schreibberechtigung geöffnet werden.

Im folgenden Beispiel werden zwei Zertifikat Speicher geöffnet. Zertifikate von Subjekten mit Nachnamen, die mit F beginnen, werden aus dem Active Directory Speicher abgerufen. Der aktuelle CAPICOM- \_ \_ Benutzer \_ Speicher, CAPICOM \_ ca \_ Store Store, wird dann als Lese-/Schreibspeicher geöffnet, und das erste Zertifikat aus der Sammlung der Zertifikate im Active Directory Store wird den Zertifikaten im CAPICOM-ca-Speicher hinzugefügt \_ \_ .

Zu Demonstrationszwecken zeigt das Beispiel das Öffnen von Stores im CAPICOM \_ -Speicher Speicher \_ , CAPICOM \_ Current \_ User \_ Store und CAPICOM-Speicher \_ Orte für lokale \_ Computer \_ . Das Beispiel zeigt, wie Sie alle Zertifikate aus einem geöffneten Speicher exportieren, die exportierten Zertifikate in eine Datei schreiben, Sie wieder einlesen und in einen anderen Speicher importieren. Die neu importierten Zertifikate werden aufgelistet und angezeigt.

Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.

Das folgende Beispiel zeigt das Öffnen von Zertifikat speichern mithilfe der frühen Bindung in der Deklaration der **Speicher** Objekte und das Erstellen einer Instanz dieser Objekte.


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



 

 
