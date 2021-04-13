---
description: Automatische Ressourcenrückgewinnung
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Automatische Ressourcenrückgewinnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342289"
---
# <a name="automatic-resource-reclamation"></a>Automatische Ressourcenrückgewinnung

Com+ benachrichtigt den Dispenser Manager, wenn die Lebensdauer eines Objekts endet. Der Dispenser-Manager benachrichtigt dann jeden Inhaber des registrierten Ressourcen Verteilers, ob er über Ressourcen verfügt, die noch von diesem Objekt aufbewahrt werden. Wenn dies der Fall ist, werden diese Ressourcen freigegeben. Dadurch wird die Möglichkeit von Ressourcenverlusten durch Komponenten verhindert, die Ressourcen über einen Ressourcen Verteiler erhalten.

Bei der automatischen Freigabe handelt es sich um eine Option, die standardmäßig deaktiviert ist. Ein Ressourcen Verteiler kann diese Option aktivieren und garantiert, dass ein Verweis auf eine Ressource, die an ein Objekt ausgegeben wird, niemals von den Objektmethoden zurückgegeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



