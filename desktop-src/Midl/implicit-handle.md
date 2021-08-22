---
title: implicit_handle-Attribut
description: Das Attribut \implicit handle\ ACF gibt das Handle an, das für Funktionen verwendet wird, die kein explizites Handle \_ als Prozedurparameter enthalten.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle MIDL-Attribut
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c53ded4c7459be8f0c8eb98f3770d88ff88a9b7da20cb3482c1032a4f74e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013808"
---
# <a name="implicit_handle-attribute"></a>Implizites \_ Handleattribut

Das **\[ \_ implizite \] Handle-ACF-Attribut** gibt das Handle an, das für Funktionen verwendet wird, die kein explizites Handle als Prozedurparameter enthalten.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*handle-type* 
</dt> <dd>

Gibt den Handledatentyp an, z. B. das [**Basistyphand \_ handle t**](handle-t.md) oder einen benutzerdefinierten Handletyp.

</dd> <dt>

*handle-name* 
</dt> <dd>

Gibt den Namen des Handles an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das vom impliziten **\[ Handleattribut \_ \]** angegebene Handle wird je nach Art der Prozedur auf unterschiedliche Weise verwendet. Wenn die Prozedur remote ist, wird das Handle als Bindungshand handle für den Remoteaufruf verwendet. Das implizite Handle kann auch verwendet werden, um eine anfängliche Bindung für eine Funktion zu erstellen, die ein Kontexthand handle verwendet. Wenn es sich bei der Prozedur um eine Serialisierungsprozedur handelt, wird das Handle als serialisierendes Handle verwendet, das den Vorgang steuert. Bei der Typserialisierung wird das Handle als Serialisierungshand handle für alle serialisierten Typen verwendet.

Das **\[ \_ implizite \] Handleattribut** gibt eine globale Variable an, die ein Handle enthält, das von jeder Funktion verwendet wird, die implizite Handles benötigt.

Der implizite Bindungshandpunkttyp muss entweder handle [**\_ t**](handle-t.md) (oder ein Typ, der auf handle **\_ t** basiert) oder ein benutzerdefinierter Handletyp sein, der mit dem [**Handleattribut angegeben**](handle.md) wird. Das implizite Serialisierungshand handle muss ein Typ sein, der auf **handle \_ t basiert.**

Wenn der implizite Handletyp nicht in der IDL-Datei oder in Dateien definiert ist, die in der IDL-Datei für den MIDL-Computer enthalten und importiert wurden, müssen Sie die Datei mit der Handletypdefinition beim Kompilieren der Stubs eingeben. Verwenden Sie die [**Include-Anweisung von**](include.md) ACF, um die Datei mit der Handletypdefinition ein include.

Das **\[ \_ implizite \] Handleattribut** kann mindestens einmal auftreten. Das **\[ \_ implizite \] Handleattribut** kann nur auftreten, [**\[ \_ \]**](auto-handle.md) wenn das automatische Handle und [**\[ explizite \_ \]**](explicit-handle.md) Handleattribute nicht auftreten.

## <a name="examples"></a>Beispiele

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Automatisches \_ Handle**](auto-handle.md)
</dt> <dt>

[**Explizites \_ Handle**](explicit-handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**include**](include.md)
</dt> </dl>

 

 




