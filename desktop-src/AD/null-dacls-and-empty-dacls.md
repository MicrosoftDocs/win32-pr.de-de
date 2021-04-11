---
title: Null-DACLs und leere DACLs (AD DS)
description: Das vorhanden sein einer nicht freigegebenen Zugriffs Steuerungs Liste (DACL) im ntSecurityDescriptor-Attribut eines Objekts kann ein schwerwiegendes Sicherheitsrisiko darstellen.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- Null DACLs und leere DACLs AD
- DACLs AD, NULL und leer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948554"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>Null-DACLs und leere DACLs (AD DS)

Das vorhanden sein einer nicht freigegebenen Zugriffs Steuerungs Liste (DACL) im [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) -Attribut eines Objekts kann ein schwerwiegendes Sicherheitsrisiko darstellen. Eine DACL mit NULL gewährt allen Benutzern Vollzugriff, die Sie anfordern. die normale Sicherheitsüberprüfung wird nicht in Bezug auf das-Objekt ausgeführt. Eine NULL-DACL darf nicht mit einer leeren DACL verwechselt werden. Eine leere DACL ist eine ordnungsgemäß zugewiesene und initialisierte DACL, die keine Zugriffs Steuerungs Einträge (ACEs) enthält. Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.

Weitere Informationen finden Sie unter [null-DACLs und leere DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).

 

 