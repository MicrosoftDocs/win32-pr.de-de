---
description: Der Zugriffssteuerungs-Editor kann eine Überwachungseigenschaftsseite enthalten, die es dem Benutzer ermöglicht, die Zugriffssteuerungseinträge (ACCESS Control Entries, ACEs) in einer Systemzugriffssteuerungsliste (SACL) für Objekte anzuzeigen und zu bearbeiten. Weitere Informationen zu SACLs finden Sie unter Access Control Lists (ACLs).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Eigenschaftenseite "Überwachung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf116a9079c5b7b6dfeb7e6df57b45d6a0a2555c14de88a32fee4fadcdc6373
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784318"
---
# <a name="auditing-property-page"></a>Eigenschaftenseite "Überwachung"

Der Zugriffssteuerungs-Editor  kann eine Überwachungseigenschaftsseite enthalten, die es dem Benutzer ermöglicht, die Zugriffssteuerungseinträge (ACCESS [*Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) in der Systemzugriffssteuerungsliste (SACL) eines Objekts anzuzeigen und zu bearbeiten. [](/windows/desktop/SecGloss/s-gly) Weitere Informationen zu SACLs finden Sie unter [Access Control Lists](access-control-lists.md) (ACLs).

**So zeigen Sie die Eigenschaftenseite "Überwachung" an**

-   Klicken Sie [auf der Eigenschaftenseite grundlegende Sicherheit](basic-security-property-page.md)auf **Erweitert.** Die **Eigenschaftenseite** Überwachung befindet sich im [Erweiterten Sicherheitseigenschaftsblatt](advanced-security-property-sheet.md).

Legen Sie zum Hinzufügen der **Eigenschaftenseite** Überwachung die **SI \_ ADVANCED-** und **SI EDIT \_ \_ AUDITS-Flags** in der SI OBJECT [**\_ \_ INFO-Struktur**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) fest, die von Ihrer [**ISecurityInformation::GetObjectInformation-Implementierung zurückgegeben**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) wird.

 

 
