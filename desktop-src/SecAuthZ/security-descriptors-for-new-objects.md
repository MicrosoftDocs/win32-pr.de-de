---
description: Wenn Sie ein Sicherungs fähiges Objekt erstellen, können Sie dem neuen-Objekt eine Sicherheits Beschreibung zuweisen.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Sicherheits Deskriptoren für neue Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3f9af674c83e4fc42448635bc54dfc0bb51b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359892"
---
# <a name="security-descriptors-for-new-objects"></a>Sicherheits Deskriptoren für neue Objekte

Wenn Sie ein Sicherungs fähiges Objekt erstellen, können Sie dem neuen-Objekt eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) zuweisen. Die Funktionen zum Erstellen von Sicherungs fähigen Objekten, wie z. b. " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " oder " [**regkreatekeyex**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)", verfügen über einen Parameter, der auf die Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) verweist, die einen Zeiger auf die Sicherheits Beschreibung des neuen Objekts enthalten kann. Beispielcode, der eine Sicherheits Beschreibung erstellt und dann **regkreatekeyex** aufruft, um die Sicherheits Beschreibung einem neuen Registrierungsschlüssel zuzuweisen, finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).

Die Systemkomponente oder der Server, von der das-Objekt verwaltet wird, kann die angegebene oder die Standard Sicherheits Beschreibung speichern, um Sie als persistentes Attribut des-Objekts zu erstellen. Wenn der Ersteller eines Objekts keinen Sicherheits Deskriptor angibt, verwendet das System geerbte oder standardmäßige Sicherheitsinformationen zum Erstellen einer Sicherheits Beschreibung. Sie können die-Funktionen verwenden, um die Informationen in der Sicherheits Beschreibung eines Objekts zu ändern.

Verzeichnisdienst Objekte, Dateien, Verzeichnisse, Registrierungsschlüssel und Desktops sind Sicherungs fähige Objekte, die über ein übergeordnetes Objekt verfügen können. Wenn Sie eines dieser Objekte erstellen, prüft das System in der Sicherheits Beschreibung des übergeordneten Objekts, ob vererbbare ACEs angezeigt werden. Das System führt in der Regel alle vererbbaren ACEs in den ACLs der Sicherheits Beschreibung des neuen Objekts zusammen. Sie können verhindern, dass eine DACL oder SACL ACEs erbt, indem Sie die von der SE \_ DACL \_ geschützten oder SE \_ SACL \_ -geschützten Bits in den Steuerungs Bits der Sicherheits Beschreibung festlegen. Weitere Informationen finden Sie unter [ACE-Vererbung](ace-inheritance.md).

 

 
