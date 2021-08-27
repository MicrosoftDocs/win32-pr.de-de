---
description: Wenn Sie einen Patch und eine oder mehrere Anpassungstransformationen für eine Anwendung installieren, wird der Patch in der Regel zuerst installiert, gefolgt von den Anpassungstransformationen.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Patchen von benutzerdefinierten Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469fd2e5f80f19e84fcdc22ed7753374bc9a456cd68946f5f4bd6764e7aa0d11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074820"
---
# <a name="patching-customized-applications"></a>Patchen von benutzerdefinierten Anwendungen

Wenn Sie einen Patch und eine oder mehrere Anpassungstransformationen für eine Anwendung installieren, wird der Patch in der Regel zuerst installiert, gefolgt von den Anpassungstransformationen. Der Patch wird von der nachfolgenden Installation der Anpassung nicht unterbrochen. Wenn Sie jedoch zuerst die Transformationen und dann den Patch installieren, kann die Anpassung möglicherweise nicht mehr vorgenommen werden.

Eine Unterbrechung der Anpassung kann beispielsweise auftreten, wenn ein Patch verwendet wird, um ein Produkt von Version 1 auf Version 2 zu aktualisieren, und eine Anpassungstransformation, die für Version 1 funktioniert, für Version 2 nicht funktioniert. In diesem Fall kann der Patch für Versionsupdates nicht auf ein benutzerdefiniertes Produkt angewendet werden, ohne zuerst das ursprüngliche Produkt zu deinstallieren und dann neu zu installieren.

 

 



