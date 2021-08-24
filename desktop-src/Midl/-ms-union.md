---
title: /ms_union Switch
description: Der \_ /ms union-Schalter steuert die NDR-Ausrichtung von nicht gekapselten Unions. Hinweis Dieses Attribut wird aus Gründen der Abwärtskompatibilität bereitgestellt.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union Switch MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b8e2f4b86929954ad67c845cf546d46f5950698fce7c21d721613af3611a066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811390"
---
# <a name="ms_union-switch"></a>\_/ms union switch

Der **/ms \_ union-Schalter** steuert die NDR-Ausrichtung von nicht gekapselten Unions.

> [!Note]  
> Dieses Attribut wird aus Gründen der Abwärtskompatibilität bereitgestellt. Es wird nicht für die Verwendung in einer neuen Schnittstelle empfohlen.

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Der MIDL-Compiler spiegelt das Verhalten des OSF-DCE-IDL-Compilers für nicht gekapselte Unions wider. Da frühere Versionen des MIDL-Compilers dies jedoch nicht getan haben, bietet der **\_ /ms-Union-Switch** Kompatibilität mit Schnittstellen, die auf früheren Versionen des MIDL-Compilers basierten.

Das Feature ms \_ union kann als Befehlszeilenschalter (**/ms \_ union**), als IDL-Schnittstellenattribut oder als IDL-Typattribut verwendet werden.

## <a name="examples"></a>Beispiele

**midl /ms \_ union file.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> </dl>

 

 




