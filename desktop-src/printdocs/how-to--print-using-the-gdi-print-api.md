---
description: In diesem Thema wird erläutert, wie Sie aus einem nativen Windows-Programm mit dem GDI-&\# 160 Drucken&\# 160; Found.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 'Vorgehensweise: Drucken mithilfe der GDI-Druck-API'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868535"
---
# <a name="how-to-print-using-the-gdi-print-api"></a><span data-ttu-id="0e9f6-103">Vorgehensweise: Drucken mithilfe der GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="0e9f6-103">How To: Print Using the GDI Print API</span></span>

<span data-ttu-id="0e9f6-104">In diesem Thema wird erläutert, wie Sie mithilfe der [GDI-Druck-API](gdi-printing.md)von einem systemeigenen Windows-Programm drucken.</span><span class="sxs-lookup"><span data-stu-id="0e9f6-104">This topic introduces how to print from a native Windows program using the [GDI Print API](gdi-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="0e9f6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0e9f6-105">Overview</span></span>

<span data-ttu-id="0e9f6-106">Das Drucken ist in der Regel ein wesentlicher Bestandteil eines systemeigenen Windows-Programms und somit kein Feature, das Sie nach dem Schreiben des Programms problemlos hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="0e9f6-106">Printing is usually an integral part of a native Windows program, so it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="0e9f6-107">Wenn Sie ein Programm für Windows 7 entwerfen, sollten Sie die Verwendung der [XPS-Druck-API](xps-printing.md) in Erwägung gezogen, um die Druck Funktionalität bereitzustellen, da Sie für die Zukunft die meisten Kompatibilitätsfunktionen bietet.</span><span class="sxs-lookup"><span data-stu-id="0e9f6-107">When designing a program for Windows 7, you should consider using the [XPS Print API](xps-printing.md) to provide the printing functionality because it provides the most compatibility for the future.</span></span> <span data-ttu-id="0e9f6-108">Programme, die unter Windows Vista und früheren Versionen von Windows ausgeführt werden müssen, verwenden wahrscheinlich die [GDI-Druck-API](gdi-printing.md) , um Druck Funktionalität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0e9f6-108">Programs that must run on Windows Vista and earlier versions of Windows will most likely use the [GDI Print API](gdi-printing.md) to provide printing functionality.</span></span> <span data-ttu-id="0e9f6-109">Die GDI-Druck-API wird auch in Windows 7 unterstützt, ist aber eingeschränkter als die XPS-Druck-API.</span><span class="sxs-lookup"><span data-stu-id="0e9f6-109">The GDI Print API is also supported in Windows 7, but it is more limited than the XPS Print API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e9f6-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e9f6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e9f6-111">Verwenden von Drucken</span><span class="sxs-lookup"><span data-stu-id="0e9f6-111">Using Printing</span></span>](using-printing.md)
</dt> <dt>

[<span data-ttu-id="0e9f6-112">Drucken aus einer Windows-Anwendung</span><span class="sxs-lookup"><span data-stu-id="0e9f6-112">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



