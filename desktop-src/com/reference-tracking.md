---
title: Verweis Nachverfolgung
description: Verweis Nachverfolgung
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474309"
---
# <a name="reference-tracking"></a>Verweis Nachverfolgung

Die Verweis Nachverfolgung kann die unbeabsichtigte oder schädliche frühe Freigabe von Objekten verhindern.

Wenn Sie die Verweis Verfolgung aktivieren, fordern Sie an, dass verteilte [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -und [**releaseaufrufe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) von com authentifiziert werden. Wenn die Verweis Verfolgung aktiviert ist, verfolgt com den Verweis Zähler pro Benutzer, damit ein Benutzer die **Freigabe** nur für Objekte aufrufen kann, die der Benutzer zuvor als " **adressf** " bezeichnet hat. Obwohl bei der Verweis Nachverfolgung die Leistung beeinträchtigt werden kann, wird sichergestellt, dass unabhängig davon, wie oft ein bestimmter Benutzer die **Freigabe** aufruft, die Objekte und stubwerte weiterhin vorhanden sind, wenn ein anderer Benutzer einen Verweis darauf hat.

Der Client kann die Verweis Nachverfolgung für einen Prozess festlegen, indem er \_ \_ in einem [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Rückruf das eoac Secure Refs-funktionsflag übergibt. Mithilfe Dcomcnfg.exe können Sie auch die Verweis Nachverfolgung für alle Anwendungen auf einem Computer aktivieren oder deaktivieren.

Wenn die Verweis Nachverfolgung aktiviert ist, verwendet [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) immer Standard Sicherheitseinstellungen. In diesem Fall tritt bei Aufrufen von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) bei **IUnknown** ein Fehler auf.

 

 