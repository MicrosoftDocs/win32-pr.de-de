---
description: SACL für ein neues Objekt
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL für ein neues Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f9833fcfb45a612b6135579e44aca6f219661fd2aeb2998b899e5794fa7bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413840"
---
# <a name="sacl-for-a-new-object"></a>SACL für ein neues Objekt

Das System verwendet den folgenden Algorithmus, um eine SACL für die meisten Typen neuer sicherungsfähiger Objekte zu erstellen:

1.  Die SACL des Objekts ist die SACL aus dem [*Sicherheitsdeskriptor,*](/windows/desktop/SecGloss/s-gly) der vom Ersteller des Objekts angegeben wird. Das System führt alle vererbbaren ACEs mit der angegebenen SACL zusammen, es sei denn, das SE \_ SACL \_ PROTECTED-Bit wird in den Steuerungsbits des Sicherheitsdeskriptors festgelegt. SYSTEM \_ RESOURCE \_ ATTRIBUTE \_ ACEs und SYSTEM \_ SCOPED POLICY ID \_ \_ \_ ACEs aus einem übergeordneten Objekt werden mit einem neuen -Objekt zusammengeführt, auch wenn das SE \_ SACL \_ PROTECTED-Bit festgelegt ist.
2.  Wenn der Ersteller keinen Sicherheitsdeskriptor angibt, erstellt das System die SACL des Objekts aus vererbbaren ACEs.
3.  Wenn keine angegebene oder geerbte SACL vorhanden ist, verfügt das Objekt über keine SACL.

Um eine SACL für ein neues Objekt anzugeben, muss für den Ersteller des Objekts die SE \_ SECURITY \_ [NAME-Berechtigung](privileges.md) aktiviert sein. Wenn die angegebene SACL für ein neues -Objekt nur SYSTEM \_ RESOURCE \_ \_ ATTRIBUTE-ACEs enthält, ist die SE \_ SECURITY \_ NAME-Berechtigung nicht erforderlich. Der Ersteller benötigt diese Berechtigung nicht, wenn die SACL des Objekts aus geerbten ACEs erstellt wird.

Das System verwendet einen anderen Algorithmus, um eine SACL für ein neues Active Directory-Objekt zu erstellen. Weitere Informationen finden Sie unter Festlegen von [Sicherheitsbeschreibungen für neue Verzeichnisobjekte.](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects)

 

 
