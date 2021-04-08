---
description: Die Sitzungs Umleitung ermöglicht es einer Anwendung, eine angebotene Sitzung an eine andere Adresse zu leiten, ohne den Anruf zu beantworten.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Umleiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760807"
---
# <a name="redirect"></a>Umleiten

Die Sitzungs Umleitung ermöglicht es einer Anwendung, eine angebotene Sitzung an eine andere Adresse zu leiten, ohne den Anruf zu beantworten. Die Anwendung kann eine Umleitung für einen Rückruf durchführen. Beispielsweise kann eine Anwendung es einem Benutzer ermöglichen, verschiedene Umleitungen basierend auf den Aufrufer-ID-Informationen anzugeben. Nachdem ein-Rückruf erfolgreich umgeleitet wurde, wechselt der Status in der Regel in den Leerlauf, und die zugehörigen Ressourcen müssen freigegeben werden.

Die Umleitung unterscheidet sich insofern von [vorn](forward-ovr.md) , dass nach dem Einrichten der Weiterleitung der Vorgang von TAPI, dem Dienstanbieter oder dem Switch durchgeführt wird, ohne dass die Anwendung weiter einbezogen wird. Die Umleitung unterscheidet sich von der [Übertragung](transfer-ovr.md) in, da die Umleitung den Anruf nicht zuerst beantworten muss.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Siehe [**lineredirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).

 

 
