---
title: Zugreifen auf Remote Computer
description: Sie können die Windows-Ereignisprotokoll-API verwenden, um auf Daten auf dem lokalen Computer oder auf einem Remote Computer zuzugreifen.
ms.assetid: df789981-0e1c-4d68-9bd5-5d054f1724d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0063238560ddd7f1613e94b83ecc7f27900bb3
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104101366"
---
# <a name="accessing-remote-computers"></a>Zugreifen auf Remote Computer

Sie können die Windows-Ereignisprotokoll-API verwenden, um auf Daten auf dem lokalen Computer oder auf einem Remote Computer zuzugreifen. Um auf Daten auf einem Remote Computer zuzugreifen, müssen Sie die [**evtopensession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) -Funktion aufrufen, um einen Remote Sitzungs Kontext zu erstellen. Wenn Sie diese Funktion verwenden, geben Sie den Namen des Remote Computers, mit dem Sie eine Verbindung herstellen möchten, die Benutzer Anmelde Informationen für die Verbindung und den Authentifizierungstyp an, der zum Authentifizieren des Benutzers verwendet werden soll. Um den aktuellen Benutzer anzugeben, legen Sie die Member Domäne, Benutzer und Kennwort auf **null** fest.

Wenn Sie die Windows-Ereignisprotokoll-API aufgerufen haben, übergeben Sie das Handle an den Remote Sitzungs Kontext, der von der [**evtopensession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) -Funktion zurückgegeben wird. (Um auf die Daten auf dem lokalen Computer zuzugreifen, übergeben Sie **null** , um die Standard Sitzung anzugeben.) Für den Zugriff auf Daten auf dem Remote Computer muss der Remote Computer die Windows-Firewallausnahme "Remote-Ereignisprotokoll Verwaltung" aktivieren. Andernfalls tritt beim Versuch, das Sitzungs Handle zu verwenden, ein Fehler auf, wenn der RPC \_ S-Server nicht verfügbar ist \_ \_ . Auf dem Computer, mit dem Sie eine Verbindung herstellen, muss Windows Vista oder höher ausgeführt werden.

Im folgenden Beispiel wird gezeigt, wie Sie eine Verbindung mit einem Remote Computer herstellen.


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
