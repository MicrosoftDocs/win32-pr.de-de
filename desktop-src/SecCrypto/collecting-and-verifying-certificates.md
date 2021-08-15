---
description: Im folgenden Beispiel werden die Zertifikate in einem lokalen Speicher aufzählt und auf Gültigkeit überprüft.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Sammeln und Überprüfen von Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60b793cf4aeca7d05d166a4b205b924db53faee09683cefcef7b0244a9eb0289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769531"
---
# <a name="collecting-and-verifying-certificates"></a>Sammeln und Überprüfen von Zertifikaten

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM.](alternatives-to-using-capicom.md)\]

Häufig muss eine Gruppe von [*Zertifikaten*](../secgloss/c-gly.md) gesammelt und überprüft werden. Dies erfolgt häufig, um eine Gruppe von Empfängern auf eine umschlagete Nachricht vorzubereiten. Im folgenden Beispiel werden die Zertifikate in einem lokalen Speicher aufzählt und auf Gültigkeit überprüft. Als Nächstes wird ein Active Directory-Speicher geöffnet, um neue Zertifikate abzurufen und dem lokalen Speicher hinzuzufügen. Die aus dem Active Directory-Speicher abgerufenen Zertifikate werden auf Gültigkeit überprüft und ggf. dem lokalen Speicher hinzugefügt. Beide Speicher werden dann geschlossen.

Bei einem CAPICOM-Fehler wird ein negativer Dezimalwert von **Err.Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err.Number** finden Sie unter Winerror.h.

In diesem Beispiel wird der Name des lokalen Speichers als Zeichenfolgenparameter übergeben. Eine Zeichenfolge, die die Suchkriterien für Zertifikate im Active Directory-Speicher angibt, wird ebenfalls als Parameter übergeben.


```VB
Sub CollectValidCerts(ByVal storename As String, ByVal _
    certname As String)

    On Error GoTo errorhandler

    ' Prepare a local certificate store to contain valid
    ' certificates for the recipients of an enveloped
    ' message.

    ' Open the local store and go to the certificates in the store
    '   1. Display the certificate
    '   2. Check the validity of the certificate
    '   3. Remove certificates that are not valid from the store

    Dim LocalStore As New Store
    Dim ADStore As New Store
    Dim i As Long

    LocalStore.Open(CAPICOM_CURRENT_USER_STORE, storename, _
        CAPICOM_STORE_OPEN_READ_WRITE)

    MsgBox("There are " & LocalStore.Certificates.Count & _
        " certificates in this store ")
    For i = 1 To LocalStore.Certificates.Count
        If LocalStore.Certificates.Item(i).IsValid Then
            LocalStore.Certificates.Item(i).Display()
        Else
            MsgBox("A certificate that is not valid was found.")
        End If
    Next i

    ' Open the AD store and retrieve a certificate based
    ' on a string passed into the function. Add any valid
    ' certificates found to the local store.

    ADStore.Open(CAPICOM_ACTIVE_DIRECTORY_USER_STORE, certname, _
        CAPICOM_STORE_OPEN_READ_ONLY)
    MsgBox("There are " & ADStore.Certificates.Count & _
        " certificates in the AD store.")

    For i = 1 To ADStore.Certificates.Count
        If ADStore.Certificates.Item(i).IsValid Then
            ADStore.Certificates.Item(i).Display()
            LocalStore.Add(ADStore.Certificates.Item(i))
        Else
            MsgBox("the certificate from the AD store is not valid.")
        End If
    Next i

    LocalStore = Nothing
    ADStore = Nothing
    MsgBox("Sub finished without error ")
    Exit Sub
errorhandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
