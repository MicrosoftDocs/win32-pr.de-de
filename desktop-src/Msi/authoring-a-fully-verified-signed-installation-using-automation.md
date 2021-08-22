---
description: Im folgenden Beispiel wird veranschaulicht, wie die Tabelle MsiDigitalCertificate und msiDigitalSignature mithilfe einer Visual Basic for Applications-Unterroutine (VBA) aufgefüllt werden.
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f1b0b90296ad92e471449213e86721482a545ff1932458b2ad6b21d47b665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559100"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation

Im folgenden Beispiel wird veranschaulicht, wie die [Tabelle MsiDigitalCertificate](msidigitalcertificate-table.md) und [die MsiDigitalSignature-Tabelle](msidigitalsignature-table.md) mithilfe einer Visual Basic for Applications-Unterroutine (VBA) aufgefüllt werden. Weitere Informationen zum Sichern von Windows Installer-Paketen finden Sie unter [Richtlinien für die Erstellung sicherer Installationen.](guidelines-for-authoring-secure-installations.md)

Die [**FileSignatureInfo-Methode gibt**](installer-filesignatureinfo.md) safearray von Bytes zurück. Weitere Informationen finden Sie unter [**SAFEARRAY-Datentyp.**](/windows/win32/api/oaidl/ns-oaidl-safearray) Die Daten aus diesem Array müssen in Unicode konvertiert werden, da Visual Basic keine Möglichkeit hat, Bytes direkt in eine Datei zu schreiben. Die [**SetStream-Methode**](record-setstream.md) kann dann die Datei der konvertierten Daten verwenden, um Streamdaten in ein angegebenes Datensatzfeld eines [**Record-Objekts zu schreiben.**](record-object.md) Beachten Sie, dass die Konvertierung der Bytedaten in Unicode die Daten möglicherweise ändern kann und dass die konvertierten Daten mit den ursprünglichen Daten übereinstimmen müssen, um die richtige Signaturüberprüfung zu erhalten. Der Paketautor muss sicherstellen, dass die ursprünglichen und konvertierten Daten übereinstimmen.


```VB
Sub PopulateDigitalSignature()

    Dim Installer As Object
    Dim Database As Object
    Dim x() As Byte
    
    Const szSignedCabinet = "c:\test.cab"
    Const szCertFile = "c:\temp\test.cer"
    Const szDatabase = "c:\test.msi"
        
    Set Installer = CreateObject("WindowsInstaller.Installer")
    
    x = Installer.FileSignatureInfo(szSignedCabinet, 0, msiSignatureInfoCertificate)
    
    Dim fs, ts
    Dim s As String
    Set fs = CreateObject("Scripting.FileSystemObject")
    Set ts = fs.CreateTextFile(szCertFile, True)        'Create a file
    
    s = StrConv(x, vbUnicode)
    ts.Write s
    ts.Close
        
    Set Database = Installer.OpenDatabase(szDatabase, msiOpenDatabaseModeTransact)
    Set ViewCert = Database.OpenView("SELECT * FROM `MsiDigitalCertificate`")
    ViewCert.Execute 0
    Set ViewSig = Database.OpenView("SELECT * FROM `MsiDigitalSignature`")
    ViewSig.Execute 0
    
    Set RecordCert = Installer.CreateRecord(2)
    RecordCert.StringData(1) = "Test"
    RecordCert.SetStream 2, szCertFile
    ViewCert.Modify msiViewModifyInsert, RecordCert
    
    Set RecordSig = Installer.CreateRecord(4)
    RecordSig.StringData(1) = "Media"
    RecordSig.StringData(2) = "1"
    RecordSig.StringData(3) = "Test"
    ViewSig.Modify msiViewModifyInsert, RecordSig
    
    Database.Commit
      fs.DeleteFile(szCertFile)
End Sub
```



 

 
