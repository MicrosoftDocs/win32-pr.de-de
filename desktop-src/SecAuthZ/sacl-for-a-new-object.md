---
description: SACL für ein neues Objekt
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL für ein neues Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356526"
---
# <a name="sacl-for-a-new-object"></a>SACL für ein neues Objekt

Das System verwendet den folgenden Algorithmus, um eine SACL für die meisten Typen von neuen Sicherungs fähigen Objekten zu erstellen:

1.  Die SACL des Objekts ist die SACL aus der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) , die durch den Ersteller des Objekts angegeben wird. Das System führt alle vererbbaren ACEs in der angegebenen SACL zusammen, es sei denn, das \_ geschützte SE SACL \_ -Bit wird in den Steuerungs Bits der Sicherheits Beschreibung festgelegt. \_ \_ Systemressourcenattribute \_ -ACEs und systemweite \_ \_ Richtlinien- \_ ID- \_ ACEs von einem übergeordneten Objekt werden mit einem neuen-Objekt zusammengeführt, auch wenn das "SE \_ SACL \_ Protected Bit" festgelegt ist.
2.  Wenn der Ersteller keine Sicherheits Beschreibung angibt, erstellt das System die SACL des Objekts aus vererbbaren ACEs.
3.  Wenn keine angegebene oder geerbte SACL vorhanden ist, hat das-Objekt keine SACL.

Um eine SACL für ein neues Objekt anzugeben, muss für den Ersteller des Objekts die \_ Sicherheits \_ Namen [Berechtigung](privileges.md) "SE" aktiviert sein. Wenn die angegebene SACL für ein neues-Objekt nur das System \_ Ressourcen \_ Attribut ACEs enthält \_ , ist die Berechtigung "SE \_ Security Name" \_ nicht erforderlich. Der Ersteller benötigt diese Berechtigung nicht, wenn die SACL des Objekts aus geerbten ACEs erstellt wird.

Das System verwendet einen anderen Algorithmus, um eine SACL für ein neues Active Directory Objekt zu erstellen. Weitere Informationen finden Sie unter [Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
