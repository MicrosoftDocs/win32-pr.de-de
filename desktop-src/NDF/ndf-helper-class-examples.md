---
title: Beispiele für die NDF-Hilfsklassen Erweiterung
description: Diese Beispiele gelten nur, wenn Entwickler der Meinung sind, dass es erforderlich ist, die Funktionalität einer Microsoft NDF-Hilfsklasse zu erweitern, die als erweiterbar deklariert ist.
ms.assetid: 048e42f5-66d8-41c6-9e97-8da68c9ad151
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3ecf34bb8e90aad8c28f582860d44e81706e77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707073"
---
# <a name="ndf-helper-class-extension-examples"></a><span data-ttu-id="7e508-103">Beispiele für die NDF-Hilfsklassen Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7e508-103">NDF Helper Class Extension Examples</span></span>

<span data-ttu-id="7e508-104">Diese Beispiele gelten nur, wenn Entwickler der Meinung sind, dass es erforderlich ist, die Funktionalität einer Microsoft NDF-Hilfsklasse zu erweitern, die als erweiterbar deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="7e508-104">These examples apply only when developers believe it is necessary to extend the functionality of a Microsoft NDF Helper Class that is declared to be extensible.</span></span> <span data-ttu-id="7e508-105">Dies ist in der Regel nicht erforderlich, aber in einigen Fällen stellen sich besondere Diagnosemöglichkeiten aufgrund der spezifischen Hardware-oder Softwareanforderungen der Komponente selbst dar.</span><span class="sxs-lookup"><span data-stu-id="7e508-105">This is generally not necessary, but in some cases, unique diagnostic opportunities present themselves because of the specific hardware or software requirements of the component.</span></span>

<span data-ttu-id="7e508-106">Die beiden folgenden Beispiele sind miteinander verknüpft, und die erste sollte vor der Analyse der zweiten verstanden werden.</span><span class="sxs-lookup"><span data-stu-id="7e508-106">The two examples that follow are related and the first should be understood before analyzing the second.</span></span> <span data-ttu-id="7e508-107">Der erste stellt eine Implementierung einer [NDF-Hilfsklassen Erweiterung](ndf-helper-class-example.md) mithilfe einer Klasse namens simplehelperfileclass bereit.</span><span class="sxs-lookup"><span data-stu-id="7e508-107">The first provides an implementation of an [NDF Helper Class Extension](ndf-helper-class-example.md) using a class called SimpleHelperFileClass.</span></span>

<span data-ttu-id="7e508-108">Die zweite [NDF-Hilfsklassen Erweiterung mit Handoff](ndf-helper-class-example-with-handoff.md)bietet ein Beispiel für eine Erweiterung, die keine bestimmten Diagnose Tasks ausführt, sondern nur eine niedrig Integritäts Hypothese für die simplehelperfileclass im ersten Beispiel generiert.</span><span class="sxs-lookup"><span data-stu-id="7e508-108">The second, [NDF Helper Class Extension with Handoff](ndf-helper-class-example-with-handoff.md), provides an example of an extension that does not perform specific diagnostic tasks but only generates a low health hypothesis for the SimpleHelperFileClass in the first example.</span></span>

 

 




