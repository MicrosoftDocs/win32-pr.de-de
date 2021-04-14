---
description: TAPI weist Sitzungs Bezeichner zu, die für jede Sitzung und Anwendung eindeutig sind.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Sitzungsbezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393802"
---
# <a name="session-identifier"></a>Sitzungsbezeichner

TAPI weist Sitzungs Bezeichner zu, die für jede Sitzung und Anwendung eindeutig sind. Eine Anwendung verwendet eine Sitzungs-ID, um mit TAPI über eine bestimmte Sitzung zu kommunizieren. Eine Anwendung erhält in der Regel einen Bezeichner, indem eine neue Kommunikationssitzung erstellt wird oder wenn TAPI eine Sitzung anbietet.

Ein Sitzungs Bezeichner kann nicht verwendet werden, um Informationen an eine andere Anwendung zu übergeben. Verwenden Sie zu diesem Zweck die [Telefonnummer](call-id-ovr.md), die von einem Dienstanbieter zugewiesen werden kann.

Weitere Informationen zu Vorgängen, die Sitzungen erstellen und eine Sitzungs-ID zurückgeben, finden Sie unter [Initiieren einer Sitzung](initiate-a-session-ovr.md) . Weitere Informationen zu Vorgängen, die Sitzungs Bezeichner von TAPI abrufen, finden [Sie unter reagieren auf eine Sitzung](respond-to-session-initiated-elsewhere-ovr.md) . Weitere Informationen zum Freigeben von Sitzungs Ressourcen finden Sie unter [Beenden einer Sitzung](terminate-a-session-ovr.md) .

Alle Dienstanbieter müssen eine bestimmte Form der Sitzungs Identifikation unterstützen.

**TAPI 2. x:** Der primäre Bezeichner einer Kommunikationssitzung ist das-Anweisungs Handle.

**TAPI 3. x:** Eine Sitzung wird durch ein [Aufruf Objekt](call-object.md) dargestellt, und der primäre Bezeichner ist ein Zeiger auf die [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) -Schnittstelle.

 

 



