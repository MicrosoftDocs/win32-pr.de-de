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
# <a name="protecting-the-automatic-logon-password"></a>Schützen des Kennworts für die automatische Anmeldung

Das automatische Anmelde Kennwort sollte mithilfe der [**lsastoreprivatedata**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion geschützt werden.

Im folgenden Beispiel wird gezeigt, wie das automatische Anmelde Kennwort geschützt wird. Im Beispiel wird ein Handle für das [**Policy**](../secmgmt/policy-object.md) -Objekt durch Aufrufen der [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) -Funktion abgerufen. Weitere Informationen zum **Richtlinien** Objekt und den **Richtlinien** Objekt Handles finden Sie unter **Richtlinien** Objekt und [Öffnen eines Richtlinien Objekt](../secmgmt/opening-a-policy-object-handle.md)Handles. Im Beispiel wird dann das geschützte Kennwort durch Aufrufen der [**lsastoreprivatedata**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion festgelegt. Beachten Sie, dass der Code das vorhandene geschützte Kennwort löscht, wenn der Aufrufer **null** für den Wert des geschützten Kennworts übergibt. Vor dem Beenden schließt der Code das Handle für das **Richtlinien** Objekt.


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



Beachten Sie Folgendes: Wenn von Winlogon kein Kennwort gefunden wird, das von der [**lsastoreprivatedata**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion gespeichert wird, wird der Wert **DefaultPassword** des Winlogon-Schlüssels (falls vorhanden) für das automatische Anmelde Kennwort verwendet.

Weitere Informationen zur automatischen Anmeldung und zum Registrierungsschlüssel Winlogon finden Sie unter [MSGina.dll Features](msgina-dll-features.md).

Weitere Informationen zum Schützen von Kenn Wörtern finden Sie unter [Handling Kennwörter](../secbp/handling-passwords.md).

 

 
