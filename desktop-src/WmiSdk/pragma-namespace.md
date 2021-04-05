---
description: Fordert an, dass der Compiler die MOF-Datei in den Namespace lädt, der als NamespacePath angegeben ist. Wenn sowohl der MOF-Compiler-n-Namespace-Schalter als auch der \# pragma-Namespace&\# 32; NamespacePath-Befehl verwendet werden, hat der Befehl Vorrang vor dem Switch.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: pragma-Namespace
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
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753688"
---
# <a name="pragma-namespace"></a>pragma-Namespace

Der Präprozessorbefehl " **pragma Namespace** " fordert an, dass der Compiler die MOF-Datei in den als " *Wert von NamespacePath*" angegebenen Namespace lädt. Wenn sowohl der MOF **-Compiler-n-** Namespace-Schalter als auch der **\# pragma Namespace Namespace Namespace** -Befehl verwendet werden, hat der Befehl Vorrang vor dem Switch. 

Im folgenden wird die Syntax beschrieben:


```mof
#pragma namespace ("[Namespace]")
```



*\[ Namespace \]* ist der angegebene Namespace.

Wenn Sie diesen Befehl oder den entsprechenden Befehls Zeilenschalter nicht angeben, verwendet der MOF-Compiler \\ standardmäßig den Standard Namespace.

## <a name="remarks"></a>Bemerkungen

Sie können festlegen, dass Client Skripts und-Anwendungen eine verschlüsselte Verbindung für die Authentifizierung verwenden, indem Sie der MOF-Datei, die den Namespace erstellt, den Wert "Requirements **sencryption** " hinzufügen. Sie können auch einen vorhandenen Namespace ändern, indem Sie dieses Attribut hinzufügen und die MOF-Datei erneut kompilieren. Weitere Informationen **zur Verwendung von**"Requirements" finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Klassen oder Instanzen im \\ Namespace "root Test" platziert werden.


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[**WMI-Standard Qualifizierer**](standard-wmi-qualifiers.md)
</dt> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




