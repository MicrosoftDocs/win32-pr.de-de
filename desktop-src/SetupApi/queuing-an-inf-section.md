---
description: Neben Datei Vorgängen in der Warteschlange können Sie auch alle Dateien in die Warteschlange stellen, die in einem INF-Abschnitt aufgeführt sind.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Warteschlangen für einen INF-Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529777"
---
# <a name="queuing-an-inf-section"></a>Warteschlangen für einen INF-Abschnitt

Neben Datei Vorgängen in der Warteschlange können Sie auch alle Dateien in die Warteschlange stellen, die in einem INF-Abschnitt aufgeführt sind.

Sie können alle Dateien, die im Abschnitt **Kopieren von Dateien** einer INF-Datei aufgelistet sind, durch Aufrufen von [**setupqueuecopysection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)in die Warteschlange stellen. Damit diese Funktion erfolgreich ist, muss der Abschnitt zum **Kopieren von Dateien** das richtige Format aufweisen, und die INF-Datei oder eine der angefügten Dateien muss die Abschnitte **SourceDisksFiles** und **SourceDisksNames** enthalten.

Wenn Sie alle im Abschnitt **Löschen von Dateien** einer INF-Datei angegebenen Dateien löschen möchten, können Sie [**setupqueuedeletesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)auch aufrufen. Wenn Sie alle Dateien im Abschnitt **Umbenennen von Dateien** einer INF-Datei umbenennen möchten, verwenden Sie [**setupqueuerenamesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

 

 



