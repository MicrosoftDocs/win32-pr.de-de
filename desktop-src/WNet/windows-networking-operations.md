---
title: Windows-Netzwerk Vorgänge
description: Eine Anwendung kann die WNET-Funktionen zum Durchsuchen, hinzufügen oder Abbrechen von Netzwerkverbindungen überall in der Netzwerk Hierarchie verwenden.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315470"
---
# <a name="windows-networking-operations"></a><span data-ttu-id="ff4a6-103">Windows-Netzwerk Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ff4a6-103">Windows Networking Operations</span></span>

<span data-ttu-id="ff4a6-104">Eine Anwendung kann die WNET-Funktionen zum Durchsuchen, hinzufügen oder Abbrechen von Netzwerkverbindungen überall in der Netzwerk Hierarchie verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff4a6-104">An application can use the WNet functions to browse, add, or cancel network connections anywhere in the network hierarchy.</span></span>

<span data-ttu-id="ff4a6-105">Eine *permanente Verbindung* ist eine Netzwerkverbindung, die vom System automatisch wieder hergestellt wird, wenn sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="ff4a6-105">A *persistent connection* is a network connection that the system automatically restores when the user logs on.</span></span> <span data-ttu-id="ff4a6-106">Sie können die Funktionen [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (oder [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) und [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) aufzurufen, um zu steuern, ob eine Netzwerkverbindung zwischen einer Sitzung und der nächsten Sitzung persistent ist.</span><span class="sxs-lookup"><span data-stu-id="ff4a6-106">You can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (or [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) and [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) functions to control whether a network connection is persistent from one session to the next.</span></span>

<span data-ttu-id="ff4a6-107">Rufen Sie die [**wnetgetuser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) -Funktion auf, um den Standardbenutzer Namen oder den Benutzernamen zu ermitteln, der zum Herstellen einer Netzwerkverbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff4a6-107">To find the default user name or the user name used to establish a network connection, call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="ff4a6-108">Zusätzlich zum Aufrufen der WNET-Funktionen kann ein Prozess auch Mailslots und Named Pipes verwenden, um mit einem anderen Prozess zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="ff4a6-108">In addition to calling the WNet functions, a process can also use mailslots and named pipes to communicate with another process.</span></span> <span data-ttu-id="ff4a6-109">Weitere Informationen finden Sie unter [Mailslots](/windows/desktop/ipc/mailslots) und [Pipes](/windows/desktop/ipc/pipes).</span><span class="sxs-lookup"><span data-stu-id="ff4a6-109">For more information, see [Mailslots](/windows/desktop/ipc/mailslots) and [Pipes](/windows/desktop/ipc/pipes).</span></span>

 

 