---
title: void-Attribut
description: Der Basistyp void gibt eine Prozedur ohne Argumente oder eine Prozedur an, die keinen Ergebniswert zurückgibt.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- void-Attribut MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad758ba334114e13493e7b082f45f37dc6e68efba16dc3a55f14fa57a772d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382436"
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

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*parameter-list* 
</dt> <dd>

Gibt die Liste der Parameter an, die zusammen mit den zugeordneten Parametertypen und Parameterattributen an die Funktion übergeben werden.

</dd> <dt>

*rückgabetyp* 
</dt> <dd>

Gibt den Namen des typs an, der von der Funktion zurückgegeben wird.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Gibt den Namen des Typs an, der das **\[** [**\_ Kontexthandleattribut**](context-handle.md) **\]** annimmt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zeigertyp **void _, der in C einen generischen Zeiger beschreibt, der zur Darstellung jedes \* *Zeigertyps typisiert werden kann, ist in MIDL auf seine Verwendung mit dem* \[ _context \_ \] handle-Schlüsselwort beschränkt.**

## <a name="examples"></a>Beispiele

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**\_Kontexthandle**](context-handle.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> </dl>

 

 




