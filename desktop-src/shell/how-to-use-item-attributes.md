---
description: Die sfgao-Flagwerte der shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Verwenden von Element Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864912"
---
# <a name="how-to-use-item-attributes"></a>Verwenden von Element Attributen

Die [**sfgao**](sfgao.md) -Flagwerte der shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.

Um dieses Attribut zu verwenden, fügen Sie die folgenden **reg \_ DWORD** -Werte unter dem Verb hinzu:

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Der attributemask-Wert gibt den [**sfgao**](sfgao.md) -Wert der Bitwerte der Maske an, die getestet werden soll.

### <a name="step-2"></a>Schritt 2:

Der AttributeValue-Wert gibt den [**sfgao**](sfgao.md) -Wert der zu testenden Bits an.

### <a name="step-3"></a>Schritt 3:

Das impliedselectionmodel gibt 0 (null) für Element Verben oder einen Wert ungleich 0 (null) für Verben im Hintergrund Kontextmenü an.

## <a name="remarks"></a>Bemerkungen

Im folgenden Beispiel Registrierungs Eintrag wird attributemask auf [**sfgao \_**](sfgao.md) schreibgeschützt (0x40000) festgelegt.

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



