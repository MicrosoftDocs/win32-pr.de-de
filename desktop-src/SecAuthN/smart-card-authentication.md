---
description: Smartcardauthentifizierung
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Smartcardauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350026"
---
# <a name="smart-card-authentication"></a><span data-ttu-id="b5ad7-103">Smartcardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="b5ad7-103">Smart Card Authentication</span></span>

<span data-ttu-id="b5ad7-104">Die grundlegenden Teile des [*Smartcard-Subsystems*](../secgloss/s-gly.md) basieren auf PCs/SC-Standards (siehe Spezifikationen unter [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ).</span><span class="sxs-lookup"><span data-stu-id="b5ad7-104">The basic parts of the [*smart card subsystem*](../secgloss/s-gly.md) are based on PC/SC standards (see the specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)).</span></span> <span data-ttu-id="b5ad7-105">Diese grundlegenden Teile umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b5ad7-105">These basic parts include:</span></span>

-   <span data-ttu-id="b5ad7-106">Ein [*Ressourcen-Manager*](../secgloss/r-gly.md) , der eine Windows-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-106">A [*resource manager*](../secgloss/r-gly.md) that uses a Windows API.</span></span>
-   <span data-ttu-id="b5ad7-107">Eine [*Benutzeroberfläche*](../secgloss/u-gly.md) (UI), die mit dem Ressourcen-Manager verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-107">A [*user interface*](../secgloss/u-gly.md) (UI) that works with the resource manager.</span></span>
-   <span data-ttu-id="b5ad7-108">Mehrere Basis [*Dienstanbieter*](../secgloss/s-gly.md) , die Zugriff auf bestimmte Dienste ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-108">Several base [*service providers*](../secgloss/s-gly.md) that provide access to specific services.</span></span> <span data-ttu-id="b5ad7-109">Im Gegensatz zur Windows-API des Ressourcen-Managers verwenden Dienstanbieter ein COM-Schnittstellen Modell, um [*smartcarddienste*](../secgloss/s-gly.md) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-109">In contrast to the resource manager's Windows API, service providers use a COM interface model to provide [*smart card*](../secgloss/s-gly.md) services.</span></span>

<span data-ttu-id="b5ad7-110">Die folgende Abbildung zeigt die Beziehungen dieser Teile in der gesamten smartcardarchitektur.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-110">The following illustration shows the relationships of these parts in the overall smart card architecture.</span></span>

![smartcardarchitektur](images/smartovr2a.png)

<span data-ttu-id="b5ad7-112">Informationen dazu, wie das [*Smartcard-Subsystem*](../secgloss/s-gly.md) mit anderen im Microsoft Internet Security Framework verfügbaren Diensten funktioniert, finden [Sie unter Relation zu anderen Diensten](relation-to-other-services.md).</span><span class="sxs-lookup"><span data-stu-id="b5ad7-112">For information about how the [*smart card subsystem*](../secgloss/s-gly.md) works with other services available in the Microsoft Internet Security Framework, see [Relation to Other Services](relation-to-other-services.md).</span></span>

<span data-ttu-id="b5ad7-113">Informationen zur Smartcardauthentifizierung finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-113">For information about smart card authentication, see the following topics.</span></span>



| <span data-ttu-id="b5ad7-114">Themen</span><span class="sxs-lookup"><span data-stu-id="b5ad7-114">Topics</span></span>                                                                      | <span data-ttu-id="b5ad7-115">Inhalte</span><span class="sxs-lookup"><span data-stu-id="b5ad7-115">Contents</span></span>                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5ad7-116">Smartcardkonzepte</span><span class="sxs-lookup"><span data-stu-id="b5ad7-116">Smart Card Concepts</span></span>](smart-card-concepts.md)<br/>                   | <span data-ttu-id="b5ad7-117">Grundlegende Konzepte und Beschreibungen der Interaktion zwischen Benutzern und Smartcards.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-117">Basic concepts and description of the interaction between users and smart cards.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="b5ad7-118">Smartcard-Ressourcen-Manager</span><span class="sxs-lookup"><span data-stu-id="b5ad7-118">Smart Card Resource Manager</span></span>](smart-card-resource-manager.md)<br/>   | <span data-ttu-id="b5ad7-119">Informationen zur Resource Manager-API, die den Zugriff auf [*Leser*](../secgloss/r-gly.md) und [*Smartcards*](../secgloss/s-gly.md)verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-119">Information about the resource manager API, which manages the access to [*readers*](../secgloss/r-gly.md) and to [*smart cards*](../secgloss/s-gly.md).</span></span><br/> |
| [<span data-ttu-id="b5ad7-120">Smartcard-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="b5ad7-120">Smart Card User Interface</span></span>](smart-card-user-interface.md)<br/>       | <span data-ttu-id="b5ad7-121">Informationen zum [*Dialogfeld "Smartcard-allgemein*](../secgloss/s-gly.md)".</span><span class="sxs-lookup"><span data-stu-id="b5ad7-121">Information about the [*smart card common dialog box*](../secgloss/s-gly.md).</span></span><br/>                                                                                   |
| [<span data-ttu-id="b5ad7-122">Smartcarddienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b5ad7-122">Smart Card Service Providers</span></span>](smart-card-service-providers.md)<br/> | <span data-ttu-id="b5ad7-123">Informationen zu Schnittstellen, Befehlen und Wrappern, die Smartcardfunktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b5ad7-123">Information about interfaces, commands, and wrappers that provide smart card capabilities.</span></span><br/>                                                                                                                                              |



 

<span data-ttu-id="b5ad7-124">Darüber hinaus finden Sie aktuelle Microsoft-smartcardentwicklungen unter [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="b5ad7-124">Additionally, current Microsoft smart card developments can be found at [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx).</span></span>

 

 
