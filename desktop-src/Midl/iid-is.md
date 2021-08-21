---
title: iid_is-Attribut
description: Das Zeigerattribut \iid is\ gibt die IID der COM-Schnittstelle an, auf die ein \_ Schnittstellenzeiger zeigt.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is MIDL-Attribut
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74553fdb1e3020d49eca7dfdd219354a4690056c45126b3af208395117ade991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383867"
---
# <a name="iid_is-attribute"></a>iid \_ is attribute

Das **\[ iid \_ \]** is-Zeigerattribut gibt die IID der COM-Schnittstelle an, auf die ein Schnittstellenzeiger zeigt.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*limited-expression* 
</dt> <dd>

Gibt einen C-Sprachausdruck an. Der MIDL-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. MIDL lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement- und Dekrementoperatoren zu.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können **\[ iid \_ in Attributlisten \]** für Funktionsparameter und für Struktur- oder Union-Member verwenden. Die Stubs verwenden die IID, um zu bestimmen, wie der Schnittstellenzeiger gemarshallt werden soll. Dies ist nützlich für einen Schnittstellenzeiger, der als Basisklassenparameter typt ist.

Dateien, die das **\[ iid \_ \] is-Attribut** verwenden, müssen mit dem MIDL-Compiler im Standardmodus kompiliert werden, der den [**Schalter /osf nicht**](-osf.md) verwendet.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 




