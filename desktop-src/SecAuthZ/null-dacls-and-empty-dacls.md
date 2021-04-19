---
description: Eine NULL-DACL gewährt allen Benutzern, die Sie anfordert, vollen Zugriff. Eine leere DACL ist eine ordnungsgemäß zugewiesene und initialisierte DACL, die keine Zugriffs Steuerungs Einträge enthält. Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: Null-DACLs und leere DACLs (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364180"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>Null-DACLs und leere DACLs (Autorisierung)

Wenn die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL), die zur [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) eines Objekts gehört, auf **null** festgelegt ist, wird eine NULL-DACL erstellt. Eine DACL mit NULL gewährt allen Benutzern Vollzugriff, die Sie anfordern. die normale Sicherheitsüberprüfung wird nicht in Bezug auf das-Objekt ausgeführt. Eine NULL-DACL darf nicht mit einer leeren DACL verwechselt werden. Eine leere DACL ist eine ordnungsgemäß zugewiesene und initialisierte DACL, die keine [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) enthält. Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.

Ein Beispiel für das Erstellen einer DACL finden Sie unter [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
