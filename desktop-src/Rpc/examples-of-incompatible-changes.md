---
title: Beispiele für inkompatible Änderungen
description: 'Beim Umgang mit nicht kompatiblen Änderungen ist die bedauerliche Faustregel wie folgt: jede Änderung kann rückwärts inkompatibel sein, es sei denn, Sie ist gut verständlich.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037117"
---
# <a name="examples-of-incompatible-changes"></a><span data-ttu-id="3b29b-103">Beispiele für inkompatible Änderungen</span><span class="sxs-lookup"><span data-stu-id="3b29b-103">Examples of Incompatible Changes</span></span>

<span data-ttu-id="3b29b-104">Beim Umgang mit nicht kompatiblen Änderungen ist die unglücklichste Faustregel wie folgt: jede Änderung kann rückwärts inkompatibel sein, es sei denn, Sie ist gut verständlich.</span><span class="sxs-lookup"><span data-stu-id="3b29b-104">When dealing with incompatible changes, the unfortunate rule of thumb is as follows: any change can be backward incompatible, unless it is very well understood.</span></span> <span data-ttu-id="3b29b-105">Diese Regel erfordert Kenntnisse der NDR-Regeln.</span><span class="sxs-lookup"><span data-stu-id="3b29b-105">This rule requires knowledge of NDR rules.</span></span> <span data-ttu-id="3b29b-106">Wenn Sie nicht wissen, was der NDR ist, nehmen Sie keine Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="3b29b-106">If you do not know what the NDR is, do not make modifications.</span></span> <span data-ttu-id="3b29b-107">Beispiele für Änderungen, die normalerweise zu einer Zugriffsverletzung in der Anwendung führen, oder eine fehlerhafte \_ \_ Stubdaten \_ Ausnahme, die von der Mars Hall-Engine ausgelöst wird, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b29b-107">Examples of changes that typically result in an access violation in the application, or a BAD\_STUB\_DATA\_EXCEPTION raised by the marshaling engine, are as follows:</span></span>

-   <span data-ttu-id="3b29b-108">Hinzufügen einer neuen Methode in der Mitte der alten Methoden.</span><span class="sxs-lookup"><span data-stu-id="3b29b-108">Adding a new method in the middle of old methods.</span></span>
-   <span data-ttu-id="3b29b-109">Hinzufügen oder Entfernen von Parametern aus einer Methode.</span><span class="sxs-lookup"><span data-stu-id="3b29b-109">Adding or removing parameters from a method.</span></span>
-   <span data-ttu-id="3b29b-110">Ändern eines Attributs, z. b. eines Zeiger Attributs: ändern \[ \] von Ref in \[ Unique \] oder \[ ptr \] oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="3b29b-110">Changing an attribute, for example a pointer attribute: changing \[ref\] to \[unique\] or \[ptr\] or vice versa.</span></span> <span data-ttu-id="3b29b-111">Jeder Zeigertyp weist eine andere Wire-Darstellung auf.</span><span class="sxs-lookup"><span data-stu-id="3b29b-111">Each pointer type has a different wire representation.</span></span>
-   <span data-ttu-id="3b29b-112">Ändern der Größe der Daten: von "Short" zu "Long", von "char" zu "WCHAR \_ t" (Unicode), durch Hinzufügen eines Felds zu einer Struktur, Ändern der Größe eines Arrays mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="3b29b-112">Changing the size of the data: from short to long, from char to wchar\_t (unicode), adding a field to a structure, changing the size of a fixed size array.</span></span>
-   <span data-ttu-id="3b29b-113">Hinzufügen von Union-Waffen zu einer Union mit einer DEFAULT-Klausel.</span><span class="sxs-lookup"><span data-stu-id="3b29b-113">Adding union arms to a union with a default clause.</span></span>

<span data-ttu-id="3b29b-114">Einige fehlerhafte Änderungen oder unbeabsichtigte Konflikte zwischen einem Client und einem Server können wie folgt auftreten:</span><span class="sxs-lookup"><span data-stu-id="3b29b-114">Some insidious changes or unintended mismatches between a client and a server may occur as follows:</span></span>

-   <span data-ttu-id="3b29b-115">Ändern eines Members eines Verbund Typs, wie z. b. einer Struktur oder eines Arrays.</span><span class="sxs-lookup"><span data-stu-id="3b29b-115">Modifying a member of a compound type, like a structure or an array.</span></span> <span data-ttu-id="3b29b-116">Wenn sich z. b. eine Client- \_ ID von einer Ganzzahl in eine GUID ändert, wird eine Client \_ Daten Satzstruktur mit dem Feld "Client-ID" nicht \_ kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3b29b-116">For example, if a CLIENT\_ID changes from an integral to a GUID, a CLIENT\_RECORD structure with the CLIENT\_ID field becomes incompatible.</span></span> <span data-ttu-id="3b29b-117">Dies ist möglicherweise schwierig zu erkennen, wenn Sie über mehrere Ebenen der Einbettung in einen tatsächlichen Remote Parametertyp kaskadiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b29b-117">This may be difficult to detect if cascaded through several levels of embedding to an actual remote parameter type.</span></span>
-   <span data-ttu-id="3b29b-118">Ändern eines importierten Typs.</span><span class="sxs-lookup"><span data-stu-id="3b29b-118">Modifying an imported type.</span></span> <span data-ttu-id="3b29b-119">Der Typ stammt möglicherweise aus einer anderen Komponente, die nicht direkt Remote ist. Daher wurde die Änderung als kompatibel betrachtet.</span><span class="sxs-lookup"><span data-stu-id="3b29b-119">The type may be coming from a different component that does not remote directly, hence the change was thought to be compatible.</span></span>
-   <span data-ttu-id="3b29b-120">\#Die Verwendung von ifdef in einer IDL-Datei ist eine gute Idee für die Verwendung von ifdef-Typdefinitionen in einer IDL-Datei – es wird ein Notfall darauf gewartet.</span><span class="sxs-lookup"><span data-stu-id="3b29b-120">Using \#ifdef in an IDL file is a bad idea to ifdef type definitions in an IDL file—it is disaster waiting to happen.</span></span> <span data-ttu-id="3b29b-121">Aufgrund von Builds oder anderen Störungen wird ein Client unweigerlich mit einem anderen Satz von Definitionen kompiliert als der Server, und er ist schließlich inkompatibel.</span><span class="sxs-lookup"><span data-stu-id="3b29b-121">Inevitably, due to build or other glitches, a client is compiled with a different set of defines than the server, and they end up being incompatible.</span></span>

 

 




