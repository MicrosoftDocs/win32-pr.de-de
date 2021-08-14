---
description: Definieren von Dateitypattributen in der Registrierung.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Definieren von Dateitypattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0a89f5770b55521ccdf51859bdde69ed58d05f864385e46f1d76e482319c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223574"
---
# <a name="how-to-define-file-type-attributes"></a>Definieren von Dateitypattributen

Durch das Zuweisen von Dateitypattributen zu einer zugeordneten ProgID können Sie einige Aspekte des Verhaltens des Dateityps steuern. Vor Windows Vista konnten Sie mit diesen Attributen einschränken, in welchem  Umfang der Benutzer die Eigenschaftenregisterkarte Ordneroptionen verwenden kann, um verschiedene Aspekte des Dateityps zu ändern, z. B. das Symbol oder verben.

Dateitypattribute sind binäre Flags, die als **REG \_ DWORD-** oder **REG \_ BINARY-Werte** im zugeordneten ProgID-Unterschlüssel des Dateityps angegeben werden.

Führen Sie die folgenden Schritte aus, um Attribute für einen Dateityp zu zuweisen.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Fügen Sie dem zugeordneten Unterschlüssel ProgID des Dateityps einen EditFlags-Eintrag hinzu.

### <a name="step-2"></a>Schritt 2:

Legen Sie den Eintrag auf den entsprechenden Attributwert fest.

Das folgende Beispiel zeigt die \_ FTA-Attribute NoRemove (0x00000010) und FTA \_ NoNewVerb (0x00000020), die für den .myp-Dateityp festgelegt sind.

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a>Hinweise

Die Flags können mit einem logischen OR kombiniert werden, um den einzelnen Attributwert zu bilden.

Eine Liste der möglichen Dateitypattribute und deren Hexadezimalwerte sowie weitere Details zum programmgesteuerten Abrufen und Festlegen dieser Werte finden Sie unter [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).

 

 



