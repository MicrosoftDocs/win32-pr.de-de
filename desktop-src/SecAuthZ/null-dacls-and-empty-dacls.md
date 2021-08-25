---
description: Eine NULL-DACL gewährt jedem Benutzer, der sie angibt, Vollzugriff. Eine leere DACL ist eine ordnungsgemäß zugeordnete und initialisierte DACL, die keine Zugriffssteuerungseinträge enthält. Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: NULL-DACLs und leere DACLs (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c15f9a3aeed120ff91dc19a091232721c623683d90f0c9cdccbc065516eea8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907820"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>NULL-DACLs und leere DACLs (Autorisierung)

Wenn die [*DACL (Discretionary Access Control List),*](/windows/desktop/SecGloss/d-gly) die zum Sicherheitsdeskriptor eines Objekts gehört, auf **NULL** festgelegt ist, wird eine NULL-DACL erstellt. [](/windows/desktop/SecGloss/s-gly) Eine NULL-DACL gewährt jedem Benutzer, der sie angibt, Vollzugriff. Eine normale Sicherheitsüberprüfung wird in Bezug auf das Objekt nicht durchgeführt. Eine NULL-DACL darf nicht mit einer leeren DACL verwechselt werden. Eine leere DACL ist eine ordnungsgemäß zugeordnete und initialisierte DACL, die keine [*Zugriffssteuerungseinträge*](/windows/desktop/SecGloss/a-gly) (ACEs) enthält. Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.

Ein Beispiel zum Erstellen einer DACL finden Sie unter [Erstellen einer DACL.](/windows/desktop/SecBP/creating-a-dacl)

 

 
