---
title: Steuern der Objekt Sichtbarkeit
description: Active Directory Domain Services bieten die Möglichkeit, Objekte von Benutzern auszublenden, denen bestimmte Rechte verweigert wurden.
ms.assetid: 3a65ec79-7de0-4d14-b980-1ca6a972ac70
ms.tgt_platform: multiple
keywords:
- Steuern der Sichtbarkeit von Objekten Active Directory
- Active Directory Active Directory mit, Steuern der Objekt Sichtbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b1ab364f0711174d5ac1dd1e4fbe98303c50b3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038789"
---
# <a name="controlling-object-visibility"></a>Steuern der Objekt Sichtbarkeit

Active Directory Domain Services bieten die Möglichkeit, Objekte von Benutzern auszublenden, denen bestimmte Rechte verweigert wurden. Wenn ein Objekt ausgeblendet ist, kann eine Anwendung, die mit den Anmelde Informationen eines Benutzers ausgeführt wird, nicht in der Lage sein, das Objekt aufzuzählen oder zu binden.

Wenn einem Benutzer die Zugriffs Steuerungs Berechtigung [**ADS \_ right \_ actrl \_ DS \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum) für einen Container gewährt wird, kann der Benutzer alle untergeordneten Objekte des Containers anzeigen. Ebenso gilt: Wenn einem Benutzer die Zugriffs Steuerungs Berechtigung " **ADS \_ right \_ actrl \_ DS \_** " für einen Container verweigert wird, kann der Benutzer die untergeordneten Objekte des Containers nicht anzeigen. Dadurch kann der Inhalt ganzer Container ausgeblendet werden.

Der Active Directory Server kann auch in einem speziellen Listen Objekt Modus abgelegt werden, indem das dritte Zeichen der [**dSHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) -Eigenschaft auf "1" festgelegt wird. Der Listen Objekt Modus kann deaktiviert werden, indem das dritte Zeichen der **dSHeuristics** -Eigenschaft auf "0" festgelegt wird. Wenn sich der Active Directory Server im Listen Objekt Modus befindet, ist ein Objekt weiterhin sichtbar, wenn dem Benutzer für das übergeordnete Objekt die [**\_ Liste ADS right \_ actrl \_ DS \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum) gewährt wurde. Wenn dem Benutzer jedoch die **\_ Liste ADS right \_ actrl \_ DS \_** direkt auf dem übergeordneten Element verweigert wurde, können bestimmte untergeordnete Objekte weiterhin sichtbar gemacht werden, wenn dem Benutzer das **ADS \_ right \_ DS List- \_ \_ Objekt** für das übergeordnete und das untergeordnete Objekt Recht gewährt wird. Der Listen Objekt Modus ermöglicht es dem Systemadministrator, den Zugriff auf einzelne Objekte für Benutzer oder Gruppen zu gewähren oder zu verweigern. Der Listen Objekt Modus sollte sparsam verwendet werden, da er eine wesentlich höhere Anzahl von Zugriffs Prüf aufrufen erfordert, die vom Verzeichnisdienst durchgeführt werden müssen, um zu bestimmen, ob ein Objekt für einen Benutzer sichtbar ist. Dies kann sich negativ auf die Leistung beim Durchsuchen oder Lesen von Objekten aus Active Directory Domain Services auswirken.

 

 