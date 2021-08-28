---
description: Sicherungsfähige Objekte verwenden ein Zugriffsmaskenformat, in dem die vier hochgeordneten Bits generische Zugriffsrechte angeben.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Generische Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee90a6866afc294cfef1c8fdad96e239f76ce8f9c251aeabc2d2a907e3e0bbe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672090"
---
# <a name="generic-access-rights"></a>Generische Zugriffsrechte

Sicherungsfähige Objekte verwenden ein [Zugriffsmaskenformat,](access-mask-format.md) in dem die vier hochgeordneten Bits generische Zugriffsrechte angeben. Jeder Typ von sicherungsfähigen Objekten ordnet diese Bits einer Reihe von Standard- und objektspezifischen Zugriffsrechten zu. Beispielsweise ordnet ein Windows-Dateiobjekt das GENERISCHE \_ \_ READ-Bit den Standardzugriffsrechten READ CONTROL und SYNCHRONIZE sowie den \_ \_ \_ \_ \_ objektspezifischen Zugriffsrechten FILE READ DATA, FILE READ EA und FILE READ \_ ATTRIBUTES zu. Andere Objekttypen ordnen das GENERIC \_ READ-Bit allen Zugriffsrechten zu, die für diesen Objekttyp geeignet sind.

Sie können generische Zugriffsrechte verwenden, um den Zugriffstyp anzugeben, den Sie benötigen, wenn Sie ein Handle für ein Objekt öffnen. Dies ist in der Regel einfacher als die Angabe aller entsprechenden Standard- und spezifischen Rechte.

Die folgende Tabelle zeigt die Konstanten, die für die generischen Zugriffsrechte definiert sind.



| Konstante         | Generische Bedeutung            |
|------------------|----------------------------|
| GENERIC \_ ALL     | Alle möglichen Zugriffsrechte |
| GENERIC \_ EXECUTE | Ausführen des Zugriffs             |
| GENERISCHER \_ LESE-    | Lesezugriff                |
| GENERISCHER \_ SCHREIBVORGANG   | Schreibzugriff               |



 

Anwendungen, die private sicherungsfähige Objekte definieren, können auch die generischen Zugriffsrechte verwenden.

 

 



