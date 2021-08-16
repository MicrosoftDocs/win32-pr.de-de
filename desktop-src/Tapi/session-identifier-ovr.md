---
description: TAPI weist Sitzungsbezeichner zu, die für jede Sitzung und Anwendung eindeutig sind.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Sitzungsbezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527706159328b3919e47c39bc5fb160615ed2c202d33c1ce39c711b6921235a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760782"
---
# <a name="session-identifier"></a>Sitzungsbezeichner

TAPI weist Sitzungsbezeichner zu, die für jede Sitzung und Anwendung eindeutig sind. Eine Anwendung verwendet einen Sitzungsbezeichner, um mit TAPI über eine bestimmte Sitzung zu kommunizieren. Eine Anwendung erhält einen Bezeichner in der Regel entweder durch Erstellen einer neuen Kommunikationssitzung oder wenn TAPI eine Sitzung anbietet.

Ein Sitzungsbezeichner kann nicht verwendet werden, um Informationen an eine andere Anwendung zu übergeben. Verwenden Sie zu diesem Zweck die [Aufruf-ID](call-id-ovr.md), die von einem Dienstanbieter zugewiesen werden kann.

Informationen zu Vorgängen, die Sitzungen erstellen und einen Sitzungsbezeichner zurückgeben, finden Sie unter [Initiieren](initiate-a-session-ovr.md) einer Sitzung. Informationen zu Vorgängen, die Sitzungsbezeichner von TAPI abrufen, finden Sie unter [Reagieren auf an anderer Stelle initiierte](respond-to-session-initiated-elsewhere-ovr.md) Sitzungen. Informationen zum Freigeben von Sitzungsressourcen finden Sie unter [Beenden einer](terminate-a-session-ovr.md) Sitzung.

Alle Dienstanbieter müssen eine Form der Sitzungsidentifikation unterstützen.

**TAPI 2.x:** Der primäre Bezeichner einer Kommunikationssitzung ist das Aufrufhandle.

**TAPI 3.x:** Eine Sitzung wird durch ein [Aufrufobjekt](call-object.md) dargestellt, und der primäre Bezeichner ist ein Zeiger auf die [**ITCallInfo-Schnittstelle.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

 

 



