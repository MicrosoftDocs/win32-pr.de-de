---
description: Unterstützung für die Registrierung der neuen Funktionalität in einer Systemregistrierung muss in der neuen DLL zusammen mit der neuen Funktion bereitgestellt werden.
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: Registrieren der neuen Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5d56153199542c11f00a3ec23d90d35a682c5fe93f91d2978dcd4f72628219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900595"
---
# <a name="registering-the-new-functionality"></a>Registrieren der neuen Funktionalität

Unterstützung für die Registrierung der neuen Funktionalität in einer Systemregistrierung muss in der neuen DLL zusammen mit der neuen Funktion bereitgestellt werden. [OID-Supportfunktionen](cryptography-functions.md) bieten Unterstützung bei dieser Registrierung. Regsvr32.exe registriert neue Funktionen. Dieses Tool ist in Windows enthalten.

Die neue DLL muss [**DllRegisterServer-**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer-Einstiegspunkte**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) für die Verwendung durch Regsvr32.exe bereitstellen. [*CryptoAPI-Funktionen*](../secgloss/c-gly.md) wie [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) oder [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)können innerhalb dieser Einstiegspunkte verwendet werden, wie im folgenden Beispiel gezeigt.


```C++
//  The DllRegisterServer Entry Point
STDAPI DllRegisterServer(void)
{
    if(!CryptRegisterOIDFunction(
         X509_ASN_ENCODING,                  // Encoding type
         CRYPT_OID_ENCODE_OBJECT_FUNC,       // Function name
         szOID_NEW_CERTIFICATE_TYPE,         // OID
         L"NewCert.dll",                     // Dll name
         L"NewCertificateTypeEncodeObject"   // Override function
         ))                                  //   name
       {
         return E_FAIL;
       }
    else
       {
         return S_OK;
       }
}

// The DllUnregisterServer Entry Point
STDAPI DllUnregisterServer(void)
{
    HRESULT     hr = S_OK;

    if(!CryptUnregisterOIDFunction(
          X509_ASN_ENCODING,             // Encoding type
          CRYPT_OID_ENCODE_OBJECT_FUNC,  // Function name
          szOID_NEW_CERTIFICATE_TYPE     // OID
          ))
    {
       if(ERROR_FILE_NOT_FOUND != GetLastError())
               hr = E_FAIL;
    }
    return hr;
}
```



Dieses Beispiel muss kompiliert und mit der neuen DLL verknüpft werden. Diese beiden Einstiegspunkte müssen zusammen mit dem Funktionseinstiegspunkt exportiert werden.

Um die neue Funktionalität auf einem Computer zu installieren, führen Sie Regsvr32.exe über eine Eingabeaufforderung aus, und geben Sie den Namen und Pfad der neuen DLL an. Regsvr32.exe greift über den Einstiegspunkt der [**DllRegisterServer-Funktion**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) auf die [**CryptRegisterOIDFunction-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) zu und registriert die neue Funktion und DLL.

 

 
