---
title: Verwenden des Dialog Felds "Verbindungen"
description: Die wnetconnectiondialog-Funktion erstellt ein Dialogfeld, in dem der Benutzer Netzwerkressourcen durchsuchen und verbinden kann.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315681"
---
# <a name="using-the-connections-dialog-box"></a><span data-ttu-id="8cde6-103">Verwenden des Dialog Felds "Verbindungen"</span><span class="sxs-lookup"><span data-stu-id="8cde6-103">Using the Connections Dialog Box</span></span>

<span data-ttu-id="8cde6-104">Die [**wnetconnectiondialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) -Funktion erstellt ein Dialogfeld, in dem der Benutzer Netzwerkressourcen durchsuchen und verbinden kann.</span><span class="sxs-lookup"><span data-stu-id="8cde6-104">The [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) function creates a dialog box that allows the user to browse and connect to network resources.</span></span> <span data-ttu-id="8cde6-105">Sie können auch die [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) -Funktion zum Erstellen eines Verbindungs Dialogfelds aufruft.</span><span class="sxs-lookup"><span data-stu-id="8cde6-105">You can also call the [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) function to create a connections dialog box.</span></span> <span data-ttu-id="8cde6-106">**WNetConnectionDialog1** erfordert eine [**connectdlgstruct**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8cde6-106">**WNetConnectionDialog1** requires a [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) structure.</span></span>

<span data-ttu-id="8cde6-107">Die [**wnetdisconnectdialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) -Funktion erstellt ein Dialogfeld, in dem der Benutzer die Verbindung mit Netzwerkressourcen trennen kann.</span><span class="sxs-lookup"><span data-stu-id="8cde6-107">The [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) function creates a dialog box that allows the user to disconnect from network resources.</span></span>

<span data-ttu-id="8cde6-108">Im folgenden Codebeispiel wird veranschaulicht, wie die **wnetconnectiondialog** -Funktion aufgerufen wird, um ein Dialogfeld zu erstellen, in dem Datenträger Ressourcen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8cde6-108">The following code sample demonstrates how to call the **WNetConnectionDialog** function to create a dialog box that displays disk resources.</span></span> <span data-ttu-id="8cde6-109">Wenn der Aufruf fehlschlägt, wird im Beispiel ein von der Anwendung definierter Fehlerhandler aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cde6-109">If the call fails, the sample calls an application-defined error handler.</span></span>


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



<span data-ttu-id="8cde6-110">Weitere Informationen zum Verwenden eines Anwendungs definierten Fehler Handlers finden Sie unter [Abrufen von Netzwerkfehlern](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="8cde6-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 