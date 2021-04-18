---
description: Die Unterstützung für das Registrieren der neuen Funktionalität in einer Systemregistrierung muss zusammen mit der neuen Funktion in der neuen DLL bereitgestellt werden.
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: Registrieren der neuen Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470541ed9b832ad5eaa914c1a35805dbd861a843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350895"
---
# <a name="registering-the-new-functionality"></a>Registrieren der neuen Funktionalität

Die Unterstützung für das Registrieren der neuen Funktionalität in einer Systemregistrierung muss zusammen mit der neuen Funktion in der neuen DLL bereitgestellt werden. [OID-Unterstützungsfunktionen](cryptography-functions.md) bieten Unterstützung bei dieser Registrierung. Regsvr32.exe registriert neue Funktionen. Dieses Tool ist in Windows enthalten.

Die neue dll muss [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) -Einstiegspunkte zur Verwendung durch Regsvr32.exe bereitstellen. [*Kryptoapi*](../secgloss/c-gly.md) -Funktionen wie [**cryptregisteroidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) oder [**cryptunregisteroidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)können innerhalb dieser Einstiegspunkte verwendet werden, wie im folgenden Beispiel gezeigt.


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



Dieses Beispiel muss kompiliert und mit der neuen DLL verknüpft werden. Diese beiden Einstiegspunkte müssen zusammen mit dem Funktions Einstiegspunkt exportiert werden.

Um die neuen Funktionen auf einem Computer zu installieren, führen Sie Regsvr32.exe über eine Eingabeaufforderung aus, und geben Sie dabei den Namen und den Pfad der neuen DLL an. Regsvr32.exe auf die Funktion " [**cryptregisteroidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) " über den Einstiegspunkt der [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) -Funktion zugreift und die neue Funktion und dll registriert.

 

 
