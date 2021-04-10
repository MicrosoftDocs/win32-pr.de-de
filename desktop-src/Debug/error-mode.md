---
description: Der Fehler Modus gibt dem System an, wie die Anwendung auf schwerwiegende Fehler reagieren wird.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Fehler Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125714"
---
# <a name="error-mode"></a><span data-ttu-id="7ab3f-103">Fehler Modus</span><span class="sxs-lookup"><span data-stu-id="7ab3f-103">Error Mode</span></span>

<span data-ttu-id="7ab3f-104">Der Fehler Modus gibt dem System an, wie die Anwendung auf schwerwiegende Fehler reagieren wird.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-104">The error mode indicates to the system how the application is going to respond to serious errors.</span></span> <span data-ttu-id="7ab3f-105">Schwerwiegende Fehler sind u. a. Datenträger Fehler, nicht fertige Laufwerke, falsche Daten Ausrichtung und nicht behandelte Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-105">Serious errors include disk failure, drive-not-ready errors, data misalignment, and unhandled exceptions.</span></span> <span data-ttu-id="7ab3f-106">Dieser Fehler Modus kann entweder pro Thread oder pro Prozess verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-106">This error mode can be managed by either a per-thread or per-process basis.</span></span> <span data-ttu-id="7ab3f-107">Eine Anwendung kann es dem System ermöglichen, ein Meldungs Feld anzuzeigen, in dem der Benutzer informiert wird, dass ein Fehler aufgetreten ist, oder er kann die Fehler behandeln.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-107">An application can let the system display a message box informing the user that an error has occurred, or it can handle the errors.</span></span>

<span data-ttu-id="7ab3f-108">Verwenden Sie [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) oder den Thread spezifischen [**setthreaderrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode), um diese Fehler ohne Benutzereingriff zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-108">To handle these errors without user intervention, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) or the thread-specific [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode).</span></span> <span data-ttu-id="7ab3f-109">Nachdem eine dieser Funktionen aufgerufen und entsprechende Flags angegeben wurden, werden die entsprechenden Fehlermeldungs Felder vom System nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-109">After calling one of these functions and specifying appropriate flags, the system will not display the corresponding error message boxes.</span></span>

<span data-ttu-id="7ab3f-110">Ein Prozess kann seinen Fehler Modus mithilfe von [**geterrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) oder [**getthreaderrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)abrufen.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-110">A process can retrieve its error mode using [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) or [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span></span>

<span data-ttu-id="7ab3f-111">Die bewährte Vorgehensweise besteht darin, dass alle Anwendungen beim Start die Prozess weite Funktion " [**setterrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) " mit dem Parameter " **SEM \_ failcriticalerrors** " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-111">Best practice is that all applications call the process-wide [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with a parameter of **SEM\_FAILCRITICALERRORS** at startup.</span></span> <span data-ttu-id="7ab3f-112">Dadurch wird verhindert, dass die Anwendung im fehlermodusdialogfelder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-112">This is to prevent error mode dialogs from hanging the application.</span></span>

<span data-ttu-id="7ab3f-113">Abgesehen davon sollten Aufrufer die Thread spezifischen Versionen dieser Funktionen bevorzugen, da Sie das normale Systemverhalten weniger stören.</span><span class="sxs-lookup"><span data-stu-id="7ab3f-113">Other than that, callers should favor the thread-specific versions of these functions since they are less disruptive to the normal behavior of the system.</span></span>

 

 
