---
title: ACF-Attribute der Stub-Optimierung
description: Diese Attribute ermöglichen es Ihnen, die Größe und Geschwindigkeit Ihres stubcodes zu optimieren.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF-Mittell, Attribute, Stub-Optimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855883"
---
# <a name="stub-optimization-acf-attributes"></a><span data-ttu-id="93b86-104">ACF-Attribute der Stub-Optimierung</span><span class="sxs-lookup"><span data-stu-id="93b86-104">Stub Optimization ACF Attributes</span></span>

<span data-ttu-id="93b86-105">Diese Attribute ermöglichen es Ihnen, die Größe und Geschwindigkeit Ihres stubcodes zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="93b86-105">These attributes enable you to optimize the size and speed of your stub code.</span></span>



| <span data-ttu-id="93b86-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="93b86-106">Attribute</span></span>                                    | <span data-ttu-id="93b86-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="93b86-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93b86-108">[](code.md)[**codenocode**](nocode.md)</span><span class="sxs-lookup"><span data-stu-id="93b86-108">[**code**](code.md)[**nocode**](nocode.md)</span></span> | <span data-ttu-id="93b86-109">Verwenden Sie die Attribute [**Code**](code.md) und [**NoCode**](nocode.md) , um zu vermeiden, dass Stub-Code für nicht verwendete Funktionen erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="93b86-109">Use the [**code**](code.md) and [**nocode**](nocode.md) attributes together to avoid generating stub code for unused functions.</span></span> <span data-ttu-id="93b86-110">Wenden Sie das **NoCode** -Attribut auf den Schnittstellen Header an, und wenden Sie das **Code** Attribut auf die Prozeduren an, die von der Client Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="93b86-110">Apply the **nocode** attribute to the interface header, and apply the **code** attribute to those procedures that the client application will implement.</span></span> <span data-ttu-id="93b86-111">Client-Stub-Code wird nur für die ausgewählten Prozeduren generiert.</span><span class="sxs-lookup"><span data-stu-id="93b86-111">Client stub code will be generated only for the selected procedures.</span></span>                                                                |
| [<span data-ttu-id="93b86-112">**optimiert**</span><span class="sxs-lookup"><span data-stu-id="93b86-112">**optimize**</span></span>](optimize.md)                 | <span data-ttu-id="93b86-113">Mit können Sie den Optimierungsgrad optimieren, den der-Mittell-Compiler beim Erzeugen von Stub-Code ausführt, indem Sie angeben, dass die Daten entweder von der gemischten oder interpretierten Methode gemarshallt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="93b86-113">Lets you fine-tune the level of optimization that the MIDL compiler performs when generating stub code, by specifying that data is to be marshaled by either the mixed-mode or interpreted method.</span></span> <span data-ttu-id="93b86-114">Sie können das [**Optimierungs**](optimize.md) Attribut auf eine Schnittstelle oder auf ausgewählte Funktionen innerhalb der Schnittstelle anwenden.</span><span class="sxs-lookup"><span data-stu-id="93b86-114">You can apply the [**optimize**](optimize.md) attribute to an interface or to selected functions within the interface.</span></span> <span data-ttu-id="93b86-115">In beiden Fällen werden die Befehlszeilen Optimierungen und alle bereits vorhandenen Standardeinstellungen von der Verwendung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="93b86-115">In either case, its use will override the command-line optimizations and any pre-existing defaults.</span></span> |



 

 

 




