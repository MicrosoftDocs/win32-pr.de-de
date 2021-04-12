---
description: Wenn Sie einen Patch und eine oder mehrere Anpassungs Transformationen in eine Anwendung installieren, wird der Patch in der Regel zuerst installiert, gefolgt von den Anpassungs Transformationen.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Patchen von angepassten Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345549"
---
# <a name="patching-customized-applications"></a>Patchen von angepassten Anwendungen

Wenn Sie einen Patch und eine oder mehrere Anpassungs Transformationen in eine Anwendung installieren, wird der Patch in der Regel zuerst installiert, gefolgt von den Anpassungs Transformationen. Der Patch wird von der nachfolgenden Installation der Anpassung nicht untergliedert. Allerdings kann die Anpassung bei der erstmaligen Installation der Transformationen und dann dem Patch unterbrechen.

Beispielsweise kann eine Unterbrechung der Anpassung auftreten, wenn ein Patch verwendet wird, um ein Produkt von Version 1 auf Version 2 zu aktualisieren, und eine Anpassungs Transformation, die für Version 1 funktioniert, nicht für Version 2 funktioniert. In diesem Fall kann der Patch für die Versions Aktualisierung nicht auf ein angepasstes Produkt angewendet werden, ohne zunächst deinstallieren und dann das ursprüngliche Produkt neu installieren zu müssen.

 

 



