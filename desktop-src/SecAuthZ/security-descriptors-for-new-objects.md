---
description: Wenn Sie ein sicherungsfähiges Objekt erstellen, können Sie dem neuen Objekt einen Sicherheitsdeskriptor zuweisen.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Sicherheitsbeschreibungen für neue Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38edc927f1f017e3f102194b0a4aac5d0442ec730e8480a00c054add0935a62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907340"
---
# <a name="security-descriptors-for-new-objects"></a>Sicherheitsbeschreibungen für neue Objekte

Wenn Sie ein sicherungsfähiges Objekt [](/windows/desktop/SecGloss/s-gly) erstellen, können Sie dem neuen Objekt einen Sicherheitsdeskriptor zuweisen. Die Funktionen zum Erstellen sicherungsfähiger Objekte wie [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) oder [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)verfügen über einen Parameter, der auf die [**SECURITY \_ ATTRIBUTES-Struktur**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) verweist, die einen Zeiger auf den Sicherheitsdeskriptor des neuen Objekts enthalten kann. Beispielcode, der einen Sicherheitsdeskriptor erstellt und dann **RegCreateKeyEx** aufruft, um den Sicherheitsdeskriptor einem neuen Registrierungsschlüssel zu zuweisen, finden Sie unter [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)(Erstellen eines Sicherheitsdeskriptors für ein neues Objekt in C++).

Die Systemkomponente oder der Server, die bzw. der das Objekt verwaltet, kann den angegebenen oder Standardsicherheitsdeskriptor speichern, um ihn zu einem persistenten Attribut des Objekts zu machen. Wenn der Ersteller eines Objekts keinen Sicherheitsdeskriptor anordnt, verwendet das System geerbte oder Standardsicherheitsinformationen, um einen Sicherheitsdeskriptor zu erstellen. Sie können Funktionen verwenden, um die Informationen in der Sicherheitsbeschreibung eines Objekts zu ändern.

Verzeichnisdienstobjekte, Dateien, Verzeichnisse, Registrierungsschlüssel und Desktops sind sicherungsfähige Objekte, die über ein übergeordnetes Objekt verfügen können. Wenn Sie eines dieser Objekte erstellen, überprüft das System im Sicherheitsdeskriptor des übergeordneten Objekts auf vererbbare ACEs. Das System führt in der Regel alle vererbten ACEs mit den ACLs des Sicherheitsdeskriptors des neuen Objekts zusammen. Sie können verhindern, dass eine DACL oder SACL ACEs erbt, indem Sie die SE \_ DACL PROTECTED- oder \_ SE SACL PROTECTED-Bits in den Steuerungsbits des Sicherheitsdeskriptors \_ \_ festlegen. Weitere Informationen finden Sie unter [ACE-Vererbung.](ace-inheritance.md)

 

 
