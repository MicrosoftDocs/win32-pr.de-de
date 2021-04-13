---
description: Im folgenden Beispielcode wird die Verwendung der Wait Chain Traversale-API veranschaulicht. Sie listet alle Threads im System auf und druckt die Warte Kette für jeden Thread.
ms.assetid: 7c5fa606-6e9b-41da-bfa9-1f066449d813
title: Verwenden von WCT
ms.topic: article
ms.date: 11/19/2019
ms.openlocfilehash: 1c0f284bf501018e4ec379a64dbbd0adc0ec026e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483299"
---
# <a name="using-wct"></a><span data-ttu-id="fe5e2-104">Verwenden von WCT</span><span class="sxs-lookup"><span data-stu-id="fe5e2-104">Using WCT</span></span>

<span data-ttu-id="fe5e2-105">Im folgenden Beispielcode wird die Verwendung der Wait Chain Traversale-API veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-105">The following sample code demonstrates the use of the wait chain traversal API.</span></span> <span data-ttu-id="fe5e2-106">Sie listet alle Threads im System auf und druckt die Warte Kette für jeden Thread.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-106">It enumerates all threads in the system and prints the wait chain for each thread.</span></span>

<span data-ttu-id="fe5e2-107">Um alle Threads im System aufzulisten, führen Sie das Beispiel ohne Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-107">To enumerate all threads in the system, run the sample with no parameters.</span></span> <span data-ttu-id="fe5e2-108">Um nur die Threads eines angegebenen Prozesses aufzulisten, führen Sie das Beispiel aus, und übergeben Sie die Prozess-ID als Parameter.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-108">To enumerate only the threads from a specified process, run the sample and pass the process identifier as a parameter.</span></span> <span data-ttu-id="fe5e2-109">Das Beispiel führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="fe5e2-109">The sample performs the following steps:</span></span>

1. <span data-ttu-id="fe5e2-110">Ruft die [registerwaitchaincomcallback](/windows/desktop/api/Wct/nf-wct-registerwaitchaincomcallback) -Funktion auf, um die com-Rückruf Funktionen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-110">Calls the [RegisterWaitChainCOMCallback](/windows/desktop/api/Wct/nf-wct-registerwaitchaincomcallback) function to register the COM callback functions.</span></span>
2. <span data-ttu-id="fe5e2-111">Ruft die [openthumwaitchainsession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) -Funktion auf, um die Warte Ketten Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-111">Calls the [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) function to create the wait chain session.</span></span>
3. <span data-ttu-id="fe5e2-112">Ruft die Funktion "- [tokenprivilegien](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " auf, um die Berechtigung "SE Debug Name" zu aktivieren \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fe5e2-112">Calls the [AdjustTokenPrivileges](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable the SE\_DEBUG\_NAME privilege.</span></span>
4. <span data-ttu-id="fe5e2-113">Ruft die [EnumProcesses](/windows/win32/api/psapi/nf-psapi-enumprocesses) -und [CreateToolhelp32Snapshot](/windows/win32/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot) -Funktionen auf, um die angegebenen Threads aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-113">Calls the [EnumProcesses](/windows/win32/api/psapi/nf-psapi-enumprocesses) and [CreateToolhelp32Snapshot](/windows/win32/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot) functions to enumerate the specified threads.</span></span>
5. <span data-ttu-id="fe5e2-114">Ruft die [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) -Funktion auf, um ein Array von [waitchain- \_ Knoten \_ Info](/windows/desktop/api/Wct/ns-wct-waitchain_node_info) -Strukturen abzurufen, die die Knoten der Warte Kette enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-114">Calls the [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) to retrieve an array of [WAITCHAIN\_NODE\_INFO](/windows/desktop/api/Wct/ns-wct-waitchain_node_info) structures that contain the nodes of the wait chain.</span></span>
6. <span data-ttu-id="fe5e2-115">Druckt Informationen aus der Warte Kette.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-115">Prints information from the wait chain.</span></span>
7. <span data-ttu-id="fe5e2-116">Ruft die [closethreadwaitchainsession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) -Funktion auf, um die Warte Kette zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-116">Calls the [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) function to clean up the wait chain.</span></span>

```C++
// Copyright (C) Microsoft. All rights reserved.

/*
 * Sample code for the Wait Chain Traversal (WCT) API.
 *
 * This program enumerates all threads in the system and prints the
 * wait chain for each of them.  It should be run from an elevated
 * command prompt to get results for services.
 *
 */

#ifndef UNICODE
 #define UNICODE
#endif

#include <windows.h>
#include <wct.h>
#include <psapi.h>
#include <tlhelp32.h>
#include <wchar.h>
#include <stdio.h>
#include <stdlib.h>

#pragma comment(lib, "Psapi.lib")
#pragma comment(lib, "Advapi32.lib")

typedef struct _STR_ARRAY
{
    CHAR Desc[32];
} STR_ARRAY;

// Human-readable names for the different synchronization types.
STR_ARRAY STR_OBJECT_TYPE[] =
{
    {"CriticalSection"},
    {"SendMessage"},
    {"Mutex"},
    {"Alpc"},
    {"Com"},
    {"ThreadWait"},
    {"ProcWait"},
    {"Thread"},
    {"ComActivation"},
    {"Unknown"},
    {"Max"}
};

// Global variable to store the WCT session handle
HWCT g_WctHandle = NULL;

// Global variable to store OLE32.DLL module handle.
HMODULE g_Ole32Hnd = NULL;

//
// Function prototypes
//

void
PrintWaitChain (
    __in DWORD ThreadId
    );


BOOL
GrantDebugPrivilege ( )
/*++

Routine Description:

    Enables the debug privilege (SE_DEBUG_NAME) for this process.
    This is necessary if we want to retrieve wait chains for processes
    not owned by the current user.

Arguments:

    None.

Return Value:

    TRUE if this privilege could be enabled; FALSE otherwise.

--*/
{
    BOOL             fSuccess    = FALSE;
    HANDLE           TokenHandle = NULL;
    TOKEN_PRIVILEGES TokenPrivileges;

    if (!OpenProcessToken(GetCurrentProcess(),
                          TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY,
                          &TokenHandle))
    {
        printf("Could not get the process token");
        goto Cleanup;
    }

    TokenPrivileges.PrivilegeCount = 1;

    if (!LookupPrivilegeValue(NULL,
                              SE_DEBUG_NAME,
                              &TokenPrivileges.Privileges[0].Luid))
    {
        printf("Couldn't lookup SeDebugPrivilege name");
        goto Cleanup;
    }

    TokenPrivileges.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;

    if (!AdjustTokenPrivileges(TokenHandle,
                               FALSE,
                               &TokenPrivileges,
                               sizeof(TokenPrivileges),
                               NULL,
                               NULL))
    {
        printf("Could not revoke the debug privilege");
        goto Cleanup;
    }

    fSuccess = TRUE;

 Cleanup:

    if (TokenHandle)
    {
        CloseHandle(TokenHandle);
    }

    return fSuccess;
}

BOOL
CheckThreads (
    __in DWORD ProcId
    )
/*++

Routine Description:

    Enumerates all threads (or optionally only threads for one
    process) in the system.  It the calls the WCT API on each of them.

Arguments:

    ProcId--Specifies the process ID to analyze.  If '0' all processes
        in the system will be checked.

Return Value:

    TRUE if processes could be checked; FALSE if a general failure
    occurred.

--*/
{
    DWORD processes[1024];
    DWORD numProcesses;
    DWORD i;

    // Try to enable the SE_DEBUG_NAME privilege for this process. 
    // Continue even if this fails--we just won't be able to retrieve
    // wait chains for processes not owned by the current user.
    if (!GrantDebugPrivilege())
    {
        printf("Could not enable the debug privilege");
    }

    // Get a list of all processes currently running.
    if (EnumProcesses(processes, sizeof(processes), &numProcesses) == FALSE)
    {
        printf("Could not enumerate processes");
        return FALSE;
    }

    for (i = 0; i < numProcesses / sizeof(DWORD); i++)
    {
        HANDLE process;
        HANDLE snapshot;

        if (processes[i] == GetCurrentProcessId())
        {
            continue;
        }

        // If the caller specified a Process ID, check if we have a match.
        if (ProcId != 0)
        {
            if (processes[i] != ProcId)
            {
                continue;
            }
        }

        // Get a handle to this process.
        process = OpenProcess(PROCESS_ALL_ACCESS, FALSE, processes[i]);
        if (process)
        {
            WCHAR file[MAX_PATH];

            printf("Process 0x%x - ", processes[i]);

            // Retrieve the executable name and print it.
            if (GetProcessImageFileName(process, file, ARRAYSIZE(file)) > 0)
            {
                PCWSTR filePart = wcsrchr(file, L'\\');
                if (filePart)
                {
                    filePart++;
                }
                else
                {
                    filePart = file;
                }

                printf("%S", filePart);
            }

            printf("\n----------------------------------\n");

            // Get a snapshot of all threads and look for the ones
            // from the relevant process
            snapshot = CreateToolhelp32Snapshot(TH32CS_SNAPTHREAD, 0);
            if (snapshot != INVALID_HANDLE_VALUE)
            {
                THREADENTRY32 thread;
                thread.dwSize = sizeof(thread);

                // Walk the thread list and print each wait chain
                if (Thread32First(snapshot, &thread))
                {
                    do
                    {
                        if (thread.th32OwnerProcessID == processes[i])
                        {
                            // Open a handle to this specific thread
                            HANDLE threadHandle = OpenThread(THREAD_ALL_ACCESS,
                                                             FALSE,
                                                             thread.th32ThreadID);
                            if (threadHandle)
                            {
                                // Check whether the thread is still running
                                DWORD exitCode;
                                GetExitCodeThread(threadHandle, &exitCode);

                                if (exitCode == STILL_ACTIVE)
                                {
                                    // Print the wait chain.
                                    PrintWaitChain(thread.th32ThreadID);
                                }

                                CloseHandle(threadHandle);
                            }
                        }
                    } while (Thread32Next(snapshot, &thread));
                }
                CloseHandle(snapshot);
            }

            CloseHandle(process);
            printf("\n");
        }
    }
    return TRUE;
}

void
PrintWaitChain (
    __in DWORD ThreadId
    )
/*++

Routine Description:

    Enumerates all threads (or optionally only threads for one
    process) in the system. It the calls the WCT API on each thread.

Arguments:

    ThreadId--Specifies the thread ID to analyze.

Return Value:

    (none)

--*/
{
    WAITCHAIN_NODE_INFO NodeInfoArray[WCT_MAX_NODE_COUNT];
    DWORD               Count, i;
    BOOL                IsCycle;

    printf("%d: ", ThreadId);

    Count = WCT_MAX_NODE_COUNT;

    // Make a synchronous WCT call to retrieve the wait chain.
    if (!GetThreadWaitChain(g_WctHandle,
                            NULL,
                            WCTP_GETINFO_ALL_FLAGS,
                            ThreadId,
                            &Count,
                            NodeInfoArray,
                            &IsCycle))
    {
        printf("Error (0X%x)\n", GetLastError());
        return;
    }

    // Check if the wait chain is too big for the array we passed in.
    if (Count > WCT_MAX_NODE_COUNT)
    {
        printf("Found additional nodes %d\n", Count);
        Count = WCT_MAX_NODE_COUNT;
    }

    // Loop over all the nodes returned and print useful information.
    for (i = 0; i < Count; i++)
    {
        switch (NodeInfoArray[i].ObjectType)
        {
            case WctThreadType:
                // A thread node contains process and thread ID.
                printf("[%x:%x:%s]->",
                       NodeInfoArray[i].ThreadObject.ProcessId,
                       NodeInfoArray[i].ThreadObject.ThreadId,
                       ((NodeInfoArray[i].ObjectStatus == WctStatusBlocked) ? "b" : "r"));
                break;

            default:
                // A synchronization object.

                // Some objects have names...
                if (NodeInfoArray[i].LockObject.ObjectName[0] != L'\0')
                {
                    printf("[%s:%S]->",
                           STR_OBJECT_TYPE[NodeInfoArray[i].ObjectType-1].Desc,
                           NodeInfoArray[i].LockObject.ObjectName);
                }
                else
                {
                    printf("[%s]->",
                           STR_OBJECT_TYPE[NodeInfoArray[i].ObjectType-1].Desc);
                }
                if (NodeInfoArray[i].ObjectStatus == WctStatusAbandoned)
                {
                    printf("<abandoned>");
                }
                break;
        }
    }

    printf("[End]");

    // Did we find a deadlock?
    if (IsCycle)
    {
        printf(" !!!Deadlock!!!");
    }

    printf("\n");
}

void
Usage ()
/*++

Routine Description:

  Print usage information to stdout.

--*/
{
    printf("\nPrints the thread wait chains for one or all processes in the system.\n\n");
    printf("\nUsage:\tWctEnum [ProcId]\n");
    printf("\t (no params) -- get the wait chains for all processes\n");
    printf("\t ProcId      -- get the wait chains for the specified process\n\n");
}

BOOL
InitCOMAccess ()
/*++

Routine Description:

    Register COM interfaces with WCT. This enables WCT to provide wait
    information if a thread is blocked on a COM call.

--*/
{
    PCOGETCALLSTATE       CallStateCallback;
    PCOGETACTIVATIONSTATE ActivationStateCallback;

    // Get a handle to OLE32.DLL. You must keep this handle around
    // for the life time for any WCT session.
    g_Ole32Hnd = LoadLibrary(L"ole32.dll");
    if (!g_Ole32Hnd)
    {
        printf("ERROR: GetModuleHandle failed: 0x%X\n", GetLastError());
        return FALSE;
    }

    // Retrieve the function addresses for the COM helper APIs.
    CallStateCallback = (PCOGETCALLSTATE)
        GetProcAddress(g_Ole32Hnd, "CoGetCallState");
    if (!CallStateCallback)
    {
        printf("ERROR: GetProcAddress failed: 0x%X\n", GetLastError());
        return FALSE;
    }

    ActivationStateCallback = (PCOGETACTIVATIONSTATE)
        GetProcAddress(g_Ole32Hnd, "CoGetActivationState");
    if (!ActivationStateCallback)
    {
        printf("ERROR: GetProcAddress failed: 0x%X\n", GetLastError());
        return FALSE;
    }

    // Register these functions with WCT.
    RegisterWaitChainCOMCallback(CallStateCallback,
                                 ActivationStateCallback);
    return TRUE;
}

int _cdecl
wmain (
    __in int argc,
    __in_ecount(argc) PWSTR* argv
    )
/*++

Routine Description:

  Main entry point for this application.

--*/
{
    int rc = 1;

    // Initialize the WCT interface to COM. Continue if this
    // fails--there just will not be COM information.
    if (!InitCOMAccess())
    {
        printf("Could not enable COM access\n");
    }

    // Open a synchronous WCT session.
    g_WctHandle = OpenThreadWaitChainSession(0, NULL);
    if (NULL == g_WctHandle)
    {
        printf("ERROR: OpenThreadWaitChainSession failed\n");
        goto Cleanup;
    }

    if (argc < 2)
    {
        // Enumerate all threads in the system.
        CheckThreads(0);
    }
    else
    {
        // Only enumerate threads in the specified process.
        //
        // Take the first command line parameter as the process ID.
        DWORD  ProcId = 0;

        ProcId = _wtoi(argv[1]);
        if (ProcId == 0)
        {
            Usage();
            goto Cleanup;
        }

        CheckThreads(ProcId);
    }

    // Close the WCT session.
    CloseThreadWaitChainSession(g_WctHandle);

    rc = 0;

 Cleanup:

    if (NULL != g_Ole32Hnd)
    {
        FreeLibrary(g_Ole32Hnd);
    }

    return rc;
}
```

## <a name="related-topics"></a><span data-ttu-id="fe5e2-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe5e2-117">Related topics</span></span>

<span data-ttu-id="fe5e2-118">[Wait Chain Traversal](wait-chain-traversal.md), [WCT Reference](wct-reference.md), [MSDN Magazine 2007 Juli-Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal), [Microsoft-Support: Beheben von Problemen mit apps von Microsoft Store](https://support.microsoft.com/help/4027498/microsoft-store-fix-problems-with-apps)</span><span class="sxs-lookup"><span data-stu-id="fe5e2-118">[Wait Chain Traversal](wait-chain-traversal.md), [WCT Reference](wct-reference.md), [MSDN Magazine 2007 July - Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal), [Microsoft Support: Fix problems with apps from Microsoft Store](https://support.microsoft.com/help/4027498/microsoft-store-fix-problems-with-apps)</span></span>
