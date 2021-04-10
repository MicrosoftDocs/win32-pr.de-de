---
description: Das automatische Anmelde Kennwort sollte mithilfe der lsastoreprivatedata-Funktion geschützt werden.
ms.assetid: 7bd4d725-de17-4801-bd06-8d47a777409d
title: Schützen des Kennworts für die automatische Anmeldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25508af4de64554e664426db3e786a1eca34579b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960475"
---
# <a name="protecting-the-automatic-logon-password"></a><span data-ttu-id="81bb9-103">Schützen des Kennworts für die automatische Anmeldung</span><span class="sxs-lookup"><span data-stu-id="81bb9-103">Protecting the Automatic Logon Password</span></span>

<span data-ttu-id="81bb9-104">Das automatische Anmelde Kennwort sollte mithilfe der [**lsastoreprivatedata**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="81bb9-104">The automatic logon password should be protected by using the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span>

<span data-ttu-id="81bb9-105">Im folgenden Beispiel wird gezeigt, wie das automatische Anmelde Kennwort geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="81bb9-105">The following example shows how to protect the automatic logon password.</span></span> <span data-ttu-id="81bb9-106">Im Beispiel wird ein Handle für das [**Policy**](../secmgmt/policy-object.md) -Objekt durch Aufrufen der [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="81bb9-106">The example retrieves a handle to the [**Policy**](../secmgmt/policy-object.md) object by calling the [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) function.</span></span> <span data-ttu-id="81bb9-107">Weitere Informationen zum **Richtlinien** Objekt und den **Richtlinien** Objekt Handles finden Sie unter **Richtlinien** Objekt und [Öffnen eines Richtlinien Objekt](../secmgmt/opening-a-policy-object-handle.md)Handles.</span><span class="sxs-lookup"><span data-stu-id="81bb9-107">For more information about the **Policy** object and **Policy** object handles, see **Policy** object and [Opening a Policy Object Handle](../secmgmt/opening-a-policy-object-handle.md), respectively.</span></span> <span data-ttu-id="81bb9-108">Im Beispiel wird dann das geschützte Kennwort durch Aufrufen der [**lsastoreprivatedata**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81bb9-108">The example then sets the protected password by calling the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span> <span data-ttu-id="81bb9-109">Beachten Sie, dass der Code das vorhandene geschützte Kennwort löscht, wenn der Aufrufer **null** für den Wert des geschützten Kennworts übergibt.</span><span class="sxs-lookup"><span data-stu-id="81bb9-109">Note that if the caller passes in **NULL** for the protected password value, then the code clears the existing protected password.</span></span> <span data-ttu-id="81bb9-110">Vor dem Beenden schließt der Code das Handle für das **Richtlinien** Objekt.</span><span class="sxs-lookup"><span data-stu-id="81bb9-110">Before exiting, the code closes the handle to the **Policy** object.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

DWORD UpdateDefaultPassword(WCHAR * pwszSecret)
{

    LSA_OBJECT_ATTRIBUTES ObjectAttributes;
    LSA_HANDLE LsaPolicyHandle = NULL;

    LSA_UNICODE_STRING lusSecretName;
    LSA_UNICODE_STRING lusSecretData;
    USHORT SecretNameLength;
    USHORT SecretDataLength;

    NTSTATUS ntsResult = STATUS_SUCCESS;
    DWORD dwRetCode = ERROR_SUCCESS;

    //  Object attributes are reserved, so initialize to zeros.
    ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

    //  Get a handle to the Policy object.
    ntsResult = LsaOpenPolicy(
        NULL,    // local machine
        &ObjectAttributes, 
        POLICY_CREATE_SECRET,
        &LsaPolicyHandle);

    if( STATUS_SUCCESS != ntsResult )
    {
        //  An error occurred. Display it as a win32 error code.
        dwRetCode = LsaNtStatusToWinError(ntsResult);
        wprintf(L"Failed call to LsaOpenPolicy %lu\n", dwRetCode);
        return dwRetCode;
    } 

    //  Initialize an LSA_UNICODE_STRING for the name of the
    //  private data ("DefaultPassword").
    SecretNameLength = (USHORT)wcslen(L"DefaultPassword");
    lusSecretName.Buffer = L"DefaultPassword";
    lusSecretName.Length = SecretNameLength * sizeof(WCHAR);
    lusSecretName.MaximumLength =
        (SecretNameLength+1) * sizeof(WCHAR);

    //  If the pwszSecret parameter is NULL, then clear the secret.
    if( NULL == pwszSecret )
    {
        wprintf(L"Clearing the secret...\n");
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            NULL);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }
    else
    {
        wprintf(L"Setting the secret...\n");
        //  Initialize an LSA_UNICODE_STRING for the value
        //  of the private data. 
        SecretDataLength = (USHORT)wcslen(pwszSecret);
        lusSecretData.Buffer = pwszSecret;
        lusSecretData.Length = SecretDataLength * sizeof(WCHAR);
        lusSecretData.MaximumLength =
            (SecretDataLength+1) * sizeof(WCHAR);
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            &lusSecretData);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }

    LsaClose(LsaPolicyHandle);

    if (dwRetCode != ERROR_SUCCESS)
        wprintf(L"Failed call to LsaStorePrivateData %lu\n",
            dwRetCode);
    
    return dwRetCode;

}

```



<span data-ttu-id="81bb9-111">Beachten Sie Folgendes: Wenn von Winlogon kein Kennwort gefunden wird, das von der [**lsastoreprivatedata**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion gespeichert wird, wird der Wert **DefaultPassword** des Winlogon-Schlüssels (falls vorhanden) für das automatische Anmelde Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="81bb9-111">Note that if Winlogon cannot find a password stored by the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function, it will use the **DefaultPassword** value of the Winlogon key (if it exists) for the automatic logon password.</span></span>

<span data-ttu-id="81bb9-112">Weitere Informationen zur automatischen Anmeldung und zum Registrierungsschlüssel Winlogon finden Sie unter [MSGina.dll Features](msgina-dll-features.md).</span><span class="sxs-lookup"><span data-stu-id="81bb9-112">For more information about automatic logon and the Winlogon registry key, see [MSGina.dll Features](msgina-dll-features.md).</span></span>

<span data-ttu-id="81bb9-113">Weitere Informationen zum Schützen von Kenn Wörtern finden Sie unter [Handling Kennwörter](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="81bb9-113">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

 

 
