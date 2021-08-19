---
description: CAPICOM aktiviert standardmäßig keine Zertifikatsperrüberprüfung.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Überprüfen des Zertifikatsperrstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf1ce98e392da94fd800316fe63c5b79c8572a319c6db4246e7907eb80966d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769539"
---
# <a name="checking-certificate-revocation-status"></a>Überprüfen des Zertifikatsperrstatus

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM.](alternatives-to-using-capicom.md)\]

CAPICOM aktiviert standardmäßig keine Zertifikatsperrüberprüfung. Die Zertifikatsperrüberprüfung kann jedoch programmgesteuert für ein bestimmtes Zertifikat über die **IsValid.CheckFlag-Eigenschaft** eines Certificate-Objekts aktiviert werden. Nachdem der entsprechende Wert von **CheckFlag** festgelegt wurde, erzwingt der Zugriff auf die **IsValid.Result-Eigenschaft** des Certificate-Objekts oder das Erstellen des Überprüfungspfads des Zertifikats mithilfe der Build-Methode eines Chain-Objekts die Sperrüberprüfung.

Im folgenden Beispiel wurde das Zertifikat als gültiges CAPICOM-Zertifikat instanziiert.


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



Das obige gilt für ein einzelnes Zertifikat, unabhängig davon, wie es abgerufen wurde. Das Durchführen einer Sperrüberprüfung für die Zertifikate in einem [**SignedData-Objekt**](signeddata.md) unterscheidet sich nicht, da die [**Verify-Methode**](signeddata-verify.md) des **SignedData-Objekts** für diesen Zweck nicht verwendet werden kann, da die Aktivierung von CAPICOM \_ VERIFY SIGNATURE AND CERTIFICATE keine \_ \_ \_ Zertifikatsperrlistenüberprüfung verursacht.

Stattdessen muss das **CheckFlag** für das Zertifikat jedes Signierers festgelegt werden. Betrachten Sie das folgende Beispiel, in dem sData als gültiges CAPICOM [**SignedData-Objekt**](signeddata.md) instanziiert wurde.


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



Das zusätzliche Beispiel ist die Schleife über alle Zertifikate im [**SignedData-Objekt.**](signeddata.md)

 

 



