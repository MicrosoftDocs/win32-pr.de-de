---
description: Zusätzlich zu einzelnen Warteschlangendateivorgängen können Sie auch alle in einem INF-Abschnitt aufgeführten Dateien in die Warteschlange stellen.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Einteilen eines INF-Abschnitts in die Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c419f23fe48057eec382c83b4da5e219114c186a9b7bc07c04fc5d7088b17e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964957"
---
# <a name="queuing-an-inf-section"></a>Einteilen eines INF-Abschnitts in die Warteschlange

Zusätzlich zu einzelnen Warteschlangendateivorgängen können Sie auch alle in einem INF-Abschnitt aufgeführten Dateien in die Warteschlange stellen.

Sie können alle Dateien,  die im Abschnitt Dateien kopieren einer INF-Datei aufgeführt sind, in die Warteschlange stellen, indem Sie [**SetupQueueCopySection aufrufen.**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) Damit diese Funktion erfolgreich  ist, muss der Abschnitt Dateien kopieren das richtige Format haben, und die INF-Datei oder eine der angefügten Dateien muss die Abschnitte **SourceDisksFiles** und **SourceDisksNames** enthalten.

Ebenso können Sie [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)  aufrufen, wenn Sie alle Dateien löschen möchten, die im Abschnitt Dateien löschen einer INF-Datei angegeben sind. Verwenden Sie SetupQueueRenameSection, um alle Dateien im Abschnitt **"Dateien** umbenennen" einer [**INF-Datei umzubenennen.**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)

 

 



