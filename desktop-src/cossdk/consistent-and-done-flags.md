---
description: Konsistente und done-Flags
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Konsistente und done-Flags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524371"
---
# <a name="consistent-and-done-flags"></a><span data-ttu-id="7d497-103">Konsistente und done-Flags</span><span class="sxs-lookup"><span data-stu-id="7d497-103">Consistent and Done Flags</span></span>

<span data-ttu-id="7d497-104">Com+ erstellt vor dem Aktivieren eines transaktionalen Objekts immer ein Kontext Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d497-104">COM+ always creates a context object before activating a transactional object.</span></span> <span data-ttu-id="7d497-105">Das Kontext Objekt enthält objektbezogene Informationen, z. b. den Ersteller und den zugehörigen Transaktions Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7d497-105">The context object holds object-related information, such as its creator and its transaction identifier.</span></span> <span data-ttu-id="7d497-106">Jedes Kontext Objekt enthält auch ein *konsistentes Flag* und ein *done-Flag*.</span><span class="sxs-lookup"><span data-stu-id="7d497-106">Each context object also contains a *consistent flag* and a *done flag*.</span></span> <span data-ttu-id="7d497-107">Diese Flags bestimmen den Status des Transaktions Objekts.</span><span class="sxs-lookup"><span data-stu-id="7d497-107">Together these flags determine the status of the transactional object.</span></span>

<span data-ttu-id="7d497-108">Das konsistente Flag gibt an, dass das Transaktions Objekt entweder konsistent oder inkonsistent ist.</span><span class="sxs-lookup"><span data-stu-id="7d497-108">The consistent flag indicates that the transactional object is either consistent or inconsistent.</span></span> <span data-ttu-id="7d497-109">Die Details, die den Zustand eines Objekts konsistent machen, sind der Programmierer.</span><span class="sxs-lookup"><span data-stu-id="7d497-109">The specific details of what makes an object's state consistent is up to the programmer.</span></span> <span data-ttu-id="7d497-110">Wenn ein Methoden Aufrufflag dieses Flag auf true festlegt, ist das Objekt konsistent.</span><span class="sxs-lookup"><span data-stu-id="7d497-110">When a method call sets this flag to True, the object is consistent.</span></span> <span data-ttu-id="7d497-111">False gibt an, dass das Objekt inkonsistent ist.</span><span class="sxs-lookup"><span data-stu-id="7d497-111">False indicates that the object is inconsistent.</span></span> <span data-ttu-id="7d497-112">Com+ legt das-Flag auf "true" fest, wenn eine Objektinstanz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d497-112">COM+ sets the flag to True when it creates an object instance.</span></span> <span data-ttu-id="7d497-113">Ein konsistentes Objekt ist bereit, mit der Transaktion fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="7d497-113">A consistent object is ready to proceed with the transaction.</span></span> <span data-ttu-id="7d497-114">Während ein Objekt aktiv bleibt, können nachfolgende Methodenaufrufe das konsistente Flag wiederholt von true auf false und umgekehrt wechseln.</span><span class="sxs-lookup"><span data-stu-id="7d497-114">While an object remains active, subsequent method calls can repeatedly switch the consistent flag from True to False and vice versa.</span></span>

<span data-ttu-id="7d497-115">Das done-Flag bestimmt die Dauer einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="7d497-115">The done flag determines the duration of a transaction.</span></span> <span data-ttu-id="7d497-116">Wenn ein Methoden Rückruf zurückgegeben wird, prüft com+ das done-Flag.</span><span class="sxs-lookup"><span data-stu-id="7d497-116">When a method call returns, COM+ inspects the done flag.</span></span> <span data-ttu-id="7d497-117">Wenn die Methode dieses Flag auf true festlegt, deaktiviert com+ das-Objekt und notiert das konsistente-Flag.</span><span class="sxs-lookup"><span data-stu-id="7d497-117">If the method sets this flag to True, COM+ deactivates the object and notes the consistent flag.</span></span> <span data-ttu-id="7d497-118">Wenn das done-Flag false ist, deaktiviert com+ das Objekt weder und bemerkt auch das konsistente Flag.</span><span class="sxs-lookup"><span data-stu-id="7d497-118">When the done flag is False, COM+ neither deactivates the object nor notes the consistent flag.</span></span> <span data-ttu-id="7d497-119">Com+ legt das done-Flag auf "false" fest, wenn eine Objektinstanz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d497-119">COM+ sets the done flag to False when it creates an object instance.</span></span>

<span data-ttu-id="7d497-120">Das konsistente Flag wandelt eine Stimme ein, um das Commit auszuführen oder die Transaktion abzubrechen, in der es ausgeführt wird, und das done-Flag schließt die Stimme ab.</span><span class="sxs-lookup"><span data-stu-id="7d497-120">The consistent flag casts a vote to commit or abort the transaction in which it executes, and the done flag finalizes the vote.</span></span> <span data-ttu-id="7d497-121">Com+ prüft das konsistente Flag, wenn das done-Flag bei einem Methoden Rückruf auf true festgelegt ist oder wenn das Objekt deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="7d497-121">COM+ inspects the consistent flag when the done flag is set to True on a method call return or when the object deactivates.</span></span> <span data-ttu-id="7d497-122">Obwohl sich das konsistente Flag eines Objekts innerhalb der einzelnen Methodenaufrufe wiederholt ändern kann, wird nur die letzte Änderung gezählt.</span><span class="sxs-lookup"><span data-stu-id="7d497-122">Although an object's consistent flag can change repeatedly within each method call, only the last change counts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d497-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d497-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d497-124">Verwalten von automatischen Transaktionen in com+</span><span class="sxs-lookup"><span data-stu-id="7d497-124">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[<span data-ttu-id="7d497-125">Festlegen der konsistenten und done-Flags</span><span class="sxs-lookup"><span data-stu-id="7d497-125">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



