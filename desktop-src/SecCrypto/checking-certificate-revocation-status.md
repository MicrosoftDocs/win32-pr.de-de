---
description: CAPICOM ermöglicht nicht standardmäßig die Überprüfung der Zertifikat Sperrung.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Überprüfen des Zertifikats Sperr Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada134bbca88b1a875ff27add7566116cf7334bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217291"
---
# <a name="checking-certificate-revocation-status"></a><span data-ttu-id="5698c-103">Überprüfen des Zertifikats Sperr Status</span><span class="sxs-lookup"><span data-stu-id="5698c-103">Checking Certificate Revocation Status</span></span>

<span data-ttu-id="5698c-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5698c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5698c-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5698c-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="5698c-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="5698c-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="5698c-107">CAPICOM ermöglicht nicht standardmäßig die Überprüfung der Zertifikat Sperrung.</span><span class="sxs-lookup"><span data-stu-id="5698c-107">CAPICOM does not enable certificate revocation checking by default.</span></span> <span data-ttu-id="5698c-108">Die Zertifikat Sperr Überprüfung kann jedoch Programm gesteuert für ein bestimmtes Zertifikat über die **IsValid. checkflag** -Eigenschaft eines Zertifikat Objekts aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5698c-108">However, certificate revocation checking can be enabled programmatically for a particular certificate through the **IsValid.CheckFlag** property of a Certificate object.</span></span> <span data-ttu-id="5698c-109">Nachdem der entsprechende Wert von **checkflag** festgelegt wurde, erzwingt der Zugriff auf die Eigenschaft " **IsValid. Result** " des Zertifikats Objekts oder das Erstellen des Zertifikats über den Überprüfungs Pfad mithilfe der Erstellungs Methode eines Ketten Objekts eine Sperr Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="5698c-109">After the appropriate value of **CheckFlag** has been set, accessing the Certificate object's **IsValid.Result** property or building the certificate's verification path using a Chain object's Build method forces revocation checking.</span></span>

<span data-ttu-id="5698c-110">Im folgenden Beispiel wurde CERT als gültiges CAPICOM-Zertifikat instanziiert.</span><span class="sxs-lookup"><span data-stu-id="5698c-110">In the following example, cert has been instantiated as a valid CAPICOM certificate.</span></span>


```VB
Dim cert As Certificate
Dim LocalStore As New Store

' Open the My store.
LocalStore.Open LocalStore.Open CAPICOM_CURRENT_USER_STORE, _
    CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_WRITE

' Get the first certificate in the My store.
set cert = LocalStore.Certificates.Item(1)

cert.IsValid.CheckFlag = CAPICOM_CHECK_TRUSTED_ROOT Or _ 
   CAPICOM_CHECK_TIME_VALIDITY Or _ 
   CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
   CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
If cert.IsValid.Result Then
'CERTIFICATE IS VALID!
Else
Dim chain As New Chain
     chain.Build (cert)
     If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
     End If
     If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
'THE REVOCATION STATUS COULD NOT BE DETERMINED
     End If
End If

```



<span data-ttu-id="5698c-111">Das vorherige gilt für ein einzelnes Zertifikat, unabhängig davon, wie es abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5698c-111">The preceding applies to an individual certificate, no matter how it was obtained.</span></span> <span data-ttu-id="5698c-112">Das Ausführen der Sperr Überprüfung für die Zertifikate in einem [**SignedData**](signeddata.md) -Objekt unterscheidet sich nicht, da die [**Verify**](signeddata-verify.md) -Methode des **SignedData** -Objekts nicht für diesen Zweck verwendet werden kann, da die Aktivierung von CAPICOM- \_ \_ \_ Überprüfungs Signatur und \_ Zertifikat keine CRL-Überprüfung auslöst.</span><span class="sxs-lookup"><span data-stu-id="5698c-112">Performing revocation checking on the certificates in a [**SignedData**](signeddata.md) object is no different because the **SignedData** object's [**Verify**](signeddata-verify.md) method cannot be used for this purpose because enabling CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE does not cause CRL checking.</span></span>

<span data-ttu-id="5698c-113">Stattdessen muss das **checkflag** für die einzelnen Signatur Geber Zertifikate festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5698c-113">Instead, the **CheckFlag** must be set for each signer's certificate.</span></span> <span data-ttu-id="5698c-114">Sehen Sie sich das folgende Beispiel an, in dem sdata als gültiges CAPICOM [**SignedData**](signeddata.md) -Objekt instanziiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5698c-114">Consider the following example where sData has been instantiated as a valid CAPICOM [**SignedData**](signeddata.md) object.</span></span>


```VB
Dim cert As Certificate
Dim chain As New Chain

' sData is an existing SignedData object.

For I = 1 To sData.Certificates.Count
   set cert = sData.Certificates(I) 
   cert.IsValid.CheckFlag = _ 
       CAPICOM_CHECK_TRUSTED_ROOT Or _ 
       CAPICOM_CHECK_TIME_VALIDITY Or _ 
       CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
       CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
   If cert.IsValid.Result Then
      'THE CERTIFICATE IS VALID!
   Else
      chain.Build cert
      If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
         'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
      End If
      If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
         'THE REVOCATION STATUS COULD NOT BE DETERMINED
      End If
   End If
Next I
```



<span data-ttu-id="5698c-115">Das weitere Beispiel ist die Schleife über alle Zertifikate im [**SignedData**](signeddata.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5698c-115">The additional example is the loop over all the certificates in the [**SignedData**](signeddata.md) object.</span></span>

 

 



