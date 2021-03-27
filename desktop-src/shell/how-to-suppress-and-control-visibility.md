---
description: In diesem Thema erfahren Sie, wie Sie die Sichtbarkeit des Verbs steuern.
title: Unterdrücken der Sichtbarkeit des Verbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215938"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a>Unterdrücken der Sichtbarkeit des Verbs

In diesem Thema erfahren Sie, wie Sie die Sichtbarkeit des Verbs steuern.

## <a name="instructions"></a>Instructions


Sie können Windows-Richtlinien Einstellungen verwenden, um die Sichtbarkeit zu steuern. Verben können durch Richtlinien Einstellungen unterdrückt werden, indem Sie dem Registrierungs Unterschlüssel des Verbs einen **SuppressionPolicy** -Unterschlüssel oder einen **suppressionpolicyex** -GUID-Wert hinzufügen. Legen Sie den Wert des unter Schlüssels **SuppressionPolicy** auf die Richtlinien-ID fest. Wenn die Richtlinie aktiviert ist, werden das Verb und der zugehörige Kontextmenü Eintrag unterdrückt. Mögliche Richtlinien-ID-Werte finden Sie unter der [**Einschränkungs**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) Enumeration.

 

 



