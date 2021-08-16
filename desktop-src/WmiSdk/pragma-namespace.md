---
description: Fordert an, dass der Compiler die MOF-Datei in den als namespacepath angegebenen Namespace geladen. Wenn sowohl der MOF-Compiler -n-Namespaceschalter als auch der \# Pragmanamespace&32;Namespacepath-Befehl verwendet werden, hat der Befehl Vorrang \# vor dem Switch.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: Pragmanamespace
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
ms.openlocfilehash: d3eea58c8e32ab8b1b851205b365b837194d0472a1c39017e2eb69dc3fe70a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316826"
---
# <a name="pragma-namespace"></a>Pragmanamespace

Der **Präprozessorbefehl pragma namespace** fordert an, dass der Compiler die MOF-Datei in den *namespacepath angegebenen Namespace laden soll.* Wenn sowohl der MOF-Compiler **-n-Namespaceschalter** als auch der **\# Pragmanamespacenamespacepath-Befehl** verwendet werden, hat der Befehl Vorrang vor dem Schalter. 

Im Folgenden wird die Syntax beschrieben:


```mof
#pragma namespace ("[Namespace]")
```



*\[ Namespace \]* ist der angegebene Namespace.

Wenn Sie diesen Befehl oder den entsprechenden Befehlszeilenschalter nicht angeben, verwendet der MOF-Compiler standardmäßig den Standardnamespace des \\ Stamms.

## <a name="remarks"></a>Hinweise

Sie können festlegen, dass Clientskripts und Anwendungen eine verschlüsselte Verbindung für die Authentifizierung verwenden, indem Sie den **RequiresEncryption-Qualifizierer** der MOF-Datei hinzufügen, die den Namespace erstellt. Sie können auch einen vorhandenen Namespace ändern, indem Sie dieses Attribut hinzufügen und die MOF-Datei erneut kompilieren. Weitere Informationen zur Verwendung von **RequiresEncryption finden** Sie unter [Erfordern einer verschlüsselten Verbindung mit einem Namespace.](requiring-an-encrypted-connection-to-a-namespace.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Klassen oder Instanzen im Namespace \\ "Stammtest" platzieren.


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Festlegen von Namepace-Sicherheitsdeskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[**WMI-Standardqualifizierer**](standard-wmi-qualifiers.md)
</dt> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




