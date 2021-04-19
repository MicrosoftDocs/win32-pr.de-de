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
# <a name="creating-a-new-computer-account"></a><span data-ttu-id="2ea46-103">Erstellen eines neuen Computer Kontos</span><span class="sxs-lookup"><span data-stu-id="2ea46-103">Creating a New Computer Account</span></span>

<span data-ttu-id="2ea46-104">Im folgenden Codebeispiel wird veranschaulicht, wie ein neues Computer Konto mithilfe der Funktion " [**nettuseradd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) " erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2ea46-104">The following code sample demonstrates how to create a new computer account using the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) function.</span></span>

<span data-ttu-id="2ea46-105">Im folgenden finden Sie Überlegungen zum Verwalten von Computer Konten:</span><span class="sxs-lookup"><span data-stu-id="2ea46-105">The following are considerations for managing computer accounts:</span></span>

-   <span data-ttu-id="2ea46-106">Der Name des Computer Kontos sollte für die Konsistenz mit Konto Verwaltungs Dienstprogrammen Großbuchstaben sein.</span><span class="sxs-lookup"><span data-stu-id="2ea46-106">The computer account name should be all uppercase for consistency with account management utilities.</span></span>
-   <span data-ttu-id="2ea46-107">Ein Computer Konto Name hat immer ein nach gestelltes Dollarzeichen ($).</span><span class="sxs-lookup"><span data-stu-id="2ea46-107">A computer account name always has a trailing dollar sign ($).</span></span> <span data-ttu-id="2ea46-108">Alle Funktionen, die zum Verwalten von Computer Konten verwendet werden, müssen den Computernamen so erstellen, dass das letzte Zeichen des Computer Konto namens ein Dollarzeichen ($) ist.</span><span class="sxs-lookup"><span data-stu-id="2ea46-108">Any functions used to manage computer accounts must build the computer name such that the last character of the computer account name is a dollar sign ($).</span></span> <span data-ttu-id="2ea46-109">Bei einer vertrauenswürdigen Vertrauensstellung lautet der Kontoname trustingdomainname $.</span><span class="sxs-lookup"><span data-stu-id="2ea46-109">For interdomain trust, the account name is TrustingDomainName$.</span></span>
-   <span data-ttu-id="2ea46-110">Die maximale Länge des Computer namens beträgt Max \_ . Computername \_ (15).</span><span class="sxs-lookup"><span data-stu-id="2ea46-110">The maximum computer name length is MAX\_COMPUTERNAME\_LENGTH (15).</span></span> <span data-ttu-id="2ea46-111">Diese Länge schließt nicht das nachfolgende Dollarzeichen ($) ein.</span><span class="sxs-lookup"><span data-stu-id="2ea46-111">This length does not include the trailing dollar sign ($).</span></span>
-   <span data-ttu-id="2ea46-112">Das Kennwort für ein neues Computer Konto sollte die Kleinbuchstaben Darstellung des Computer Konto namens ohne das nachfolgende Dollarzeichen ($) sein.</span><span class="sxs-lookup"><span data-stu-id="2ea46-112">The password for a new computer account should be the lowercase representation of the computer account name, without the trailing dollar sign ($).</span></span> <span data-ttu-id="2ea46-113">Bei einer vertrauenswürdigen Vertrauensstellung kann das Kennwort ein beliebiger Wert sein, der mit dem auf der Vertrauens Seite der Beziehung angegebenen Wert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="2ea46-113">For interdomain trust, the password can be an arbitrary value that matches the value specified on the trust side of the relationship.</span></span>
-   <span data-ttu-id="2ea46-114">Die maximale Kenn Wort Länge ist LM20 \_ pwlen (14).</span><span class="sxs-lookup"><span data-stu-id="2ea46-114">The maximum password length is LM20\_PWLEN (14).</span></span> <span data-ttu-id="2ea46-115">Das Kennwort sollte auf diese Länge gekürzt werden, wenn der Computer Konto Name diese Länge überschreitet.</span><span class="sxs-lookup"><span data-stu-id="2ea46-115">The password should be truncated to this length if the computer account name exceeds this length.</span></span>
-   <span data-ttu-id="2ea46-116">Das zum Zeitpunkt der Erstellung des Computer Kontos angegebene Kennwort ist nur gültig, bis das Computer Konto in der Domäne aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="2ea46-116">The password provided at computer-account-creation time is valid only until the computer account becomes active on the domain.</span></span> <span data-ttu-id="2ea46-117">Während der Aktivierung der Vertrauensstellungs Beziehung wird ein neues Kennwort eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="2ea46-117">A new password is established during trust relationship activation.</span></span>


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



<span data-ttu-id="2ea46-118">Der Benutzer, der die Konto Verwaltungsfunktionen aufruft, muss auf dem Bereitstellungs Zielcomputer über Administrator Rechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="2ea46-118">The user that calls the account management functions must have Administrator privilege on the target computer.</span></span> <span data-ttu-id="2ea46-119">Im Fall vorhandener Computer Konten kann der Ersteller des Kontos das Konto unabhängig von der administrativen Mitgliedschaft verwalten.</span><span class="sxs-lookup"><span data-stu-id="2ea46-119">In the case of existing computer accounts, the creator of the account can manage the account, regardless of administrative membership.</span></span> <span data-ttu-id="2ea46-120">Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="2ea46-120">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="2ea46-121">Auf dem Bereitstellungs Zielcomputer kann die Berechtigung "" festgelegt werden, um angegebenen Benutzern die Möglichkeit zu geben, Computer Konten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ea46-121">The SeMachineAccountPrivilege can be granted on the target computer to give specified users the ability to create computer accounts.</span></span> <span data-ttu-id="2ea46-122">Dadurch haben nicht Administratoren die Möglichkeit, Computer Konten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ea46-122">This gives non-administrators the ability to create computer accounts.</span></span> <span data-ttu-id="2ea46-123">Der Aufrufer muss dieses Privileg vor dem Hinzufügen des Computer Kontos aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2ea46-123">The caller needs to enable this privilege prior to adding the computer account.</span></span> <span data-ttu-id="2ea46-124">Weitere Informationen zu Konto Berechtigungen finden Sie unter [Berechtigungen](/windows/desktop/SecAuthZ/privileges) und [Autorisierungs Konstanten](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="2ea46-124">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

 

 