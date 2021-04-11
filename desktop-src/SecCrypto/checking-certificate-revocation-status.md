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
# <a name="checking-certificate-revocation-status"></a>Überprüfen des Zertifikats Sperr Status

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

CAPICOM ermöglicht nicht standardmäßig die Überprüfung der Zertifikat Sperrung. Die Zertifikat Sperr Überprüfung kann jedoch Programm gesteuert für ein bestimmtes Zertifikat über die **IsValid. checkflag** -Eigenschaft eines Zertifikat Objekts aktiviert werden. Nachdem der entsprechende Wert von **checkflag** festgelegt wurde, erzwingt der Zugriff auf die Eigenschaft " **IsValid. Result** " des Zertifikats Objekts oder das Erstellen des Zertifikats über den Überprüfungs Pfad mithilfe der Erstellungs Methode eines Ketten Objekts eine Sperr Überprüfung.

Im folgenden Beispiel wurde CERT als gültiges CAPICOM-Zertifikat instanziiert.


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



Das vorherige gilt für ein einzelnes Zertifikat, unabhängig davon, wie es abgerufen wurde. Das Ausführen der Sperr Überprüfung für die Zertifikate in einem [**SignedData**](signeddata.md) -Objekt unterscheidet sich nicht, da die [**Verify**](signeddata-verify.md) -Methode des **SignedData** -Objekts nicht für diesen Zweck verwendet werden kann, da die Aktivierung von CAPICOM- \_ \_ \_ Überprüfungs Signatur und \_ Zertifikat keine CRL-Überprüfung auslöst.

Stattdessen muss das **checkflag** für die einzelnen Signatur Geber Zertifikate festgelegt werden. Sehen Sie sich das folgende Beispiel an, in dem sdata als gültiges CAPICOM [**SignedData**](signeddata.md) -Objekt instanziiert wurde.


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



Das weitere Beispiel ist die Schleife über alle Zertifikate im [**SignedData**](signeddata.md) -Objekt.

 

 



