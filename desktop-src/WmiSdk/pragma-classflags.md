---
description: Steuert die Art und Weise, wie WMI Klassen abhängig von den angegebenen Flags erstellt oder aktualisiert.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347262"
---
# <a name="pragma-classflags"></a>pragma classflags

Der **pragma classflags** -Präprozessorbefehl steuert die Art und Weise, wie WMI Klassen abhängig von den angegebenen Flags erstellt oder aktualisiert.

Im folgenden wird die Syntax für diesen Befehl beschrieben:


```mof
#pragma classflags ("[flag1], [flag2]")
```



Das *\[ Flag \]* muss mindestens eines der folgenden Argumente aufweisen. Sie können alle Flags kombinieren, die einander nicht widersprechen.



| Flag        | Beschreibung                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| createonly  | Weist den Compiler an, keine Änderungen an vorhandenen Klassen vorzunehmen, und beendet eine Kompilierung, wenn eine in der MOF-Datei angegebene Klasse bereits in WMI vorhanden ist.                                                                                                                                                                                                        |
| ForceUpdate | Erzwingt das Aktualisieren von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind. Wenn Sie z. b. einen Klassen Qualifizierer in einer untergeordneten Klasse definieren und die Basisklasse versucht, denselben Qualifizierer hinzuzufügen, bewirkt die Verwendung dieses Flags, dass der Compiler diesen Konflikt durch Löschen des in Konflikt stehenden Qualifizierers in der untergeordneten Klasse löst. Wenn die untergeordnete Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl. |
| safeupdate  | Ermöglicht dem Compiler, Klassen zu aktualisieren, auch wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht. Mithilfe dieses Flags können Sie z. b. einer Basisklasse eine neue Eigenschaft hinzufügen, ohne dass die Eigenschaft auch einer bereits vorhandenen untergeordneten Klasse hinzugefügt werden muss. Wenn die untergeordneten Klassen Instanzen aufweisen, schlägt die Aktualisierung fehl.                           |
| updateonly  | Weist den Compiler an, keine neuen Klassen zu erstellen, und bewirkt, dass der Compiler die Kompilierung beendet, wenn eine in der MOF-Datei angegebene Klasse nicht vorhanden ist.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie diesen Befehl mit den Flags updateonly und ForceUpdate verwenden können.


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




