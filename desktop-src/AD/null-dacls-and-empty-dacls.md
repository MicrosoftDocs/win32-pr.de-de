---
title: NULL-DACLs und leere DACLs (AD DS)
description: Das Vorhandensein einer NULL-DACL (Discretionary Access Control List) im nTSecurityDescriptor-Attribut eines beliebigen Objekts kann ein schwerwiegendes Sicherheitsrisiko darstellen.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- NULL-DACLs und leere DACLs AD
- DACLs AD, NULL und Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41e03917c1190b7926eca11db038e2143bcb91d142e0617d143d4d80bb6e601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185795"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>NULL-DACLs und leere DACLs (AD DS)

Das Vorhandensein einer NULL-DACL (Discretionary Access Control List) im [**nTSecurityDescriptor-Attribut**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) eines beliebigen Objekts kann ein schwerwiegendes Sicherheitsrisiko darstellen. Eine NULL-DACL gewährt allen Benutzern, die sie anfordern, Vollzugriff. eine normale Sicherheitsüberprüfung wird in Bezug auf das Objekt nicht durchgeführt. Eine NULL-DACL darf nicht mit einer leeren DACL verwechselt werden. Eine leere DACL ist eine ordnungsgemäß zugeordnete und initialisierte DACL, die keine Zugriffssteuerungseinträge (ACCESS Control Entries, ACEs) enthält. Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.

Weitere Informationen finden Sie unter [NULL-DACLs und Leere DACLs.](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls)

 

 