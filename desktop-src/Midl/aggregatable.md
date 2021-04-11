---
title: Aggregierbares Attribut
description: Das Attribut \ aggregatable \ gibt an, dass die Klasse Aggregationen unterstützt.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- Zusammenfassung des aggregierbare-Attributs
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314841"
---
# <a name="aggregatable-attribute"></a>Aggregierbares Attribut

Das Aggregat Attribut gibt an, dass die-Klasse **\[ Aggregationen \]** unterstützt.

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*coclass-Attribute-List* 
</dt> <dd>

Andere Attribute, die auf die-Klasse angewendet werden.

</dd> <dt>

*Name der Co-Klasse* 
</dt> <dd>

Der Name der Klasse.

</dd> <dt>

*coclass-Interface-List* 
</dt> <dd>

Eine Liste der Schnittstellen für die-Klasse.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **\[ aggregierbare \]** -Attribut einer [**Co-Klasse**](coclass.md) -Anweisung, um den Benutzern mitzuteilen, dass die-Klasse Aggregationen unterstützt. Das heißt, die-Klasse ermöglicht es, dass ihre Schnittstellen von einer Container Klasse verfügbar gemacht werden, als wären diese Schnittstellen die eigenen Schnittstellen des Containers.

Die TYPEFLAG-Darstellung für dieses Attribut ist "TYPEFLAG" \_ .

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 