---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem ein Objekt mit erhöhten Component Object Model wird.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: COM-Objektmodell des Administrators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b331d71f83428ad821bc1c2f9de24984025aaf7f95874c2203ee9fb1f9158a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784787"
---
# <a name="administrator-com-object-model"></a>COM-Objektmodell des Administrators

Im COM-Objektmodell des Administrators führt eine Anwendung, die als Standardbenutzer ausgeführt wird, Vorgänge aus, die Administratorrechte erfordern, indem sie ein Objekt mit [Component Object Model](/windows/desktop/com/component-object-model--com--portal) erstellt. Informationen zum Erstellen eines COM-Objekts mit erhöhten Rechten finden Sie unter [Der COM-Moniker für erhöhte Rechte.](../com/the-com-elevation-moniker.md)

Ein Nachteil bei der Verwendung des COM-Objektmodells des Administrators ist, dass der Benutzer jedes Mal aufgefordert wird, wenn ein privilegierter Vorgang ausgeführt wird.

Jede Benutzeroberfläche, die das COM-Objekt steuern kann, muss vom COM-Objekt selbst dargestellt werden. Andernfalls kann ein nicht privilegierter Prozess dazu führen, dass das COM-Objekt mit erhöhten Rechten privilegierte Vorgänge ausführen kann, ohne dass der Benutzer dazu aufgefordert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Anwendungen, die Administratorrechte erfordern](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Administratorbrokermodell](administrator-broker-model.md)
</dt> <dt>

[Aufgabenmodell mit erhöhten Rechten](elevated-task-model.md)
</dt> <dt>

[Betriebssystemdienstmodell](operating-system-service-model.md)
</dt> </dl>

 

 
