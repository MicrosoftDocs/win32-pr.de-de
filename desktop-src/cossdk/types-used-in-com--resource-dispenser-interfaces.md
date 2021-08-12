---
description: Typen, die in COM+-Ressourcenverteilerschnittstellen verwendet werden
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Typen, die in COM+-Ressourcenverteilerschnittstellen verwendet werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e98473ce108ea280532c2188e911b488e42669b98273b14fc229d003905b581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305230"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>Typen, die in COM+-Ressourcenverteilerschnittstellen verwendet werden

Die folgenden Typen werden in den Schnittstellen des Ressourcenverteilers verwendet.



| type           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | Ein **DWORD,** das einen Ressourcentyp identifiziert, nicht eine bestimmte Ressource. Ein **RESTYPID** ist in der Regel ein Zeiger auf eine Struktur im Speicher des Verteilers, die den Ressourcentyp beschreibt. Der Verteiler-Manager versteht diese Struktur im Speicher des Ressourcenverteilers nicht (und muss sie nicht verstehen). Der Verteiler-Manager verwendet **RESTYPID** nur, um auf einen Ressourcentyp innerhalb eines Ressourcenverteilers zu verweisen.                                                                                                                                   |
| **Resid**      | Ein **DWORD,** das eine bestimmte Ressource im Gegensatz zu einem Ressourcentyp identifiziert. Ein **RESID** ist normalerweise ein (**void \* *_), der auf eine Struktur im Speicher des Ressourcenverteilers verweist, die die Ressource darstellt. Der Verteiler-Manager muss diese Struktur im Speicher des Ressourcenverteilers nicht verstehen. Der Verteiler-Manager verwendet _* RESID,** um auf eine bestimmte Ressource in einem Ressourcenverteiler zu verweisen.                                                                                                                                 |
| **SRESID**     | Eine Unicode-Zeichenfolgenversion von **RESID,** die in den Methoden [**IHolder::TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) und [**IHolder::UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) verwendet wird. Zeichenfolgen sind manchmal nützlich, wenn nur eine kleine Menge von Informationen zu einer Ressource aufgezeichnet werden muss und die gesamte Beschreibung der Ressource in der **SRESID** enthalten sein kann. Insbesondere kann die Verwendung der **SRESID** manchmal die Notwendigkeit einer Zuordnung im Ressourcenverteiler beseitigen, wenn die Ressource eine Beziehung zwischen zwei (oder mehr) Dingen darstellt. |
| **TRANSID**    | Identifiziert eine Transaktion. Dieser Typ kann in die **ITransaction-Schnittstelle** umgewandelt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | Gibt an, wie lange eine Ressource inaktiv sein kann, bevor sie zerstört wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Ressourcenverteilerkonzepte](com--resource-dispenser-concepts.md)
</dt> <dt>

[COM+-Ressourcenverteilerschnittstellen](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



