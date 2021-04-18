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
# <a name="registering-the-new-functionality"></a><span data-ttu-id="fdbcc-103">Registrieren der neuen Funktionalität</span><span class="sxs-lookup"><span data-stu-id="fdbcc-103">Registering the New Functionality</span></span>

<span data-ttu-id="fdbcc-104">Die Unterstützung für das Registrieren der neuen Funktionalität in einer Systemregistrierung muss zusammen mit der neuen Funktion in der neuen DLL bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-104">Support for registering the new functionality in a system registry must be provided in the new DLL along with the new function.</span></span> <span data-ttu-id="fdbcc-105">[OID-Unterstützungsfunktionen](cryptography-functions.md) bieten Unterstützung bei dieser Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-105">[OID Support Functions](cryptography-functions.md) provide assistance with this registration.</span></span> <span data-ttu-id="fdbcc-106">Regsvr32.exe registriert neue Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-106">Regsvr32.exe registers new functions.</span></span> <span data-ttu-id="fdbcc-107">Dieses Tool ist in Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-107">This tool is included with Windows.</span></span>

<span data-ttu-id="fdbcc-108">Die neue dll muss [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) -Einstiegspunkte zur Verwendung durch Regsvr32.exe bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-108">The new DLL must provide [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) entry points for use by Regsvr32.exe.</span></span> <span data-ttu-id="fdbcc-109">[*Kryptoapi*](../secgloss/c-gly.md) -Funktionen wie [**cryptregisteroidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) oder [**cryptunregisteroidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)können innerhalb dieser Einstiegspunkte verwendet werden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-109">[*CryptoAPI*](../secgloss/c-gly.md) functions, such as [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) or [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), can be used within these entry points, as shown in the following example.</span></span>


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



<span data-ttu-id="fdbcc-110">Dieses Beispiel muss kompiliert und mit der neuen DLL verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-110">This example must be compiled and linked into the new DLL.</span></span> <span data-ttu-id="fdbcc-111">Diese beiden Einstiegspunkte müssen zusammen mit dem Funktions Einstiegspunkt exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-111">These two entry points, along with the function entry point, must be exported.</span></span>

<span data-ttu-id="fdbcc-112">Um die neuen Funktionen auf einem Computer zu installieren, führen Sie Regsvr32.exe über eine Eingabeaufforderung aus, und geben Sie dabei den Namen und den Pfad der neuen DLL an.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-112">To install the new functionality on a computer, run Regsvr32.exe from a command prompt, specifying the name and path of the new DLL.</span></span> <span data-ttu-id="fdbcc-113">Regsvr32.exe auf die Funktion " [**cryptregisteroidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) " über den Einstiegspunkt der [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) -Funktion zugreift und die neue Funktion und dll registriert.</span><span class="sxs-lookup"><span data-stu-id="fdbcc-113">Regsvr32.exe accesses the [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) function through the [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) function entry point and registers the new function and DLL.</span></span>

 

 
