---
title: /Ms_union Schalter
description: Der/MS- \_ Union-Switch steuert die NDR-Ausrichtung von nicht gekapselten Unions. Hinweis Dieses Attribut wird aus Gründen der Abwärtskompatibilität bereitgestellt.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /Ms_union-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857548"
---
# <a name="ms_union-switch"></a>/MS \_ Union-Switch

Der **/MS- \_ Union** -Switch steuert die NDR-Ausrichtung von nicht gekapselten Unions.

> [!Note]  
> Dieses Attribut wird aus Gründen der Abwärtskompatibilität bereitgestellt. Es wird nicht empfohlen, in einer neuen-Schnittstelle zu verwenden.

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Der mittlerer l-Compiler spiegelt das Verhalten des OSF-DCE-IDL-Compilers für nicht gekapselte Unions wider. Da jedoch frühere Versionen des Mittel l-Compilers dies nicht getan haben, bietet der **/MS \_ Union** -Switch Kompatibilität mit Schnittstellen, die auf früheren Versionen des Mittel l-Compilers erstellt wurden.

Die MS \_ -Union-Funktion kann als Befehls Zeilenschalter (**/MS \_ Union**), als idl-Schnittstellen Attribut oder als IDL-Type-Attribut verwendet werden.

## <a name="examples"></a>Beispiele

**Mittel l/MS \_ Union file. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




