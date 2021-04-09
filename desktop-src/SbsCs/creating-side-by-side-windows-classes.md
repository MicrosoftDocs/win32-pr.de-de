---
description: Anwendungs Kontexte können zum Erstellen paralleler Windows-Klassen verwendet werden.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Erstellen paralleler Windows-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866023"
---
# <a name="creating-side-by-side-windows-classes"></a><span data-ttu-id="8e80d-103">Erstellen paralleler Windows-Klassen</span><span class="sxs-lookup"><span data-stu-id="8e80d-103">Creating Side-By-Side Windows Classes</span></span>

<span data-ttu-id="8e80d-104">Anwendungs Kontexte können zum Erstellen paralleler Windows-Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e80d-104">Application contexts can be used to create side-by-side Windows classes.</span></span> <span data-ttu-id="8e80d-105">Wenn Sie parallele Windows-Klassen verwenden, kann die Anwendung unterschiedliche Versionen einer Klasse gleichzeitig in einem übergeordneten Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e80d-105">By using side-by-side Windows classes, your application can have different versions of a class active at the same time in a lone parent window.</span></span> <span data-ttu-id="8e80d-106">Um eine Seite-an-Seite-Windows-Klasse zu erstellen, muss Ihre Anwendung vor dem Aufrufen von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) einen Aktivierungs Kontext aktivieren, um ein Handle für das neue Fenster zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8e80d-106">To create a side-by-side Windows class, your application must activate an activation context before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to obtain a handle to the new window.</span></span>

<span data-ttu-id="8e80d-107">Beispielsweise hatten die allgemeinen Windows-Steuerelemente Version 5,82 und Version 6,0 ein Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8e80d-107">For example, Windows Common Controls version 5.82 and version 6.0 both had an Edit control.</span></span> <span data-ttu-id="8e80d-108">Standardmäßig verwendet Windows das Bearbeitungs Steuerelement der Version 5,82.</span><span class="sxs-lookup"><span data-stu-id="8e80d-108">Windows defaults to using the version 5.82 Edit control.</span></span> <span data-ttu-id="8e80d-109">Um ein paralleles Fenster zu erhalten, das über das Bearbeitungs Steuerelement der Version 6,0 verfügt, kann die Anwendung vor dem Aufrufen von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) wie gewohnt auf eine Assembly verweisen, die benannte Fenster Klassen verfügbar macht, und dann den Aktivierungs Kontext aktivieren, der auf die Steuerelemente der Version 6,0 verweist.</span><span class="sxs-lookup"><span data-stu-id="8e80d-109">To obtain a side-by-side window that has the version 6.0 Edit control, before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) as usual, your application can reference an assembly that exposes named window classes and then activate the activation context that references the version 6.0 controls.</span></span>

 

 
