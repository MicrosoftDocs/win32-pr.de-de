---
description: Im folgenden Beispiel wird veranschaulicht, wie die msidigitalcertificate-Tabelle und die msidigitalsignature-Tabelle mit einer Visual Basic for Applications-Unterroutine (VBA) aufgefüllt werden.
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99267feffac71401f36635c08fa7f9f6598a0c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959518"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation

Im folgenden Beispiel wird veranschaulicht, wie die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md) und die [msidigitalsignature-Tabelle](msidigitalsignature-table.md) mit einer Visual Basic for Applications-Unterroutine (VBA) aufgefüllt werden. Weitere Informationen zum Sichern von Windows Installer Paketen finden Sie unter [Richtlinien zum Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md).

Die [**filesignatureinfo-Methode**](installer-filesignatureinfo.md) gibt ein SafeArray von Bytes zurück. Weitere Informationen finden Sie unter dem [**SAFEARRAY-Datentyp**](/windows/win32/api/oaidl/ns-oaidl-safearray). Die Daten aus diesem Array müssen in Unicode konvertiert werden, da Visual Basic keine Möglichkeit hat, Bytes direkt in eine Datei zu schreiben. Die [**setStream-Methode**](record-setstream.md) kann dann die Datei der konvertierten Daten verwenden, um Datenstrom Daten in ein angegebenes Daten Satz Feld eines [**Datensatz-Objekts**](record-object.md)zu schreiben. Beachten Sie, dass bei der Konvertierung der Bytedaten in Unicode die Daten potenziell geändert werden können und dass die konvertierten Daten für die korrekte Signatur Überprüfung mit den ursprünglichen Daten identisch sein müssen. Der Paket Ersteller muss sicherstellen, dass die ursprünglichen und konvertierten Daten stimmen.


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



 

 
