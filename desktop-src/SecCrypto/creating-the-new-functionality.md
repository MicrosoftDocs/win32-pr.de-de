---
description: Die folgenden Funktionen gehören zu den CryptoAPI-Funktionen, die erweitert werden können.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Erstellen der neuen Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd528e7e9cf62896c74de07f042dec0e77a7dba5fe5fee32b9b1e2eb229da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768868"
---
# <a name="creating-the-new-functionality"></a>Erstellen der neuen Funktionalität

Die folgenden Funktionen gehören zu den CryptoAPI-Funktionen, die erweitert werden können.



| CryptoAPI-Funktion                                   | OID-Funktionsname definieren                         | Zeichenfolge des OID-Funktionsnamens  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | CRYPT \_ OID \_ ENCODE \_ OBJECT \_ FUNC<br/>     | "CryptDllEncodeObject"    |
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | CRYPT \_ OID \_ DECODE \_ OBJECT \_ FUNC<br/>     | "CryptDllDecodeObject"    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | CRYPT \_ OID \_ OPEN \_ STORE \_ PROV \_ FUNC<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | CRYPT \_ OID \_ VERIFY \_ CTL \_ USAGE \_ FUNC<br/> | "CertDllVerifyCTLUsage"   |
| [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | CRYPT \_ OID \_ VERIFY \_ REVOCATION \_ FUNC<br/> | "CertDllVerifyRevocation" |



 

Bei normaler Verwendung mit einer vorhandenen OID und einem Codierungstyp wird der Code in der CryptoAPI-Funktion selbst verwendet. Wenn eine dieser Funktionen mit einer OID und einem Codierungstyp aufgerufen wird, für die code in der CryptoAPI-Funktion nicht entworfen wurde, muss eine neue Funktion mit der neuen Funktionalität in einer DLL erstellt werden. Diese DLL muss in der Registrierung registriert oder im Arbeitsspeicher installiert werden.

Wenn eine der aufgelisteten Funktionen mit der neu festgelegten OID und dem Codierungstyp aufgerufen wird, wird der Code in der neuen DLL anstelle des Codes verwendet, der als Teil der CryptoAPI-Funktion bereitgestellt wird.

Der Name der neu entwickelten Funktion kann der Name sein, der in der vorherigen Tabelle unter "Zeichenfolge des OID-Funktionsnamens" aufgeführt ist, oder ein anderer Name kann angegeben werden, wenn der neue Funktionscode registriert wird.

Die neue Funktion muss einen geeigneten Prototyp verwenden. In allen Fällen mit Ausnahme von [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)entspricht dieser Prototyp der CryptoAPI-Funktion, die die neue Funktion aufruft. Im Fall von **CertOpenStore** lautet der Prototyp wie folgt.


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> Wenn die Prototypen nicht übereinstimmen, wird der Systemstapel beschädigt.

 

Zusätzlich zur Bereitstellung des Codes für die neue Funktion in einer DLL erfordert das Erweitern der Funktionalität von [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) oder [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) eine Typdefinition für die neue C-Datenstruktur, die in einer Headerdatei platziert wird, die beim Kompilieren des Programms des Benutzers enthalten ist.

 

 




