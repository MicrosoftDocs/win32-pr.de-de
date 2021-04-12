---
description: Eine Geschäftsregel ermöglicht einer Anwendung die Verwendung von Logik zur Laufzeit, um dem Client gewährte Berechtigungen zu qualifizieren.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Geschäftsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218830"
---
# <a name="business-rules"></a><span data-ttu-id="14e16-103">Geschäftsregeln</span><span class="sxs-lookup"><span data-stu-id="14e16-103">Business Rules</span></span>

<span data-ttu-id="14e16-104">Eine Geschäftsregel ermöglicht einer Anwendung die Verwendung von Logik zur Laufzeit, um dem Client gewährte Berechtigungen zu qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="14e16-104">A business rule allows an application to use logic at run time to qualify permissions granted to the client.</span></span>

<span data-ttu-id="14e16-105">Eine Geschäftsregel ist ein Skript, das in der Programmiersprache Visual Basic Scripting Edition (VBScript) geschrieben oder mithilfe der Microsoft JScript-Entwicklungssoftware geschrieben wurde, die einem [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="14e16-105">A business rule is a script written in the Visual Basic Scripting Edition (VBScript) programming language or written using the Microsoft JScript development software that is associated with an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="14e16-106">Wenn eine Anwendung den Zugriff auf einen Vorgang überprüft, prüft der Autorisierungs-Manager zunächst, ob der aktuelle Client Zugriff auf Tasks hat, die diesen Vorgang enthalten, aber nicht mit Geschäftsregeln verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="14e16-106">When an application checks access for an operation, Authorization Manager first checks if the current client has access to any tasks that contain that operation but that are not associated with business rules.</span></span> <span data-ttu-id="14e16-107">Wenn der Zugriff auf diese Weise nicht gewährt wird, führt der Autorisierungs-Manager Geschäftsregel Skripts aus, die einer Aufgabe zugeordnet sind, die den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="14e16-107">If access is not granted this way, Authorization Manager runs business-rule scripts associated with any task that contains the operation.</span></span>

<span data-ttu-id="14e16-108">Eine Anwendung übergibt Informationen als Paar von Arrays, die die Namen und Werte von Parametern darstellen, an ein Geschäftsregel Skript.</span><span class="sxs-lookup"><span data-stu-id="14e16-108">An application passes information to a business-rule script as a pair of arrays that represent the names and values of parameters.</span></span> <span data-ttu-id="14e16-109">Das Skript hat Zugriff auf diese Parameter über ein [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) -Objekt, das beim Ausführen des Skripts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="14e16-109">The script has access to these parameters through an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is created when the script runs.</span></span>

<span data-ttu-id="14e16-110">Einem Task, der in einem Delegierten Bereich enthalten ist, kann kein Geschäftsregel Skript zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="14e16-110">A business-rule script cannot be assigned to a task contained by a delegated scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14e16-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14e16-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14e16-112">Qualifizieren des Zugriffs mit Geschäftslogik in C++</span><span class="sxs-lookup"><span data-stu-id="14e16-112">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



