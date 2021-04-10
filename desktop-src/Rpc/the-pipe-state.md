---
title: Der Pipezustand
description: Auf dem-Server erstellt der-compilercompiler eine Zustands Variable, mit der Push-, Pull-und zuordnungsprozeduren koordiniert werden.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101946"
---
# <a name="the-pipe-state"></a><span data-ttu-id="0c856-103">Der Pipezustand</span><span class="sxs-lookup"><span data-stu-id="0c856-103">The Pipe State</span></span>

<span data-ttu-id="0c856-104">Auf dem-Server erstellt der-compilercompiler eine *Zustands* Variable, mit der Push-, Pull-und zuordnungsprozeduren koordiniert werden.</span><span class="sxs-lookup"><span data-stu-id="0c856-104">On the server, the MIDL compiler creates a *state* variable that coordinates push, pull, and alloc procedures.</span></span> <span data-ttu-id="0c856-105">Auf der Clientseite muss der Entwickler die *Zustands* Variable erstellen.</span><span class="sxs-lookup"><span data-stu-id="0c856-105">On the client side, the developer must create the *state* variable.</span></span> <span data-ttu-id="0c856-106">Daher ist die *Zustands* Variable auf beiden Seiten lokal – d. h., der Client und der Server behalten jeweils ihren eigenen Pipezustand.</span><span class="sxs-lookup"><span data-stu-id="0c856-106">Therefore, the *state* variable is local to both sides—that is, the client and server each maintain their own pipe state.</span></span> <span data-ttu-id="0c856-107">Der Server-Stub-Code verwaltet die Zustands Variable auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="0c856-107">The server stub code maintains the state variable on the server.</span></span> <span data-ttu-id="0c856-108">Sie sollten nicht versuchen, den Inhalt direkt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0c856-108">You should not attempt to modify its contents directly.</span></span> <span data-ttu-id="0c856-109">Der Client muss die Felder in der Pipe-Steuerelement Struktur initialisieren und seine *Zustands* Variable beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0c856-109">The client must initialize the fields in the pipe control structure and maintain its *state* variable.</span></span> <span data-ttu-id="0c856-110">Es verwendet die *State* -Variable, um zu bestimmen, wo Daten gesucht oder platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0c856-110">It uses the *state* variable to identify where to locate or place data.</span></span>

<span data-ttu-id="0c856-111">Die Client *Status* Variable kann so einfach wie ein Datei Handle sein, wenn Sie Daten aus einer Datei in eine andere übertragen.</span><span class="sxs-lookup"><span data-stu-id="0c856-111">The client *state* variable can be as simple as a file handle, if you are transferring data from one file to another.</span></span> <span data-ttu-id="0c856-112">Es kann auch eine ganze Zahl sein, die auf ein Element in einem Array verweist.</span><span class="sxs-lookup"><span data-stu-id="0c856-112">It can also be an integer that points to an element in an array.</span></span> <span data-ttu-id="0c856-113">Sie können auch eine recht komplexe Zustands Struktur definieren, um zusätzliche Aufgaben auszuführen, z. b. das Koordinieren der Push-und Pull-Routinen für einen \[ [in](/windows/desktop/Midl/in)-, [out](/windows/desktop/Midl/out-idl) - \] Parameter.</span><span class="sxs-lookup"><span data-stu-id="0c856-113">Or you can define a fairly complex state structure to perform additional tasks, such as coordinating the push and pull routines on an \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl)\] parameter.</span></span>

 

 