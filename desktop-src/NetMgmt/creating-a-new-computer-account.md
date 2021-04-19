---
title: Erstellen eines neuen Computer Kontos
description: Im folgenden Codebeispiel wird veranschaulicht, wie ein neues Computer Konto mithilfe der Funktion "nettuseradd" erstellt wird.
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd02a9d2053310c50e40957e6afee6e3a4a5ab1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341941"
---
# <a name="creating-a-new-computer-account"></a>Erstellen eines neuen Computer Kontos

Im folgenden Codebeispiel wird veranschaulicht, wie ein neues Computer Konto mithilfe der Funktion " [**nettuseradd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) " erstellt wird.

Im folgenden finden Sie Überlegungen zum Verwalten von Computer Konten:

-   Der Name des Computer Kontos sollte für die Konsistenz mit Konto Verwaltungs Dienstprogrammen Großbuchstaben sein.
-   Ein Computer Konto Name hat immer ein nach gestelltes Dollarzeichen ($). Alle Funktionen, die zum Verwalten von Computer Konten verwendet werden, müssen den Computernamen so erstellen, dass das letzte Zeichen des Computer Konto namens ein Dollarzeichen ($) ist. Bei einer vertrauenswürdigen Vertrauensstellung lautet der Kontoname trustingdomainname $.
-   Die maximale Länge des Computer namens beträgt Max \_ . Computername \_ (15). Diese Länge schließt nicht das nachfolgende Dollarzeichen ($) ein.
-   Das Kennwort für ein neues Computer Konto sollte die Kleinbuchstaben Darstellung des Computer Konto namens ohne das nachfolgende Dollarzeichen ($) sein. Bei einer vertrauenswürdigen Vertrauensstellung kann das Kennwort ein beliebiger Wert sein, der mit dem auf der Vertrauens Seite der Beziehung angegebenen Wert übereinstimmt.
-   Die maximale Kenn Wort Länge ist LM20 \_ pwlen (14). Das Kennwort sollte auf diese Länge gekürzt werden, wenn der Computer Konto Name diese Länge überschreitet.
-   Das zum Zeitpunkt der Erstellung des Computer Kontos angegebene Kennwort ist nur gültig, bis das Computer Konto in der Domäne aktiv wird. Während der Aktivierung der Vertrauensstellungs Beziehung wird ein neues Kennwort eingerichtet.


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



Der Benutzer, der die Konto Verwaltungsfunktionen aufruft, muss auf dem Bereitstellungs Zielcomputer über Administrator Rechte verfügen. Im Fall vorhandener Computer Konten kann der Ersteller des Kontos das Konto unabhängig von der administrativen Mitgliedschaft verwalten. Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).

Auf dem Bereitstellungs Zielcomputer kann die Berechtigung "" festgelegt werden, um angegebenen Benutzern die Möglichkeit zu geben, Computer Konten zu erstellen. Dadurch haben nicht Administratoren die Möglichkeit, Computer Konten zu erstellen. Der Aufrufer muss dieses Privileg vor dem Hinzufügen des Computer Kontos aktivieren. Weitere Informationen zu Konto Berechtigungen finden Sie unter [Berechtigungen](/windows/desktop/SecAuthZ/privileges) und [Autorisierungs Konstanten](/windows/desktop/SecAuthZ/authorization-constants).

 

 