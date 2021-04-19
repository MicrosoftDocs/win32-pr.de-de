---
description: Die empfohlene programmgesteuerte Methode zum Festlegen von Kontexten in einer Anwendung, die nicht frei Hand fähig ist, besteht darin, die SetInputScope-Funktionen zu verwenden, um den Feldern in der Anwendung Kontext zuzuordnen.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Festlegen des Kontexts mit den "*"-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350298"
---
# <a name="setting-context-with-the-setinputscope-apis"></a><span data-ttu-id="6d0cd-103">Festlegen des Kontexts mit den "\*"-APIs</span><span class="sxs-lookup"><span data-stu-id="6d0cd-103">Setting Context with the SetInputScope APIs</span></span>

<span data-ttu-id="6d0cd-104">Die empfohlene programmgesteuerte Methode zum Festlegen von Kontexten in einer Anwendung, die nicht frei Hand fähig ist, besteht darin, die [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -Funktionen zu verwenden, um den Feldern in der Anwendung Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-104">The recommended programmatic technique for setting contexts in an application that is not ink enabled is to use the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions to associate context with the fields in the application.</span></span>

<span data-ttu-id="6d0cd-105">Das Microsoft Windows XP Tablet PC Edition Development Kit 1,7 war die erste Version von Microsoft Windows für die Bereitstellung von " [**stinputscope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)".</span><span class="sxs-lookup"><span data-stu-id="6d0cd-105">The Microsoft Windows XP Tablet PC Edition Development Kit 1.7 was the first version of Microsoft Windows to offer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span> <span data-ttu-id="6d0cd-106">Windows Vista bietet auch Unterstützung für diese Funktionen.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-106">Windows Vista also provides support for these functions.</span></span> <span data-ttu-id="6d0cd-107">Die **Definitionen** von "\*" werden in "InputScope. idl" und "InputScope. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-107">The **SetInputScope** definitions are declared in InputScope.idl and InputScope.h.</span></span> <span data-ttu-id="6d0cd-108">Weitere Informationen finden Sie unter [Text Services-Framework](../tsf/text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="6d0cd-108">For more details, see [Text Services Framework](../tsf/text-services-framework.md).</span></span>

<span data-ttu-id="6d0cd-109">Die [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -Funktionen sind die empfohlene Methode, um Kontext für Steuerelemente und Anwendungen festzulegen, für die keine frei Hand Eingabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-109">The [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions are the recommended way to set context for controls and applications that are not ink enabled.</span></span>

## <a name="common-input-scopes"></a><span data-ttu-id="6d0cd-110">Allgemeine Eingabe Bereiche</span><span class="sxs-lookup"><span data-stu-id="6d0cd-110">Common Input Scopes</span></span>

<span data-ttu-id="6d0cd-111">Mithilfe der [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -Funktionen und der definierten Gruppe allgemeiner Eingabe Bereiche, die in der [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Enumeration beschrieben werden, können Sie die Erkennungsgenauigkeit der Handschrift Erkennungsfunktionen von Microsoft verbessern.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-111">Using the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions and the defined set of common input scopes described in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration, you can improve the recognition accuracy of the Microsoft handwriting recognizers.</span></span>

> [!Note]  
> <span data-ttu-id="6d0cd-112">Die Erkennungs Tools für Englisch (USA), Englisch (Vereinigtes Königreich), Deutsch, Französisch, Italienisch, Spanisch, Niederländisch und Portugiesisch unterstützen derzeit die Verwendung der allgemeinen Eingabe Bereiche mit "\* [**tinputscope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)".</span><span class="sxs-lookup"><span data-stu-id="6d0cd-112">The recognizers for English (United States), English (United Kingdom), German, French, Italian, Spanish, Dutch, and Portuguese currently support using the common input scopes with [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span>

 

 

 
