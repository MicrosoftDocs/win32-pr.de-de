---
description: Vektoren von Ausnahme Handlern sind eine Erweiterung der strukturierten Ausnahmebehandlung.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Behandlung von Vektoren Ausnahmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861127"
---
# <a name="vectored-exception-handling"></a><span data-ttu-id="39844-103">Behandlung von Vektoren Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="39844-103">Vectored Exception Handling</span></span>

<span data-ttu-id="39844-104">Vektoren von Ausnahme Handlern sind eine Erweiterung der strukturierten Ausnahmebehandlung.</span><span class="sxs-lookup"><span data-stu-id="39844-104">Vectored exception handlers are an extension to structured exception handling.</span></span> <span data-ttu-id="39844-105">Eine Anwendung kann eine Funktion registrieren, um alle Ausnahmen für die Anwendung zu überwachen oder zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="39844-105">An application can register a function to watch or handle all exceptions for the application.</span></span> <span data-ttu-id="39844-106">Vektorhandler sind nicht Frame basiert. Daher können Sie einen Handler hinzufügen, der unabhängig davon, wo Sie sich in einem Aufruf Rahmen befinden, aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="39844-106">Vectored handlers are not frame-based, therefore, you can add a handler that will be called regardless of where you are in a call frame.</span></span> <span data-ttu-id="39844-107">Vektorhandler werden in der Reihenfolge aufgerufen, in der Sie hinzugefügt wurden, nachdem der Debugger eine erste Benachrichtigungs Benachrichtigung erhalten hat, aber bevor das System mit dem Entwickeln des Stapels beginnt.</span><span class="sxs-lookup"><span data-stu-id="39844-107">Vectored handlers are called in the order that they were added, after the debugger gets a first chance notification, but before the system begins unwinding the stack.</span></span>

<span data-ttu-id="39844-108">Verwenden Sie die [**addvectoredcontinuehandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) -Funktion, um einen Vektoren Continue-Handler hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39844-108">To add a vectored continue handler, use the [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) function.</span></span> <span data-ttu-id="39844-109">Verwenden Sie zum Entfernen dieses Handlers die [**removevectoredcontinuehandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="39844-109">To remove this handler, use the [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) function.</span></span>

<span data-ttu-id="39844-110">Verwenden Sie zum Hinzufügen eines Vektoren Ausnahme Handlers die [**addvectoredexceptionhandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="39844-110">To add a vectored exception handler, use the [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) function.</span></span> <span data-ttu-id="39844-111">Verwenden Sie zum Entfernen dieses Handlers die [**removevectoredexceptionhandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="39844-111">To remove this handler, use the [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) function.</span></span>

 

 
