---
description: Ändern der Rückgabewerte durch com+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Ändern der Rückgabewerte durch com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127033"
---
# <a name="how-com-modifies-return-values"></a><span data-ttu-id="8cb85-103">Ändern der Rückgabewerte durch com+</span><span class="sxs-lookup"><span data-stu-id="8cb85-103">How COM+ Modifies Return Values</span></span>

<span data-ttu-id="8cb85-104">Com+ ändert niemals den Rückgabewert eines **HRESULT** , das einen Fehler angibt, wie z \_ . b. e unerwartete oder e \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="8cb85-104">COM+ never changes the return value of an **HRESULT** that indicates failure, such as E\_UNEXPECTED or E\_FAIL.</span></span> <span data-ttu-id="8cb85-105">Wenn ein Objekt, das die com+-Funktionalität verwendet, jedoch einen **HRESULT** -Wert zurückgibt, der einen Erfolg angibt (z. b. s \_ OK, s \_ false oder noError), konvertiert com+ manchmal das **HRESULT** in einen com+-Fehlercode, bevor es zum Aufrufer zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="8cb85-105">However, when an object using COM+ functionality returns an **HRESULT** value indicating success (such as S\_OK, S\_FALSE, or NOERROR), COM+ sometimes converts the **HRESULT** into a COM+ error code before it returns to the caller.</span></span>

<span data-ttu-id="8cb85-106">Wenn eine Anwendung z. b. \_ nach dem Aufruf von [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)den Wert OK zurückgibt, wird das **HRESULT** in den \_ abgebrochenen Kontext E konvertiert, wenn das Objekt der Stamm einer Transaktion ist, für die kein Commit ausgeführt werden kann \_ .</span><span class="sxs-lookup"><span data-stu-id="8cb85-106">For example, when an application returns S\_OK after calling [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), if the object is the root of a transaction that fails to commit, the **HRESULT** is converted to CONTEXT\_E\_ABORTED.</span></span>

<span data-ttu-id="8cb85-107">Wenn com+ einen **HRESULT** -Wert konvertiert, löscht er alle Ausgabeparameter der Methode.</span><span class="sxs-lookup"><span data-stu-id="8cb85-107">When COM+ converts an **HRESULT** value, it clears all of the method's output parameters.</span></span> <span data-ttu-id="8cb85-108">Zurückgegebene Verweise werden freigegeben, und die Werte der zurückgegebenen Objekt Zeiger werden auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8cb85-108">Returned references are released, and the values of the returned object pointers are set to **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cb85-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8cb85-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cb85-110">Fehler Isolation und FailFast-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8cb85-110">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="8cb85-111">Ermitteln der Fehlerquelle</span><span class="sxs-lookup"><span data-stu-id="8cb85-111">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="8cb85-112">Interpretieren von Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="8cb85-112">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="8cb85-113">Strategien für die Behandlung von Fehlern in com+</span><span class="sxs-lookup"><span data-stu-id="8cb85-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="8cb85-114">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="8cb85-114">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



