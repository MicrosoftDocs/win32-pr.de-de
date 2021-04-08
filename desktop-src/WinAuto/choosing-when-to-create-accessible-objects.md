---
title: Auswählen, wann barrierefreie Objekte erstellt werden sollen
description: Server Entwickler können alle zugänglichen Objekte in einem Container erstellen, wenn der Container erstellt wird, oder Sie können die barrierefreien Objekte dynamisch erstellen.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037254"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Auswählen, wann barrierefreie Objekte erstellt werden sollen

Server Entwickler können alle zugänglichen Objekte in einem Container erstellen, wenn der Container erstellt wird, oder Sie können die barrierefreien Objekte dynamisch erstellen.

Stellen Sie sich z. b. ein Dialogfeld mit mehreren benutzerdefinierten Steuerelementen vor. Ein Server erstellt barrierefreie Objekte für alle benutzerdefinierten Steuerelemente, wenn das Dialogfeld angezeigt wird. Wenn eines der Steuerelemente jedoch ein benutzerdefiniertes Kombinations Feld ist, wartet der Server, bis ein Benutzer es auswählt, um barrierefreie Objekte für die im Kombinations Feld enthaltenen Elemente zu erstellen.

Wenn das übergeordnete Objekt barrierefreie Objekte dynamisch erstellt, wird weniger Arbeitsspeicher verwendet, als wenn alle möglichen zugänglichen Objekte im Voraus erstellt wurden.

 

 




