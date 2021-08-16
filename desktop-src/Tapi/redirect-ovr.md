---
description: Die Sitzungsumleitung ermöglicht es einer Anwendung, eine angebotene Sitzung an eine andere Adresse umzuleiten, ohne den Anruf zu beantworten.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Umleiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea44aaa10bc174784822032359d68d24ba01b6f7f1dcdf0fb211554107b8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761204"
---
# <a name="redirect"></a>Umleiten

Die Sitzungsumleitung ermöglicht es einer Anwendung, eine angebotene Sitzung an eine andere Adresse umzuleiten, ohne den Anruf zu beantworten. Die Anwendung kann die Umleitung auf Aufrufbasis durchführen. Beispielsweise kann eine Anwendung einem Benutzer erlauben, basierend auf den Informationen zur Aufrufer-ID unterschiedliche Umleitungen anzugeben. Nachdem ein Aufruf erfolgreich umgeleitet wurde, geht der Zustand in der Regel in den Leerlauf über, und zugeordnete Ressourcen müssen freigegeben werden.

Die Umleitung unterscheidet sich von [der Weiterleitung](forward-ovr.md) darin, dass der Vorgang nach dem Einrichten der Weiterleitung von TAPI, dem Dienstanbieter oder dem Switch ohne weitere Beteiligung der Anwendung ausgeführt wird. Die Umleitung unterscheidet sich von der [Übertragung,](transfer-ovr.md) da die Umleitung keine erste Antwort auf den Anruf erfordert.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2.x:** Weitere Informationen finden Sie unter [**lineRedirect.**](/windows/win32/api/tapi/nf-tapi-lineredirect)

 

 
