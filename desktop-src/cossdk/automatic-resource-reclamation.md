---
description: Automatische Ressourcenrückgewinnung
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Automatische Ressourcenrückgewinnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec280c0b0ae222cf0c63e136b7643bbd05c1fffa5589ccc4b736dd247a43b1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730670"
---
# <a name="automatic-resource-reclamation"></a>Automatische Ressourcenrückgewinnung

COM+ benachrichtigt den Vorgesetzten jedes Mal, wenn die Lebensdauer eines Objekts endet. Der Versender-Manager benachrichtigt dann den Besitzer jedes registrierten Ressourcensenders, um festzustellen, ob er noch über Ressourcen verfügt, die von diesem Objekt gehalten werden. Wenn dies der Fehler ist, werden diese Ressourcen frei, sodass es nicht zu Ressourcenverlusten durch Komponenten kommt, die Ressourcen über einen Ressourcensender erhalten.

Das Feature für die automatische Rückgewinnung ist eine Option, die standardmäßig deaktiviert ist. Ein Ressourcensender kann diese Option aktivieren und so garantieren, dass ein Verweis auf eine Ressource, die an ein Objekt vererbt wird, nie von den Objektmethoden zurückgegeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KONZEPTE DES COM+-Ressourcensenders](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



