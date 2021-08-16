---
description: Die SFGAO-Flagwerte der Shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Verwenden von Elementattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ddcc567a820ba1d9c1394ca38f78fc9ce9ec634596f8dbe41feca9def32e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859569"
---
# <a name="how-to-use-item-attributes"></a>Verwenden von Elementattributen

Die [**SFGAO-Flagwerte**](sfgao.md) der Shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.

Um dieses Attributfeature zu verwenden, fügen Sie die folgenden **REG \_ DWORD-Werte** unter dem Verb hinzu:

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Der AttributeMask-Wert gibt den [**SFGAO-Wert**](sfgao.md) der Bitwerte der Maske an, mit der getestet werden soll.

### <a name="step-2"></a>Schritt 2:

Der AttributeValue-Wert gibt den [**SFGAO-Wert**](sfgao.md) der getesteten Bits an.

### <a name="step-3"></a>Schritt 3:

Das ImpliedSelectionModel gibt 0 (null) für Elementverben oder einen Wert ungleich 0 (null) für Verben im Kontextmenü im Hintergrund an.

## <a name="remarks"></a>Hinweise

Im folgenden Beispielregistrierungseintrag ist AttributeMask auf [**SFGAO \_ READONLY**](sfgao.md) (0x40000) festgelegt.

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

 

 



