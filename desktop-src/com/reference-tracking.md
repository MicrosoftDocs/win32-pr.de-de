---
title: Referenznachverfolgung
description: Referenznachverfolgung
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1321c922cc0a7493e3e4792f7c0f925618330c2e42665296fb06792635a4ea70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309763"
---
# <a name="reference-tracking"></a>Referenznachverfolgung

Die Verweisnachverfolgung kann die unbeabsichtigte oder böswillige frühe Freigabe von Objekten verhindern.

Wenn Sie die Verweisnachverfolgung aktivieren, fordern Sie, dass verteilte [**AddRef-**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Releaseaufrufe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) von COM authentifiziert werden. Wenn die Verweisnachverfolgung aktiviert ist, verfolgt COM die Anzahl der Benutzerverweise nach, sodass ein Benutzer **Release** nur für Objekte aufrufen kann, die der Benutzer zuvor **Als AddRef** bezeichnet hat. Obwohl die Verweisnachverfolgung die Leistung beeinträchtigen kann, stellt sie sicher, dass unabhängig davon, wie oft ein angegebener Benutzer **Release** aufruft, die Objekte und Stubs weiterhin vorhanden sind, wenn eine andere Person einen Verweis darauf hat.

Der Client kann die Verweisnachverfolgung für einen Prozess festlegen, indem er das EOAC \_ SECURE \_ REFS-Funktionsflag in einem Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)übergibt. Sie können die Verweisnachverfolgung auch für alle Anwendungen auf einem Computer aktivieren oder deaktivieren, indem Sie Dcomcnfg.exe verwenden.

Wenn die Verweisnachverfolgung aktiviert ist, verwendet [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) immer Standardsicherheitseinstellungen. In diesem Fall schlagen Aufrufe von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) auf **IUnknown** fehl.

 

 