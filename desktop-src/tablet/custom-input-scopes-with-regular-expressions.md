---
description: Sie können benutzerdefinierte Eingabe Bereiche mithilfe von Sprachmodellen definieren, die aus regulären Ausdrücken für Handschrift bestehen, und Sie den Feldern zuweisen. Wenn Sie z. b. eine Datenbankanwendung für Lagerteile erstellen und möchten, dass Benutzer mithilfe des Schreib Bereichs des Tablet PC-Eingabe Bereichs Teile eingeben können. Besteht die Syntax der Teilenummer aus drei Buchstaben, gefolgt von vier Zahlen gefolgt von einem anderen Buchstaben (z. b. ABC1234D), hätte die Handschrifterkennung eine schwierige Zeit, diese Eingabe zu erkennen, da Sie nicht im Sprachmodell definiert ist. Es ist kein vordefiniertes Faktoid vorhanden, das dieser Syntax entspricht, und Microsoft kann die Syntax nicht für jedes mögliche Feld einschließen, das eine Anwendung benötigt. Reguläre Ausdrücke für die Handschrift stellen eine einfache Möglichkeit für Anwendungen dar, Ihr eigenes Sprachmodell für ein bestimmtes sonderverwendungs Feld zu definieren. Beachten Sie, dass Sie bei der Arbeit in einer frei Hand fähigen Anwendung, die die Eigenschaft "Faktoid" des erkenzercontext-Objekts verwendet, nicht die Version 1-Faktoide in einem regulären Ausdruck verwenden können.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Benutzerdefinierte Eingabe Bereiche mit regulären Ausdrücken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041538"
---
# <a name="custom-input-scopes-with-regular-expressions"></a><span data-ttu-id="f6c88-106">Benutzerdefinierte Eingabe Bereiche mit regulären Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="f6c88-106">Custom Input Scopes with Regular Expressions</span></span>

<span data-ttu-id="f6c88-107">Sie können benutzerdefinierte Eingabe Bereiche mithilfe von Sprachmodellen definieren, die aus regulären Ausdrücken für Handschrift bestehen, und Sie den Feldern zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f6c88-107">You can define custom input scopes by using language models composed of regular expressions for handwriting and assigning them to fields.</span></span>

<span data-ttu-id="f6c88-108">Wenn Sie z. b. eine Datenbankanwendung für Lagerteile erstellen und möchten, dass Benutzer mithilfe des Schreib Bereichs des Tablet PC-Eingabe Bereichs Teile eingeben können.</span><span class="sxs-lookup"><span data-stu-id="f6c88-108">For example, if you are creating a database application for warehouse parts and want users to be able to enter part numbers using the Tablet PC Input Panel's writing pad.</span></span> <span data-ttu-id="f6c88-109">Besteht die Syntax der Teilenummer aus drei Buchstaben, gefolgt von vier Zahlen gefolgt von einem anderen Buchstaben (z. b. ABC1234D), hätte die Handschrifterkennung eine schwierige Zeit, diese Eingabe zu erkennen, da Sie nicht im Sprachmodell definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f6c88-109">If the part number syntax consists of three letters followed by four numbers followed by another letter (for example, ABC1234D), the handwriting recognizer would have a difficult time recognizing such input because it is not defined in the language model.</span></span> <span data-ttu-id="f6c88-110">Es ist kein vordefiniertes Faktoid vorhanden, das dieser Syntax entspricht, und Microsoft kann die Syntax nicht für jedes mögliche Feld einschließen, das eine Anwendung benötigt.</span><span class="sxs-lookup"><span data-stu-id="f6c88-110">There is no predefined factoid that corresponds to such syntax, nor can Microsoft include the syntax for every possible field an application might need.</span></span> <span data-ttu-id="f6c88-111">Reguläre Ausdrücke für die Handschrift stellen eine einfache Möglichkeit für Anwendungen dar, Ihr eigenes Sprachmodell für ein bestimmtes sonderverwendungs Feld zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f6c88-111">Handwriting regular expressions provide an easy way for applications to define their own language model for a particular special-use field.</span></span>

> [!Note]  
> <span data-ttu-id="f6c88-112">Wenn Sie in einer frei Hand fähigen Anwendung arbeiten, die die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " des " [**erkennzercontext**](inkrecognizercontext-class.md) "-Objekts verwendet, können Sie die Faktoide der Version 1 nicht in einem regulären Ausdruck verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6c88-112">When working in an ink-enabled application that uses the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object, you cannot use version 1 factoids in a regular expression.</span></span>

 

 

 



