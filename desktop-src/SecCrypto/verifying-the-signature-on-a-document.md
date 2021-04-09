---
description: Wenn ein signiertes Dokument empfangen wird, kann die Gültigkeit der Signatur oder der Signaturen überprüft werden.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Überprüfen der Signatur in einem Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865451"
---
# <a name="verifying-the-signature-on-a-document"></a><span data-ttu-id="eadc7-103">Überprüfen der Signatur in einem Dokument</span><span class="sxs-lookup"><span data-stu-id="eadc7-103">Verifying the Signature on a Document</span></span>

<span data-ttu-id="eadc7-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eadc7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="eadc7-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="eadc7-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="eadc7-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="eadc7-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="eadc7-107">Wenn ein signiertes Dokument empfangen wird, kann die Gültigkeit der Signatur oder der Signaturen überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="eadc7-107">When a signed document is received, the validity of the signature or signatures can be checked.</span></span> <span data-ttu-id="eadc7-108">Eine Signatur kann auf Folgendes geprüft werden:</span><span class="sxs-lookup"><span data-stu-id="eadc7-108">A signature can be checked for:</span></span>

-   <span data-ttu-id="eadc7-109">Gültigkeit des Signatur Hashs</span><span class="sxs-lookup"><span data-stu-id="eadc7-109">Validity of the signature hash</span></span>
-   <span data-ttu-id="eadc7-110">Gültigkeit des Zertifikats des Signatur Gebers</span><span class="sxs-lookup"><span data-stu-id="eadc7-110">Validity of the signer's certificate</span></span>

<span data-ttu-id="eadc7-111">Der Signatur [*Hash*](../secgloss/h-gly.md) wird mithilfe des [*öffentlichen Schlüssels*](../secgloss/p-gly.md) des Signatur Gebers entschlüsselt, der im [*Zertifikat*](../secgloss/c-gly.md)des Signatur Gebers gefunden wurde und als Teil der Signatur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="eadc7-111">The signature [*hash*](../secgloss/h-gly.md) is decrypted using the [*public key*](../secgloss/p-gly.md) of the signer found on the signer's [*certificate*](../secgloss/c-gly.md), included as part of the signature.</span></span> <span data-ttu-id="eadc7-112">Wenn die entschlüsselte Signatur mit einem neuen Hash des ursprünglichen Dokuments übereinstimmt, wurde die Signatur vom Besitzer des privaten Schlüssels erstellt, der dem öffentlichen Schlüssel zugeordnet ist, der zum Entschlüsseln des Hashwerts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eadc7-112">If the decrypted signature matches a new hash of the original document, the signature was created by the owner of the private key associated with the public key used to decrypt the hash.</span></span> <span data-ttu-id="eadc7-113">Außerdem wird sichergestellt, dass das Dokument, auf dem die Signatur basiert, sichergestellt ist, dass es nach dem Erstellen der Signatur nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="eadc7-113">In addition, the document that the signature is based on is guaranteed not to have been changed after the signature was created.</span></span>

<span data-ttu-id="eadc7-114">Das Zertifikat, das den öffentlichen Schlüssel und die Identität des Signatur Gebers bereitgestellt hat, kann auch auf Gültigkeit überprüft werden, z. b. ob das Zertifikat widerrufen wurde, ob das Zertifikat veraltet ist oder ob das Zertifikat von einem vertrauenswürdigen Zertifikat Aussteller ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="eadc7-114">The certificate that provided the public key and the identity of the signer can also be checked for validity including such issues as whether the certificate has been revoked, whether the certificate is out of date, or whether the certificate was issued by a trusted certificate issuer.</span></span>

<span data-ttu-id="eadc7-115">Im folgenden Beispiel werden der signierte Inhalt und das **SignedData** -Objekt aus einer Datei gelesen, und die Signatur und die Gültigkeit des Zertifikats, das zum Erstellen der Signatur verwendet wird, werden überprüft.</span><span class="sxs-lookup"><span data-stu-id="eadc7-115">In the following example, the content signed and the **SignedData** object are read in from a file and the signature and the validity of the certificate used to create the signature are checked.</span></span>

> [!Note]  
> <span data-ttu-id="eadc7-116">Wenn die Signatur nicht kryptografisch gültig ist oder das Zertifikat des Signatur Gebers ungültig ist, wird eine Ausnahme ausgelöst, und das überprüfende Programm muss die Ausnahme behandeln.</span><span class="sxs-lookup"><span data-stu-id="eadc7-116">If the signature is not cryptographically valid or the certificate of the signer is not valid, an exception is raised and the verifying program must handle the exception.</span></span> <span data-ttu-id="eadc7-117">Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eadc7-117">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="eadc7-118">Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="eadc7-118">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="eadc7-119">Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="eadc7-119">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
