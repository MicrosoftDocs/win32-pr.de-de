---
title: WPD-Programmierhandbuch
description: Dieser Programmierleitfaden konzentriert sich darauf, wie Beispielaufgaben mithilfe der WPD-Schnittstellen und -Methoden in den Schnittstellen ausgeführt werden.
ms.assetid: 87777b0b-a7a0-4032-99bb-92b717d3c452
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db13d50942c28cd4937d27a745d61d7a30a01a15
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409863"
---
# <a name="wpd-programming-guide"></a><span data-ttu-id="b71a9-103">WPD-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="b71a9-103">WPD programming guide</span></span>

<span data-ttu-id="b71a9-104">Die primäre Quelle für diesen Programmierleitfaden ist ein Beispiel, das im Paket mit dem Windows Portable Devices (WPD) Software Development Kit (SDK) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b71a9-104">The primary source for this programming guide is a sample that ships with the Windows Portable Devices (WPD) Software Development Kit (SDK).</span></span> <span data-ttu-id="b71a9-105">Dieses Beispiel namens WpdApiSample.exe besteht aus sieben CPP-Modulen.</span><span class="sxs-lookup"><span data-stu-id="b71a9-105">This sample, named WpdApiSample.exe, consists of seven .cpp modules.</span></span> <span data-ttu-id="b71a9-106">Sechs dieser Module enthalten den Code, der 26 Aufgaben veranschaulicht, die eine Anwendung mithilfe der WPD-Anwendungsprogrammierschnittstelle (APPLICATION Programming Interface, API) ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="b71a9-106">Six of these modules contain the code that demonstrates 26 tasks that an application can accomplish using the WPD application programming interface (API).</span></span>

<span data-ttu-id="b71a9-107">Die Ausnahmen von oben sind die Themen, in denen Folgendes beschrieben wird: Gerätedienstaufgaben, das Kontextmenü und Eigenschaftenblatterweiterungen; diese Themen wurden nicht aus WpdApiSample übernommen.</span><span class="sxs-lookup"><span data-stu-id="b71a9-107">The exceptions to the above are the topics that describe: device service tasks, the context menu and property sheet extensions; these topics were not taken from WpdApiSample.</span></span> <span data-ttu-id="b71a9-108">Die Gerätedienstaufgaben basieren auf dem Beispiel wpdServiceApiSample.</span><span class="sxs-lookup"><span data-stu-id="b71a9-108">The device service tasks are based on the sample named WpdServiceApiSample.</span></span> <span data-ttu-id="b71a9-109">Die Kontextmenü- und Eigenschaftenblatterweiterungen sind Codeausschnitte aus Anwendungen, die nicht im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b71a9-109">The context menu and property sheet extensions are snippets taken from applications that do not ship with the Windows SDK.</span></span>

<span data-ttu-id="b71a9-110">Die folgenden Abschnitte konzentrieren sich auf die Aufgaben, die durch diese Beispiele ausgeführt werden, und erläutern, wie diese mithilfe der WPD-Schnittstellen und einer Reihe von Methoden in diesen Schnittstellen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b71a9-110">The following sections focus on the tasks accomplished by these samples and explain how each is accomplished using the WPD interfaces and a number of the methods found in these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b71a9-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b71a9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b71a9-112">**Portable Windows-Geräte**</span><span class="sxs-lookup"><span data-stu-id="b71a9-112">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
