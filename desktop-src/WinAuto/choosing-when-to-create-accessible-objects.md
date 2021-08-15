---
title: Auswählen, wann barrierefreie Objekte erstellt werden
description: Serverentwickler können alle zugänglichen Objekte innerhalb eines Containers erstellen, wenn der Container erstellt wird, oder sie können die barrierefreien Objekte dynamisch erstellen.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a53ee02cb7de574242b3ba9986cdf0ce6068e8495e1ebaf638eed08e9c04b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325979"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Auswählen, wann barrierefreie Objekte erstellt werden

Serverentwickler können alle zugänglichen Objekte innerhalb eines Containers erstellen, wenn der Container erstellt wird, oder sie können die barrierefreien Objekte dynamisch erstellen.

Stellen Sie sich beispielsweise ein Dialogfeld mit mehreren benutzerdefinierten Steuerelementen vor. Ein Server erstellt barrierefreie Objekte für alle benutzerdefinierten Steuerelemente, wenn das Dialogfeld angezeigt wird. Wenn eines der Steuerelemente jedoch ein benutzerdefiniertes Kombinationsfeld ist, wartet der Server, bis ein Benutzer es auswählt, um barrierefreie Objekte für die Elemente zu erstellen, die das Kombinationsfeld enthält.

Wenn das übergeordnete Element barrierefreie Objekte dynamisch erstellt, verwenden Anwendungen weniger Arbeitsspeicher, als wenn alle möglichen barrierefreien Objekte im Voraus erstellt wurden.

 

 




