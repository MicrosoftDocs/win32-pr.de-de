---
description: Ein Vertrauens nehmer ist das Benutzerkonto, das Gruppenkonto oder die Anmelde Sitzung, auf die ein Zugriffs Steuerungs Eintrag angewendet wird. Jeder ACE in einer Zugriffs Steuerungs Liste (Access Control List, ACL) verfügt über eine Sicherheits-ID (SID), die einen Vertrauens nehmer identifiziert.
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: Vertrauens nehmer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90084a0b6bfc7f63db12b7f47eba335adc87239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218669"
---
# <a name="trustees"></a>Vertrauens nehmer

Ein Vertrauens nehmer ist das Benutzerkonto, das Gruppenkonto oder die [*Anmelde Sitzung*](/windows/desktop/SecGloss/l-gly) , auf die ein [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) angewendet wird. Jeder ACE in einer [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL) verfügt über eine [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID), die einen Vertrauens nehmer identifiziert.

Benutzerkonten enthalten Konten, die von Menschen oder Programmen wie Windows-Diensten verwendet werden, um sich am lokalen Computer anzumelden.

Gruppenkonten können nicht verwendet werden, um sich an einem Computer anzumelden, Sie sind jedoch in ACEs nützlich, um einen Satz von Zugriffsrechten für ein oder mehrere Benutzerkonten zuzulassen oder zu verweigern.

Eine [*Anmelde-SID*](/windows/desktop/SecGloss/l-gly) , mit der die aktuelle Anmelde Sitzung identifiziert wird, ist nützlich, um Zugriffsrechte nur zuzulassen oder zu verweigern, bis der Benutzer sich abmeldet.

Die Zugriffs Steuerungsfunktionen verwenden die [**Treuhänder**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) Struktur zum Identifizieren eines Vertrauens nehmers. Die Vertrauens nehmer-Struktur ermöglicht es Ihnen, eine namens Zeichenfolge oder eine **SID zum Identifizieren** eines Vertrauens nehmers zu verwenden. Wenn Sie einen Namen verwenden, führen die Funktionen, die einen ACE aus der **Treuhänder** Struktur erstellen, die Aufgabe aus, die SID-Puffer zuzuordnen und die SID zu suchen, die dem Kontonamen entspricht. Es gibt zwei Hilfsfunktionen, [**buildtreuhänewithsid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) und [**buildtreuewithname**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea), die eine Vertrauens nehmer **-Struktur mit** einer angegebenen SID oder einem Namen initialisieren. Mit [**buildtreuewithobjectandsid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) und [**buildtreuhänder-withobjectandname**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) können **Sie eine Vertrauens** nehmer-Struktur mit Objekt spezifischen ACE-Informationen initialisieren. Die drei weiteren Hilfsfunktionen " [**gettrusteeform**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma)", " [**gettrusteename**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)" und " [**gettrusteetype**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea)" rufen die Werte der verschiedenen Mitglieder einer Vertrauens nehmer **-Struktur ab** .

Der **ptstrinname** -Member der [**Treuhänder**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) Struktur kann ein Zeiger auf [**Objekte \_ und \_ Namen**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) oder [**Objekte und eine \_ \_ sid-**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) Struktur sein. Diese Strukturen geben Informationen zu einem [Objekt spezifischen ACE](object-specific-aces.md) zusätzlich zu einem Vertrauens nehmer Namen oder einer SID an. Dadurch können Funktionen wie " [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) " und " [**getexplicitentriesfromacl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) " Objektspezifische ACE-Informationen im **Treuhänder** -Member der [**expliziten \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Struktur speichern.

 

 
