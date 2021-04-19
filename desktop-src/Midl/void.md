---
title: void-Attribut
description: Der Basistyp void gibt eine Prozedur ohne Argumente oder eine Prozedur an, die keinen Ergebniswert zurückgibt.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- void-Attribut-Mittel l
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339249"
---
# <a name="void-attribute"></a>void-Attribut

Der Basistyp **void** gibt eine Prozedur ohne Argumente oder eine Prozedur an, die keinen Ergebniswert zurückgibt.

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-List* 
</dt> <dd>

Gibt die Liste der Parameter an, die an die Funktion übergeben werden, zusammen mit den zugeordneten Parametertypen und Parameter Attributen.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Gibt den Namen des Typs an, der von der Funktion zurückgegeben wird.

</dd> <dt>

*Context-Handle-type* 
</dt> <dd>

Gibt den Namen des Typs an, der das **\[** [**Kontext \_ handle**](context-handle.md) - **\]** Attribut annimmt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zeigertyp " **void \***", der in C einen generischen Zeiger beschreibt, der in einen beliebigen Zeigertyp umgewandelt werden kann, ist in der mittleren l auf seine Verwendung mit dem **\[ Kontext \_ handle \]** -Schlüsselwort begrenzt.

## <a name="examples"></a>Beispiele

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




