---
description: Steuert die Art und Weise, wie WMI Klassen erstellt oder aktualisiert, abhängig von den angegebenen Flags.
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
ms.openlocfilehash: 6fd2b8ec75bd0521ce31af1ee7ce9dba2d9498890f9b5ddc768463f733322cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996320"
---
# <a name="pragma-classflags"></a>pragma classflags

Der **Präprozessorbefehl pragma classflags** steuert die Art und Weise, wie WMI Klassen erstellt oder aktualisiert, je nach den angegebenen Flags.

Im Folgenden wird die Syntax für diesen Befehl beschrieben:


```mof
#pragma classflags ("[flag1], [flag2]")
```



*\[ Das \] Flag* muss mindestens eines der folgenden Argumente sein. Sie können alle Flags kombinieren, die einander nicht widerspricht.



| Flag        | Beschreibung                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| createonly  | Weist den Compiler an, keine Änderungen an vorhandenen Klassen vorzunehmen, und beendet eine Kompilierung, wenn eine in der MOF-Datei angegebene Klasse bereits in WMI vorhanden ist.                                                                                                                                                                                                        |
| Forceupdate | Erzwingt Aktualisierungen von Klassen, wenn in Konflikt stehende untergeordnete Klassen vorhanden sind. Wenn Sie z. B. einen Klassenqualifizierer in einer untergeordneten Klasse definieren und die Basisklasse versucht, den gleichen Qualifizierer hinzuzufügen, bewirkt die Verwendung dieses Flags, dass der Compiler diesen Konflikt löst, indem der in Konflikt stehtde Qualifizierer in der untergeordneten Klasse gelöscht wird. Wenn die untergeordnete Klasse Über -Instanzen verfügt, schlägt das Update fehl. |
| Safeupdate  | Ermöglicht dem Compiler, Klassen auch dann zu aktualisieren, wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht. Mit diesem Flag können Sie z. B. einer Basisklasse eine neue Eigenschaft hinzufügen, ohne die Eigenschaft auch einer bereits vorhandenen untergeordneten Klasse hinzufügen zu müssen. Wenn die untergeordneten Klassen Über -Instanzen verfügen, schlägt das Update fehl.                           |
| updateonly  | Weist den Compiler an, keine neuen Klassen zu erstellen, und bewirkt, dass der Compiler die Kompilierung beendet, wenn keine in der MOF-Datei angegebene Klasse vorhanden ist.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung dieses Befehls mit den Flags updateonly und forceupdate veranschaulicht.


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




