---
title: Verwenden einer Schnittstelle für mehrere Dokumente
description: Verwenden einer Schnittstelle für mehrere Dokumente
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Mciwndregisterclass-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858222"
---
# <a name="using-a-multiple-document-interface"></a><span data-ttu-id="6f832-104">Verwenden einer Schnittstelle für mehrere Dokumente</span><span class="sxs-lookup"><span data-stu-id="6f832-104">Using a Multiple Document Interface</span></span>

<span data-ttu-id="6f832-105">Anwendungen, die eine Multiple Document Interface (MDI) verwenden, müssen möglicherweise Fenster Stile angeben, die über die [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6f832-105">Applications that use a multiple document interface (MDI) might need to specify window styles that are not available through the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="6f832-106">Für diese Anwendungen können Sie mithilfe der Funktion " [**mciwndregisterclass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) " und der Funktion " [fiatewindowex](/windows/win32/api/winuser/nf-winuser-createwindowexa) " ein mciwnd-Fenster registrieren und erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f832-106">For these applications, you can register and create an MCIWnd window by using the [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) function with the [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="6f832-107">Die **mciwndregisterclass** -Funktion registriert die Fenster Klasse des mciwnd \_ \_ -Fenster Klassen, und dann erstellt " **kreatewindowex** " eine Instanz eines mciwnd-Fensters.</span><span class="sxs-lookup"><span data-stu-id="6f832-107">The **MCIWndRegisterClass** function registers the MCIWND\_WINDOW\_CLASS window class and then **CreateWindowEx** creates an instance of an MCIWnd window.</span></span>

 

 