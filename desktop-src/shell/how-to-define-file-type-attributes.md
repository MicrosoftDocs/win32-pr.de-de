---
description: Definieren von Dateityp Attributen in der Registrierung.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Definieren von Dateityp Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864931"
---
# <a name="how-to-define-file-type-attributes"></a>Definieren von Dateityp Attributen

Durch das Zuweisen von Dateityp Attributen zu einer zugeordneten ProgID können Sie einige Aspekte des Verhaltens des Dateityps steuern. Vor Windows Vista konnten diese Attribute Ihnen ermöglichen, den Umfang zu beschränken, in dem der Benutzer die Eigenschaften Registerkarte **Ordneroptionen** verwenden könnte, um verschiedene Aspekte des Dateityps zu ändern, z. b. das Symbol oder die Verben.

Dateityp Attribute sind binäre Flags, die als **reg \_ DWORD** -oder **reg- \_ Binär** Werte im zugeordneten ProgID-Unterschlüssel des Dateityps angegeben werden.

Um Attribute für einen Dateityp zuzuweisen, führen Sie die folgenden Schritte aus.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Fügen Sie dem zugeordneten ProgID-Unterschlüssel des Dateityps einen EditFlags-Eintrag hinzu.

### <a name="step-2"></a>Schritt 2:

Legen Sie den Eintrag auf den entsprechenden Attribut Wert fest.

Im folgenden Beispiel werden die \_ für den MYP-Dateityp festgelegten Attribute "FTA NoRemove (0x00000010)" und "FTA \_ nonewverb (0x00000020)" gezeigt.

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a>Bemerkungen

Die Flags können mit einem logischen OR kombiniert werden, um den Wert eines einzelnen Attributs zu bilden.

Eine Liste der möglichen Dateityp Attribute und ihrer hexadezimalen Werte sowie weitere Informationen zum programmgesteuerten abrufen und Festlegen dieser Werte finden Sie unter [**filetypeattributeflags**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).

 

 



