---
description: Der imm enthält eine Thread Identifikations Überprüfung, mit der bestimmt wird, ob ein aufrufenden Thread der Ersteller eines angegebenen Eingabemethoden-Kontext Handles (himc-Typs) oder Fenster Handles (HWND-Typ) ist.
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Entwickeln IME-Aware Anwendungen mit mehreren Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351482"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a><span data-ttu-id="57b46-103">Entwickeln IME-Aware Anwendungen mit mehreren Threads</span><span class="sxs-lookup"><span data-stu-id="57b46-103">Developing IME-Aware Multiple-thread Applications</span></span>

<span data-ttu-id="57b46-104">Der imm enthält eine Thread Identifikations Überprüfung, mit der bestimmt wird, ob ein aufrufenden Thread der Ersteller eines angegebenen Eingabemethoden-Kontext Handles (himc-Typs) oder Fenster Handles (HWND-Typ) ist.</span><span class="sxs-lookup"><span data-stu-id="57b46-104">The IMM includes thread identification checking that determines if a calling thread is the creator of a specified input method context handle (HIMC type) or window handle (HWND type).</span></span> <span data-ttu-id="57b46-105">Wenn der Thread nicht der Ersteller des Handles ist, tritt bei der aufgerufenen imm-Funktion ein Fehler auf, und ein nachfolgende Aufruf von [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen \_ ungültigen \_ Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="57b46-105">If the thread is not the creator of the handle, the called IMM function fails and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_ACCESS.</span></span>

> [!Note]  
> <span data-ttu-id="57b46-106">Die aktuelle imm-Architektur bietet keine Synchronisierungs Funktion für den Zugriff auf die imm-Handles.</span><span class="sxs-lookup"><span data-stu-id="57b46-106">The current IMM architecture does not provide a synchronization facility for access to IMM handles.</span></span>

 

<span data-ttu-id="57b46-107">Um die Überprüfung der Thread Identifizierung verwenden zu können, müssen die Anwendungen die folgenden Richtlinien einhalten:</span><span class="sxs-lookup"><span data-stu-id="57b46-107">To use thread identification checking, your applications must adhere to the following guidelines:</span></span>

-   <span data-ttu-id="57b46-108">Ein Thread sollte nicht auf den von einem anderen Thread erstellten Eingabe Kontext zugreifen.</span><span class="sxs-lookup"><span data-stu-id="57b46-108">A thread should not access the input context created by another thread.</span></span>
-   <span data-ttu-id="57b46-109">Ein Thread sollte einem von einem anderen Thread erstellten Fenster keinen Eingabe Kontext zuordnen und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="57b46-109">A thread should not associate an input context with a window created by another thread, and vice versa.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57b46-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57b46-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57b46-111">Verwenden des Eingabemethoden-Managers</span><span class="sxs-lookup"><span data-stu-id="57b46-111">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
