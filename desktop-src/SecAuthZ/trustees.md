---
description: Ein Vertrauensinhaber ist das Benutzerkonto, das Gruppenkonto oder die Anmeldesitzung, für die ein Zugriffssteuerungseintrag (ACE) gilt. Jeder ACE in einer Zugriffssteuerungsliste (Access Control List, ACL) verfügt über eine Sicherheits-ID (SID), die einen Vertrauenshänder identifiziert.
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: Treuhänder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e79bc49a4ffc93c87b040327a2c7626bc7d816e060cf4bfcd42a6bcab0d024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906960"
---
# <a name="trustees"></a>Treuhänder

Ein Vertrauensinhaber ist das Benutzerkonto, das Gruppenkonto [](/windows/desktop/SecGloss/a-gly) oder die [*Anmeldesitzung,*](/windows/desktop/SecGloss/l-gly) für die ein Zugriffssteuerungseintrag (ACE) gilt. Jeder ACE in einer [*Zugriffssteuerungsliste*](/windows/desktop/SecGloss/a-gly) [](/windows/desktop/SecGloss/s-gly) (Access Control List, ACL) verfügt über eine Sicherheits-ID (SID), die einen Vertrauenshänder identifiziert.

Benutzerkonten umfassen Konten, die von menschlichen Benutzern oder Programmen wie Windows Services zum Anmelden am lokalen Computer verwendet werden.

Gruppenkonten können nicht verwendet werden, um sich bei einem Computer anmelden, aber sie sind in ACEs nützlich, um einen Satz von Zugriffsrechten für ein oder mehrere Benutzerkonten zu erlauben oder zu verweigern.

Eine [*Anmelde-SID,*](/windows/desktop/SecGloss/l-gly) die die aktuelle Anmeldesitzung identifiziert, ist nützlich, um Zugriffsrechte nur zu erlauben oder zu verweigern, bis sich der Benutzer abmeldet.

Die Zugriffssteuerungsfunktionen verwenden die [**VERTRAUENS-Struktur,**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) um einen Vertrauenshänder zu identifizieren. Mit **der VERTRAUENS-Struktur** können Sie eine Namenszeichenfolge oder sid verwenden, um einen Vertrauenshänder zu identifizieren. Wenn Sie einen Namen verwenden, führen die Funktionen, die einen ACE aus der **VERTRAUENS-Struktur** erstellen, die Aufgabe aus, die SID-Puffer zu zuordnen und die SID zu suchen, die dem Kontonamen entspricht. Es gibt zwei Hilfsfunktionen, [**BuildTrusteeWithSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) und [**BuildTrusteeWithName,**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea)die eine **TRUSTEE-Struktur** mit einer angegebenen SID oder einem angegebenen Namen initialisieren. [**Mit BuildTrusteeWithObjectsAndSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) und [**BuildTrusteeWithObjectsAndName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) können Sie eine **TRUSTEE-Struktur** mit objektspezifischen ACE-Informationen initialisieren. Drei weitere Hilfsfunktionen, [**GetTrusteeForm,**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma) [**GetTrusteeName**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)und [**GetTrusteeType,**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea)rufen die Werte der verschiedenen Member einer **TRUSTEE-Struktur** ab.

Der **ptstrName-Member** der [**TRUSTEE-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) kann ein Zeiger auf eine [**OBJECTS AND \_ \_ NAME-**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) oder [**OBJECTS AND \_ \_ SID-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) sein. Diese Strukturen geben Zusätzlich zu einem [Vertrauenstreuhändernamen](object-specific-aces.md) oder einer SID Informationen zu einem objektspezifischen ACE an. Dadurch können Funktionen wie [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) und [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) objektspezifische ACE-Informationen im Vertrauenstreuhänder-Member der [**EXPLICIT \_ ACCESS-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) speichern. 

 

 
