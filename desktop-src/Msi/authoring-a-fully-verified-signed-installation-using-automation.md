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
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a><span data-ttu-id="ed62b-103">Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation</span><span class="sxs-lookup"><span data-stu-id="ed62b-103">Authoring a Fully Verified Signed Installation Using Automation</span></span>

<span data-ttu-id="ed62b-104">Im folgenden Beispiel wird veranschaulicht, wie die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md) und die [msidigitalsignature-Tabelle](msidigitalsignature-table.md) mit einer Visual Basic for Applications-Unterroutine (VBA) aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="ed62b-104">The following sample demonstrates how to populate the [MsiDigitalCertificate table](msidigitalcertificate-table.md) and [MsiDigitalSignature table](msidigitalsignature-table.md) by using a Visual Basic for Applications (VBA) subroutine.</span></span> <span data-ttu-id="ed62b-105">Weitere Informationen zum Sichern von Windows Installer Paketen finden Sie unter [Richtlinien zum Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md).</span><span class="sxs-lookup"><span data-stu-id="ed62b-105">For more information about securing Windows Installer packages see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md).</span></span>

<span data-ttu-id="ed62b-106">Die [**filesignatureinfo-Methode**](installer-filesignatureinfo.md) gibt ein SafeArray von Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="ed62b-106">The [**FileSignatureInfo method**](installer-filesignatureinfo.md) returns a SAFEARRAY of bytes.</span></span> <span data-ttu-id="ed62b-107">Weitere Informationen finden Sie unter dem [**SAFEARRAY-Datentyp**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="ed62b-107">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span> <span data-ttu-id="ed62b-108">Die Daten aus diesem Array müssen in Unicode konvertiert werden, da Visual Basic keine Möglichkeit hat, Bytes direkt in eine Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ed62b-108">The data from this array must be converted to Unicode because Visual Basic does not have a way to write bytes straight into a file.</span></span> <span data-ttu-id="ed62b-109">Die [**setStream-Methode**](record-setstream.md) kann dann die Datei der konvertierten Daten verwenden, um Datenstrom Daten in ein angegebenes Daten Satz Feld eines [**Datensatz-Objekts**](record-object.md)zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ed62b-109">The [**SetStream method**](record-setstream.md) can then use the file of converted data to write stream data into a specified record field of a [**Record object**](record-object.md).</span></span> <span data-ttu-id="ed62b-110">Beachten Sie, dass bei der Konvertierung der Bytedaten in Unicode die Daten potenziell geändert werden können und dass die konvertierten Daten für die korrekte Signatur Überprüfung mit den ursprünglichen Daten identisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="ed62b-110">Note that conversion of the byte data to Unicode can potentially change the data and that the converted data must match the original data for correct signature verification.</span></span> <span data-ttu-id="ed62b-111">Der Paket Ersteller muss sicherstellen, dass die ursprünglichen und konvertierten Daten stimmen.</span><span class="sxs-lookup"><span data-stu-id="ed62b-111">The package author must ensure that the original and converted data match.</span></span>


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



 

 
