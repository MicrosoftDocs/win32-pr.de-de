---
title: Erkennen des Betriebsmodus einer Domäne
description: In Windows 2000 kann eine Domäne in zwei Betriebsmodi gemischt und System eigen ausgeführt werden.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Erkennen des Betriebsmodus einer Domänen Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858156"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a>Erkennen des Betriebsmodus einer Domäne

In Windows 2000 kann eine Domäne in zwei Betriebsmodi ausgeführt werden: gemischt und System eigen. Der gemischte Modus sollte verwendet werden, um Domänen Controller unter Windows NT 4,0 in einer Windows 2000-Domäne einzubinden. Der gemischte Modus unterstützt keine universellen Gruppen oder schsted Groups. Wenn auf allen Domänen Controllern in der Domäne Windows 2000 ausgeführt wird, können Sie den einheitlichen Modus verwenden.

Wenn Sie den Betriebsmodus einer Windows 2000-Domäne Programm gesteuert erkennen möchten, lesen Sie die [**nTMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) -Eigenschaft des [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekts für diese Domäne. Der Wert 0 (null) bedeutet, dass sich die Domäne im einheitlichen Modus befindet. Der Wert eins (1) gibt an, dass sich die Domäne im gemischten Modus befindet. Sie können auch die [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) -Funktion verwenden, um den Betriebsmodus sowie andere Daten über die Domäne und ihren Status zu erhalten.

Verwenden Sie zum Binden an das [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekt der Domäne des Benutzerkontos, unter dem die Anwendung ausgeführt wird, die Server lose Bindung und RootDSE, um den Distinguished Name für die Domäne zu erhalten, und verwenden Sie dann den Distinguished Name, um eine Bindung an das **domainDns** -Objekt herzustellen, das diese Domäne darstellt. Weitere Informationen zu Server losen Bindungen und RootDSE finden Sie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md).

Weitere Informationen und ein Codebeispiel, das zeigt, wie der Betriebsmodus einer Domäne Programm gesteuert erkannt wird, finden Sie unter [Beispielcode zum Bestimmen des Betriebsmodus](example-code-for-determining-the-operation-mode.md).

 

 