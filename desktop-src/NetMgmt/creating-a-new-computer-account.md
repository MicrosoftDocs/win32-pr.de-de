---
title: Erstellen eines neuen Computerkontos
description: Im folgenden Codebeispiel wird veranschaulicht, wie Sie mithilfe der NetUserAdd-Funktion ein neues Computerkonto erstellen.
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9b54b3e3b157bfed33b3f2429024e005b9b859bba563c0173b2ca02ab5f499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912300"
---
# <a name="creating-a-new-computer-account"></a>Erstellen eines neuen Computerkontos

Im folgenden Codebeispiel wird veranschaulicht, wie Sie mithilfe der [**NetUserAdd-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) ein neues Computerkonto erstellen.

Im Folgenden werden Überlegungen zur Verwaltung von Computerkonten berücksichtigt:

-   Der Name des Computerkontos sollte aus Gründen der Konsistenz mit den Hilfsprogrammen für die Kontoverwaltung groß geschrieben werden.
-   Ein Computerkontoname weist immer ein nachgestelltes Dollarzeichen ($) auf. Alle Funktionen, die zum Verwalten von Computerkonten verwendet werden, müssen den Computernamen so erstellen, dass das letzte Zeichen des Computerkontonamens ein Dollarzeichen ($) ist. Bei domänenübergreifender Vertrauensstellung lautet der Kontoname TrustingDomainName$.
-   Die maximale Länge des Computernamens ist MAX \_ COMPUTERNAME \_ LENGTH (15). Diese Länge enthält nicht das nachgestellte Dollarzeichen ($).
-   Das Kennwort für ein neues Computerkonto sollte die Kleinbuchstabendarstellung des Computerkontonamens ohne das nachgestellte Dollarzeichen ($) sein. Bei domänenübergreifender Vertrauensstellung kann das Kennwort ein beliebiger Wert sein, der mit dem auf der Vertrauensstellungsseite der Beziehung angegebenen Wert übereinstimmt.
-   Die maximale Kennwortlänge beträgt LM20 \_ PWLEN (14). Das Kennwort sollte auf diese Länge abgeschnitten werden, wenn der Name des Computerkontos diese Länge überschreitet.
-   Das bei der Erstellung des Computerkontos angegebene Kennwort ist nur gültig, bis das Computerkonto in der Domäne aktiv wird. Während der Aktivierung der Vertrauensstellung wird ein neues Kennwort erstellt.


```C++
#include <windows.h>
#include <lm.h>
#pragma comment(lib, "netapi32.lib")

BOOL AddMachineAccount(
    LPWSTR wTargetComputer,
    LPWSTR MachineAccount,
    DWORD AccountType
    )
{
    LPWSTR wAccount;
    LPWSTR wPassword;
    USER_INFO_1 ui;
    DWORD cbAccount;
    DWORD cbLength;
    DWORD dwError;

    //
    // Ensure a valid computer account type was passed.
    //
    if (AccountType != UF_WORKSTATION_TRUST_ACCOUNT &&
        AccountType != UF_SERVER_TRUST_ACCOUNT &&
        AccountType != UF_INTERDOMAIN_TRUST_ACCOUNT
        ) 
    {
        SetLastError(ERROR_INVALID_PARAMETER);
        return FALSE;
    }

    //
    // Obtain number of chars in computer account name.
    //
    cbLength = cbAccount = lstrlenW(MachineAccount);

    //
    // Ensure computer name doesn't exceed maximum length.
    //
    if(cbLength > MAX_COMPUTERNAME_LENGTH) {
        SetLastError(ERROR_INVALID_ACCOUNT_NAME);
        return FALSE;
    }

    //
    // Allocate storage to contain Unicode representation of
    // computer account name + trailing $ + NULL.
    //
    wAccount=(LPWSTR)HeapAlloc(GetProcessHeap(), 0,
        (cbAccount + 1 + 1) * sizeof(WCHAR)  // Account + '$' + NULL
        );

    if(wAccount == NULL) return FALSE;

    //
    // Password is the computer account name converted to lowercase;
    //  you will convert the passed MachineAccount in place.
    //
    wPassword = MachineAccount;

    //
    // Copy MachineAccount to the wAccount buffer allocated while
    //  converting computer account name to uppercase.
    //  Convert password (in place) to lowercase.
    //
    while(cbAccount--) {
        wAccount[cbAccount] = towupper( MachineAccount[cbAccount] );
        wPassword[cbAccount] = towlower( wPassword[cbAccount] );
    }

    //
    // Computer account names have a trailing Unicode '$'.
    //
    wAccount[cbLength] = L'$';
    wAccount[cbLength + 1] = L'\0'; // terminate the string

    //
    // If the password is greater than the max allowed, truncate.
    //
    if(cbLength > LM20_PWLEN) wPassword[LM20_PWLEN] = L'\0';

    //
    // Initialize the USER_INFO_1 structure.
    //
    ZeroMemory(&ui, sizeof(ui));

    ui.usri1_name = wAccount;
    ui.usri1_password = wPassword;

    ui.usri1_flags = AccountType | UF_SCRIPT;
    ui.usri1_priv = USER_PRIV_USER;

    dwError=NetUserAdd(
                wTargetComputer,    // target computer name
                1,                  // info level
                (LPBYTE) &ui,       // buffer
                NULL
                );

    //
    // Free allocated memory.
    //
    if(wAccount) HeapFree(GetProcessHeap(), 0, wAccount);

    //
    // Indicate whether the function was successful.
    //
    if(dwError == NO_ERROR)
        return TRUE;
    else {
        SetLastError(dwError);
        return FALSE;
    }
}
```



Der Benutzer, der die Kontoverwaltungsfunktionen aufruft, muss auf dem Zielcomputer über Administratorrechte verfügen. Bei vorhandenen Computerkonten kann der Ersteller des Kontos das Konto unabhängig von der Administratormitgliedschaft verwalten. Weitere Informationen zum Aufrufen von Funktionen, die Administratorrechte erfordern, finden Sie unter [Ausführen mit speziellen Berechtigungen.](/windows/desktop/SecBP/running-with-special-privileges)

SeMachineAccountPrivilege kann auf dem Zielcomputer gewährt werden, um angegebenen Benutzern die Möglichkeit zu geben, Computerkonten zu erstellen. Dadurch können Nichtadministratoren Computerkonten erstellen. Der Aufrufer muss diese Berechtigung aktivieren, bevor er das Computerkonto hinzufügt. Weitere Informationen zu Kontoberechtigungen finden Sie unter [Berechtigungen](/windows/desktop/SecAuthZ/privileges) und [Autorisierungskonstanten.](/windows/desktop/SecAuthZ/authorization-constants)

 

 