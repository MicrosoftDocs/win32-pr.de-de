---
description: Eine frei Hand fähige Anwendung kommuniziert mit dem Erkennungssystem über die Tablet PC Platform-APIs.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Erkennungs-API-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560861"
---
# <a name="recognition-api-architecture"></a><span data-ttu-id="14391-103">Erkennungs-API-Architektur</span><span class="sxs-lookup"><span data-stu-id="14391-103">Recognition API Architecture</span></span>

<span data-ttu-id="14391-104">Eine frei Hand fähige Anwendung kommuniziert mit dem Erkennungssystem über die Tablet PC Platform-APIs.</span><span class="sxs-lookup"><span data-stu-id="14391-104">An ink-enabled application communicates with the recognition system through the Tablet PC Platform APIs.</span></span> <span data-ttu-id="14391-105">Anwendungen verwenden das [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="14391-105">Applications use the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object to accomplish this.</span></span> <span data-ttu-id="14391-106">Die Tablet PC-Plattform interagiert mit Ihrem Erkennungs Modul, indem Sie die Schnittstellen im C-Stil verwenden, die in diesem Abschnitt dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="14391-106">The Tablet PC Platform interacts with your recognizer by using the C-style interfaces that are documented in this section.</span></span> <span data-ttu-id="14391-107">In der folgenden Abbildung zeigt der Bereich in der gestrichelten Linie, was in diesem Abschnitt dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="14391-107">In the following illustration, the area inside the dashed line shows what is documented in this section.</span></span>

![Abbildung der Erkennungs Architektur mit hervorgehobenem Erkennungs Modul](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

<span data-ttu-id="14391-109">Eine benutzerdefinierte Erkennung muss "recapis. h" enthalten (standardmäßig installiert in C: \\ Programme \\ Microsoft Tablet PC Platform SDK \\ include).</span><span class="sxs-lookup"><span data-stu-id="14391-109">A custom recognizer must include Recapis.h (installed by default in C:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include).</span></span> <span data-ttu-id="14391-110">Sofern nicht erwähnt, muss ihre Dynamic Link Library (dll) alle API-Funktionen exportieren, auch wenn Sie festlegen, dass einige von Ihnen E \_ notimpl zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="14391-110">Except where noted, your dynamic-link library (DLL) must export all of the API functions, even if you choose to have some of them return E\_NOTIMPL.</span></span>

<span data-ttu-id="14391-111">Unter keinen Umständen wird Ihre Erkennung direkt von einer frei Hand fähigen Anwendung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="14391-111">Under no circumstances will your recognizer be called directly by an ink-enabled application.</span></span> <span data-ttu-id="14391-112">Stattdessen werden von Anwendungen entweder die Automation-APIs oder die verwalteten APIs aufgerufen, um Ergebnisse von ihrer Erkennung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="14391-112">Instead, applications will call either the Automation APIs or the Managed APIs to get results from your recognizer.</span></span>

 

 



