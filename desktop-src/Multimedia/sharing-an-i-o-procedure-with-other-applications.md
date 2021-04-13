---
title: Freigeben einer e/a-Prozedur mit anderen Anwendungen
description: Freigeben einer e/a-Prozedur mit anderen Anwendungen
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- Multimedia-Datei-e/a, freigegebene Verfahren
- Datei-e/a, freigegebene Prozeduren
- Eingabe und Ausgabe (e/a), freigegebene Prozeduren
- E/a (Eingabe und Ausgabe), freigegebene Prozeduren
- Freigeben von e/a-Prozeduren mit anderen Anwendungen
- mmioinstallioproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390197"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a><span data-ttu-id="49c1f-109">Freigeben einer e/a-Prozedur mit anderen Anwendungen</span><span class="sxs-lookup"><span data-stu-id="49c1f-109">Sharing an I/O Procedure with Other Applications</span></span>

<span data-ttu-id="49c1f-110">Wenn Sie eine e/a-Prozedur für andere Anwendungen freigeben möchten, müssen Sie eine Dynamic Link Library (dll) für Ihre Anwendung schreiben.</span><span class="sxs-lookup"><span data-stu-id="49c1f-110">If you want to share an I/O procedure with other applications, you need to write a dynamic-link library (DLL) for your application.</span></span> <span data-ttu-id="49c1f-111">Sie können die e/a-Prozedur freigeben, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="49c1f-111">You can share the I/O procedure by doing one of the following:</span></span>

-   <span data-ttu-id="49c1f-112">Fügen Sie den Code für die e/a-Prozedur in die dll ein.</span><span class="sxs-lookup"><span data-stu-id="49c1f-112">Include the code for the I/O procedure in the DLL.</span></span>
-   <span data-ttu-id="49c1f-113">Erstellen Sie eine Funktion in der dll, die die [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) -Funktion aufruft, um die e/a-Prozedur zu installieren.</span><span class="sxs-lookup"><span data-stu-id="49c1f-113">Create a function in the DLL that calls the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function to install the I/O procedure.</span></span>
-   <span data-ttu-id="49c1f-114">Exportieren Sie diese Funktion in der Modul Definitionsdatei der dll.</span><span class="sxs-lookup"><span data-stu-id="49c1f-114">Export this function in the module-definitions file of the DLL.</span></span>

<span data-ttu-id="49c1f-115">Um die freigegebene e/a-Prozedur zu verwenden, muss eine Anwendung zuerst die-Funktion in der dll zum Installieren der e/a-Prozedur aufruft.</span><span class="sxs-lookup"><span data-stu-id="49c1f-115">To use the shared I/O procedure, an application must first call the function in the DLL to install the I/O procedure.</span></span>

 

 