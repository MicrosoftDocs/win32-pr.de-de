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
# <a name="adding-certificates-to-a-certificate-store"></a><span data-ttu-id="44873-103">Hinzufügen von Zertifikaten zu einem Zertifikat Speicher</span><span class="sxs-lookup"><span data-stu-id="44873-103">Adding Certificates to a Certificate Store</span></span>

<span data-ttu-id="44873-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="44873-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="44873-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="44873-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="44873-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="44873-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="44873-107">[*Zertifikate*](../secgloss/c-gly.md) können dem [*Zertifikat Speicher*](../secgloss/c-gly.md) hinzugefügt oder daraus entfernt werden, wenn der Speicher mit Lese-/Schreibberechtigungen geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="44873-107">[*Certificates*](../secgloss/c-gly.md) can be added to or removed from [*certificate stores*](../secgloss/c-gly.md) if the store is opened with read/write permission.</span></span> <span data-ttu-id="44873-108">Die Lese-/Schreibberechtigung wird Active Directory speichern nicht erteilt.</span><span class="sxs-lookup"><span data-stu-id="44873-108">Read/write permission is not granted to Active Directory stores.</span></span> <span data-ttu-id="44873-109">Während Zertifikate hinzugefügt oder aus dem Speicher Speicher entfernt werden können, werden Änderungen in Speicher speichern zwischen den Sitzungen nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="44873-109">While certificates can be added to or removed from memory stores, changes in memory stores are not persisted between sessions.</span></span>

<span data-ttu-id="44873-110">Zertifikate können einem Zertifikat Speicher hinzugefügt werden, der mit der Lese-/Schreibberechtigung mithilfe der **Add** -Methode geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="44873-110">Certificates can be added to a certificate store that is opened with read/write permission by using the **Add** method.</span></span> <span data-ttu-id="44873-111">Ein Zertifikat kann mithilfe der **Remove** -Methode aus einem Zertifikat Speicher entfernt werden, der mit der Lese-/Schreibberechtigung geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="44873-111">A certificate can be removed from a certificate store that is opened with read/write permission by using the **Remove** method.</span></span> <span data-ttu-id="44873-112">Neue Filialen können erstellt und im aktuellen CAPICOM \_ \_ \_ -Benutzerspeicher und CAPICOM- \_ \_ Speicherorten für lokale Computer \_ gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="44873-112">New stores can be created and saved in the CAPICOM\_CURRENT\_USER\_STORE and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="44873-113">Neu erstellte Filialen an einem dieser Speicherorte können mit Lese-/Schreibberechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="44873-113">Newly created stores in either of these locations can be opened with read/write permission.</span></span>

<span data-ttu-id="44873-114">Im folgenden Beispiel werden zwei Zertifikat Speicher geöffnet.</span><span class="sxs-lookup"><span data-stu-id="44873-114">In the following example, two certificate stores are opened.</span></span> <span data-ttu-id="44873-115">Zertifikate von Subjekten mit Nachnamen, die mit F beginnen, werden aus dem Active Directory Speicher abgerufen.</span><span class="sxs-lookup"><span data-stu-id="44873-115">Certificates of subjects with last names beginning with F are retrieved from the Active Directory store.</span></span> <span data-ttu-id="44873-116">Der aktuelle CAPICOM- \_ \_ Benutzer \_ Speicher, CAPICOM \_ ca \_ Store Store, wird dann als Lese-/Schreibspeicher geöffnet, und das erste Zertifikat aus der Sammlung der Zertifikate im Active Directory Store wird den Zertifikaten im CAPICOM-ca-Speicher hinzugefügt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="44873-116">The CAPICOM\_CURRENT\_USER\_STORE, CAPICOM\_CA\_STORE store is then opened as a read/write store and the first certificate from the collection of certificates in the Active Directory store is added to the certificates in the CAPICOM\_CA\_STORE.</span></span>

<span data-ttu-id="44873-117">Zu Demonstrationszwecken zeigt das Beispiel das Öffnen von Stores im CAPICOM \_ -Speicher Speicher \_ , CAPICOM \_ Current \_ User \_ Store und CAPICOM-Speicher \_ Orte für lokale \_ Computer \_ .</span><span class="sxs-lookup"><span data-stu-id="44873-117">For demonstration purposes, the example shows the opening of stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="44873-118">Das Beispiel zeigt, wie Sie alle Zertifikate aus einem geöffneten Speicher exportieren, die exportierten Zertifikate in eine Datei schreiben, Sie wieder einlesen und in einen anderen Speicher importieren.</span><span class="sxs-lookup"><span data-stu-id="44873-118">The example shows exporting all certificates from an open store, writing the exported certificates to a file, reading them back in, and importing them into a different store.</span></span> <span data-ttu-id="44873-119">Die neu importierten Zertifikate werden aufgelistet und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44873-119">The newly imported certificates are them enumerated and displayed.</span></span>

<span data-ttu-id="44873-120">Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44873-120">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="44873-121">Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="44873-121">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="44873-122">Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="44873-122">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="44873-123">Das folgende Beispiel zeigt das Öffnen von Zertifikat speichern mithilfe der frühen Bindung in der Deklaration der **Speicher** Objekte und das Erstellen einer Instanz dieser Objekte.</span><span class="sxs-lookup"><span data-stu-id="44873-123">The following example shows opening certificate stores using early binding in the declaration of the **Store** objects and in creating an instance of those objects.</span></span>


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



 

 
