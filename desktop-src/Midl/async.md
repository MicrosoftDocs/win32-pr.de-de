---
title: Async-Attribut
description: Das Attribut \ Async \ ACF definiert einen Remote Prozedur Aufrufvorgang als asynchronen Vorgang.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- Async-Attribut, Mittel l
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948659"
---
# <a name="async-attribute"></a>Async-Attribut

Das \[ **Async** - \] ACF-Attribut definiert einen Remote Prozedur Aufrufvorgang als asynchronen Vorgang.

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Opt-ACF-Attribute* 
</dt> <dd>

Gibt optionale Anwendungs Konfigurations Attribute an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion in der IDL-Datei an.

</dd> <dt>

*param-Liste* 
</dt> <dd>

Gibt eine optionale Parameterliste an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist in COM-Schnittstellen nicht anwendbar.

Um eine RPC-Funktion als asynchron zu deklarieren, deklarieren Sie zuerst die Funktion als Teil einer Schnittstellen Definition in einer IDL-Datei. Ändern Sie dann die Funktionsdeklaration in der Anwendungs Konfigurationsdatei (ACF), indem Sie das \[ **Async** - \] Attribut anwenden. Beachten Sie, dass die Funktionsdeklaration das asynchrone Handle nicht erwähnt und dass das Bindungs Handle der erste Parameter ist. \[Wenn Sie das **Async** - \] Attribut in der ACF-Datei anwenden, wird der entsprechende Code generiert, damit der asynchrone Server beim Aufrufen dieser Funktion erwartet, dass vor den anderen Parametern ein asynchrones handle empfangen wird.

> [!Note]  
> Das Async-Attribut kann nicht mit dem [**/OSF**](-osf.md) -Befehls Zeilenschalter verwendet werden.

 

## <a name="examples"></a>Beispiele

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Asynchroner RPC](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 