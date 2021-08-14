---
title: Credential Guard und Drittanbieter-Apps
description: Credential Guard erlaubt Drittanbieter-SSPs nicht, Kennworthashes von LSA abzufragen.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5c773379e3b7fa52e2095d8db676dddc081e51806fd8f615d2b3a4b744fea95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706750"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Sicherheitssupportanbieter von Drittanbietern mit Credential Guard

Credential Guard erlaubt Drittanbieter-SSPs nicht, Kennworthashes von LSA abzufragen. SSPs und Zugriffspunkte werden aber weiterhin über das Kennwort informiert, wenn sich ein Benutzer anmeldet bzw. sein Kennwort ändert. Die Verwendung von undokumentierten APIs in benutzerdefinierten SSPs und Zugriffspunkten wird nicht unterstützt.

Da die Tiefe und der Umfang der Schutzmaßnahmen, die Credential Guard bereitstellt, erweitert werden, können nachfolgende Versionen von Windows 10 mit Credential Guard Szenarien beeinträchtigen, die in der Vergangenheit funktioniert haben. Credential Guard kann beispielsweise die Verwendung eines bestimmten Anmeldeinformationstyps oder einer bestimmten Komponente blockieren, um zu verhindern, dass Schadsoftware Sicherheitsrisiken nutzt. Daher sollten Sie Szenarien, die für Vorgänge in einer Organisation wichtig sind, vor dem Upgrade eines Geräts testen, auf dem Credential Guard ausgeführt wird.

Eine vollständige Beschreibung und empfohlene Gegenmaßnahmen finden Sie in [diesem Artikel.](/windows/security/identity-protection/credential-guard/credential-guard)

 

 