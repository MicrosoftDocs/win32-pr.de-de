---
description: In com+-ressourcendispenser-Schnittstellen verwendete Typen
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: In com+-ressourcendispenser-Schnittstellen verwendete Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c4d0f62ec7c61a9bc0f189c1ee02d1868a3242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748641"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>In com+-ressourcendispenser-Schnittstellen verwendete Typen

Die folgenden Typen werden in den Resource Dispenser-Schnittstellen verwendet.



| type           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Restypid**   | Ein **DWORD** , das einen Ressourcentyp identifiziert, nicht eine bestimmte Ressource. Eine **restypid** ist normalerweise ein Zeiger auf eine-Struktur im Arbeitsspeicher des Verteilers, die den Ressourcentyp beschreibt. Der Dispenser-Manager versteht diese Struktur nicht (und ist nicht erforderlich) im Speicher des Ressourcen Verteilers. Der Dispenser-Manager verwendet **restypid** nur, um auf einen Ressourcentyp innerhalb eines Ressourcen Verteilers zu verweisen.                                                                                                                                   |
| **Resid**      | Ein **DWORD** , das eine bestimmte Ressource identifiziert, im Gegensatz zu einem Ressourcentyp. Eine **RESID** ist normalerweise eine (**void \* *_), die auf eine Struktur im Speicher des Ressourcen Verteilers verweist, der die Ressource darstellt. Der Dispenser-Manager muss diese Struktur nicht im Arbeitsspeicher des Ressourcen Verteilers verstehen. Der Dispenser-Manager verwendet _* Resid** , um auf eine bestimmte Ressource innerhalb eines Ressourcen Verteilers zu verweisen.                                                                                                                                 |
| **Sresid**     | Eine Unicode-Zeichen folgen Version von **RESID**, die in der [**ihälter:: trackresources**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) -Methode und [**ihälter:: untrackresources**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) -Methode verwendet wird. Zeichen folgen sind manchmal nützlich, wenn nur eine kleine Menge von Informationen zu einer Ressource aufgezeichnet werden muss und die gesamte Beschreibung der Ressource in der **sresid** enthalten sein kann. Insbesondere kann die Verwendung von **sresid** mitunter die Notwendigkeit einer Zuordnung im Ressourcen Verteiler ausschließen, wenn die Ressource eine Beziehung zwischen zwei (oder mehr) Dingen darstellt. |
| **Transid**    | Identifiziert eine Transaktion. Dieser Typ kann in die **ITransaction** -Schnittstelle umgewandelt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Timeinsekunden** | Gibt an, wie lange eine Ressource inaktiv sein kann, bevor Sie zerstört wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> <dt>

[Com+-Ressourcen Verteiler Schnittstellen](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



