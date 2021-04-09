---
title: Verknüpfen mit der Remote Zugriffs-dll
description: Wenn eine Anwendung statisch mit der rasapi32-DLL verknüpft ist, kann die Anwendung nicht geladen werden, wenn der Remote Zugriffs Dienst nicht installiert ist.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858384"
---
# <a name="linking-to-the-remote-access-dll"></a><span data-ttu-id="dfa15-103">Verknüpfen mit der Remote Zugriffs-dll</span><span class="sxs-lookup"><span data-stu-id="dfa15-103">Linking to the Remote Access DLL</span></span>

<span data-ttu-id="dfa15-104">Wenn eine Anwendung statisch mit der rasapi32-DLL verknüpft ist, kann die Anwendung nicht geladen werden, wenn der Remote Zugriffs Dienst nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dfa15-104">If an application links statically to the RASAPI32 DLL, the application will fail to load if Remote Access Service is not installed.</span></span> <span data-ttu-id="dfa15-105">Eine RAS-Anwendung kann geladen werden, wenn RAS nicht mithilfe von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) zum Laden der dll und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) zum Abrufen von Zeigern auf die RAS-Funktionen installiert wird.</span><span class="sxs-lookup"><span data-stu-id="dfa15-105">A RAS application can load when RAS is not installed by using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to load the DLL, and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain pointers to the RAS functions.</span></span>

<span data-ttu-id="dfa15-106">Die RAS-Funktionen befinden sich in RASAPI32.DLL.</span><span class="sxs-lookup"><span data-stu-id="dfa15-106">The RAS functions are located in RASAPI32.DLL.</span></span> <span data-ttu-id="dfa15-107">Die Import Bibliothek für diese Funktionen ist rasapi32. LIB.</span><span class="sxs-lookup"><span data-stu-id="dfa15-107">The import library for these functions is RASAPI32.LIB.</span></span> <span data-ttu-id="dfa15-108">Um die RAS-Funktionen verwenden zu können, müssen die Programme die folgenden Dateien enthalten:</span><span class="sxs-lookup"><span data-stu-id="dfa15-108">To use the RAS functions, your programs must include the following files:</span></span>



| <span data-ttu-id="dfa15-109">Datei</span><span class="sxs-lookup"><span data-stu-id="dfa15-109">File</span></span>       | <span data-ttu-id="dfa15-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfa15-110">Description</span></span>                                                                 |
|------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="dfa15-111">Shof. Micha</span><span class="sxs-lookup"><span data-stu-id="dfa15-111">RAS.H</span></span>      | <span data-ttu-id="dfa15-112">Enthält die Prototypen, Konstanten und Strukturdefinitionen der RAS-Funktion.</span><span class="sxs-lookup"><span data-stu-id="dfa15-112">Contains the RAS function prototypes, constants, and structure definitions.</span></span> |
| <span data-ttu-id="dfa15-113">Raserror. Micha</span><span class="sxs-lookup"><span data-stu-id="dfa15-113">RASERROR.H</span></span> | <span data-ttu-id="dfa15-114">Enthält die RAS-Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="dfa15-114">Contains the RAS error codes.</span></span>                                               |



 

 

 