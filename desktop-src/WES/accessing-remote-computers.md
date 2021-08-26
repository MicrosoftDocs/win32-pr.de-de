---
title: Zugreifen auf Remotecomputer
description: Sie können die Windows Ereignisprotokoll-API verwenden, um auf Daten auf dem lokalen Computer oder auf einem Remotecomputer zuzugreifen.
ms.assetid: df789981-0e1c-4d68-9bd5-5d054f1724d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a64bf1b3bded6ba1c72231e85bc78fa7f486739741fea1391c869ad79b457e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032580"
---
# <a name="accessing-remote-computers"></a>Zugreifen auf Remotecomputer

Sie können die Windows Ereignisprotokoll-API verwenden, um auf Daten auf dem lokalen Computer oder auf einem Remotecomputer zuzugreifen. Um auf Daten auf einem Remotecomputer zu zugreifen, müssen Sie die [**EvtOpenSession-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) aufrufen, um einen Remotesitzungskontext zu erstellen. Wenn Sie diese Funktion aufrufen, geben Sie den Namen des Remotecomputers, mit dem Sie eine Verbindung herstellen möchten, die Benutzeranmeldeinformationen, die zum Herstellen der Verbindung verwendet werden, und den Authentifizierungstyp an, der zum Authentifizieren des Benutzers verwendet werden soll. Um den aktuellen Benutzer anzugeben, legen Sie die Domänen-, Benutzer- und Kennwortmitglieder auf **NULL fest.**

Wenn Sie Windows Ereignisprotokoll-API aufrufen, übergeben Sie das Handle an den Remotesitzungskontext, den die [**EvtOpenSession-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) zurückgibt. (Um auf Daten auf dem lokalen Computer zu zugreifen, übergeben Sie **NULL,** um die Standardsitzung anzugeben.) Für den Zugriff auf Daten auf dem Remotecomputer muss der Remotecomputer die Remoteereignisprotokollverwaltung Windows Firewallausnahme aktivieren. Andernfalls tritt beim Versuch, das Sitzungshandy zu verwenden, ein Fehler mit RPC \_ S \_ SERVER \_ UNAVAILABLE auf. Auf dem Computer, mit dem Sie eine Verbindung herstellen, muss Windows Vista oder höher ausgeführt werden.

Das folgende Beispiel zeigt, wie Sie eine Verbindung mit einem Remotecomputer herstellen.


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote);
void EnumProviders(EVT_HANDLE hRemote);

void main(void)
{
    EVT_HANDLE hRemote = NULL;
    LPWSTR pwsComputerName = L"<name of the remote computer goes here>";
    

    // Enumerate the registered providers on the local computer.
    wprintf(L"Registered providers on the local computer\n\n");
    EnumProviders(hRemote);

    hRemote = ConnectToRemote(pwsComputerName);
    if (NULL == hRemote)
    {
        wprintf(L"Failed to connect to remote computer. Error code is %d.\n", GetLastError());
        goto cleanup;
    }

    // Enumerate the registered providers on the remote computer.
    // To access a remote computer, the remote computer must enable 
    // Remote Event Log Management as an exception in the firewall;
    // otherwise, the remote call fails with RPC_S_SERVER_UNAVAILABLE.
    wprintf(L"\n\nRegistered providers on the remote computer\n\n");
    EnumProviders(hRemote);

cleanup:

    if (hRemote)
        EvtClose(hRemote);
}

// Create a session conext for the remote computer. Set the 
// Domain, User, and Password member to NULL to specify
// the current user.
EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote)
{
    EVT_HANDLE hRemote = NULL;
    EVT_RPC_LOGIN Credentials;

    RtlZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));
    Credentials.Server = lpwszRemote;
    Credentials.Domain = NULL; 
    Credentials.User = NULL; 
    Credentials.Password = NULL; 
    Credentials.Flags = EvtRpcLoginAuthNegotiate; 

    // This call creates a remote session context; it does not actually
    // create a connection to the remote computer. The connection to
    // the remote computer happens when you use the context.
    hRemote = EvtOpenSession(EvtRpcLogin, &Credentials, 0, 0);

    SecureZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));

    return hRemote;
}

// Enumerate the registered providers on the computer.
void EnumProviders(EVT_HANDLE hRemote)
{
    EVT_HANDLE hPublishers = NULL;
    WCHAR wszPublisherName[255 + 1];
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    hPublishers = EvtOpenPublisherEnum(hRemote, 0);
    if (NULL == hPublishers)
    {
        wprintf(L"EvtOpenPublisherEnum failed with %d\n", GetLastError());
        goto cleanup;
    }

    while (true)
    {
        if (EvtNextPublisherId(hPublishers, sizeof(wszPublisherName)/sizeof(WCHAR), wszPublisherName, &dwBufferUsed))
        {
            wprintf(L"%s\n", wszPublisherName);
        }
        else
        {
            status = GetLastError();
            if (ERROR_NO_MORE_ITEMS == status)
            {
                break;
            }
            else
            {
                wprintf(L"EvtNextPublisherId failed with 0x%ud\n", GetLastError());
            }
        }
    }

cleanup:

    if (hPublishers)
        EvtClose(hPublishers);
}
```
