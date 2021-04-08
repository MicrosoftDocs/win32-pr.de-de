---
title: iid_is-Attribut
description: Das Attribut \ IID \_ is \ Pointer gibt die IID der COM-Schnittstelle an, auf die von einem Schnittstellen Zeiger verwiesen wird.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037820"
---
# <a name="iid_is-attribute"></a>IID \_ ist Attribut

Die **\[ IID \_ ist \]** ein Zeiger Attribut, das die IID der COM-Schnittstelle angibt, auf die von einem Schnittstellen Zeiger verwiesen wird.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*eingeschränkter Ausdruck* 
</dt> <dd>

Gibt einen C-sprach Ausdruck an. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. "Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können **\[ IID \_ \]** in Attribut Listen für Funktionsparameter und für Struktur-oder Union-Member verwenden. Die stuader verwenden die IID, um zu bestimmen, wie der Schnittstellen Zeiger gemarshallt werden soll. Dies ist nützlich für einen Schnittstellen Zeiger, der als Basisklassen Parameter typisiert ist.

Dateien, die das **\[ IID \_ \]** -Attribut verwenden, müssen mit dem mittlerer l-Compiler im Standardmodus kompiliert werden, der nicht den [**/OSF**](-osf.md) -Schalter verwendet.

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

[**UUID**](uuid.md)
</dt> </dl>

 

 




