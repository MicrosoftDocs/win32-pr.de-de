---
description: Die folgenden Funktionen sind unter den CryptoAPI-Funktionen, die erweitert werden können.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Erstellen der neuen Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525736"
---
# <a name="creating-the-new-functionality"></a>Erstellen der neuen Funktionalität

Die folgenden Funktionen sind unter den CryptoAPI-Funktionen, die erweitert werden können.



| CryptoAPI-Funktion                                   | OID-Funktionsname definieren                         | Name der OID-Funktionsname  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**Bei cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | Crypt \_ OID-codiercodierungsobjekt \_ \_ \_ Func<br/>     | "Cryptdllencodebug Object"    |
| [**Cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | Crypt- \_ OID- \_ Decodieren von Objekten ( \_ \_ Func)<br/>     | "Cryptdlldecodeobject"    |
| [**CertOpenStore übergebene**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | Crypt \_ OID \_ Open \_ Store \_ Prov \_ Func<br/>  | "Certdllopenstoreprov"    |
| [**Certverifyctlusage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | Crypt \_ OID \_ Verify \_ CTL \_ Usage \_ Func<br/> | "Certdllverifyctlusage"   |
| [**Certverifywiderruf**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | Sperr \_ Funktion der Crypt OID- \_ Überprüfung \_ \_<br/> | "Certdllverifywiderruf" |



 

Bei normaler Verwendung mit einer vorhandenen OID und einem Codierungstyp wird der Code in der CryptoAPI-Funktion selbst verwendet. Wenn eine dieser Funktionen mit einer OID und einem Codierungstyp aufgerufen wird, den Code in der CryptoAPI-Funktion nicht verarbeiten konnte, muss eine neue Funktion, die die neue Funktionalität enthält, in einer DLL erstellt werden. Diese DLL muss in der Registrierung registriert oder im Arbeitsspeicher installiert sein.

Wenn eine der aufgelisteten Funktionen mit der neu bezeichneten OID und dem Codierungstyp aufgerufen wird, wird der Code in der neuen dll anstelle des Codes verwendet, der als Teil der CryptoAPI-Funktion bereitgestellt wird.

Der Name der neu entwickelten Funktion kann der Name sein, der unter "OID Function Name String" in der vorherigen Tabelle aufgeführt ist, oder es kann ein anderer Name angegeben werden, wenn der neue Funktionscode registriert wird.

Die neue Funktion muss einen geeigneten Prototyp verwenden. In allen Fällen mit Ausnahme von [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)ist dieser Prototyp identisch mit der CryptoAPI-Funktion, die die neue Funktion aufruft. Im Fall von **certopeinstore** lautet der Prototyp wie folgt.


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
> Wenn die Prototypen nicht identisch sind, wird der System Stapel beschädigt.

 

Zusätzlich zur Bereitstellung des Codes für die neue Funktion in einer DLL erfordert die Erweiterung der Funktionalität von " [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) " oder " [**cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) " eine Typdefinition für die neue C-Datenstruktur, die in eine Header Datei eingefügt werden muss, wenn das Programm des Benutzers kompiliert wird.

 

 




