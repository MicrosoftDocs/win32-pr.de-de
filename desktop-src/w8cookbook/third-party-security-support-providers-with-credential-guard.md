---
title: Credential Guard und Drittanbieter-apps
description: Credential Guard erlaubt Drittanbieter-SSPs nicht, Kennworthashes von LSA abzufragen.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473140"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Security Support Provider von Drittanbietern mit Credential Guard

Credential Guard erlaubt Drittanbieter-SSPs nicht, Kennworthashes von LSA abzufragen. SSPs und Zugriffspunkte werden aber weiterhin über das Kennwort informiert, wenn sich ein Benutzer anmeldet bzw. sein Kennwort ändert. Die Verwendung von undokumentierten APIs in benutzerdefinierten SSPs und Zugriffspunkten wird nicht unterstützt.

Da die Tiefe und der Umfang der Schutzmaßnahmen, die Credential Guard bereitstellt, erweitert werden, können nachfolgende Versionen von Windows 10 mit Credential Guard Szenarien beeinträchtigen, die in der Vergangenheit funktioniert haben. Beispielsweise kann Anmelde Informationen Guard die Verwendung eines bestimmten Typs von Anmelde Informationen oder einer bestimmten Komponente blockieren, um zu verhindern, dass Schadsoftware von Sicherheitsrisiken ausgenutzt wird. Daher sollten Sie Szenarien, die für Vorgänge in einer Organisation wichtig sind, vor dem Upgrade eines Geräts testen, auf dem Credential Guard ausgeführt wird.

Die vollständige Beschreibung und empfohlene entschärfungen finden Sie in [diesem Artikel](/windows/security/identity-protection/credential-guard/credential-guard) .

 

 