---
title: enable_allocate-Attribut
description: Das Attribut \enable allocate\ ACF gibt an, dass der \_ Serverstubcode die Stubspeicherverwaltungsumgebung aktivieren soll.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate MIDL-Attribut
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f44b3a2f11094c37edf24f5fc00bbd8229d65dc2a54292acd2ca3221472e85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979620"
---
# <a name="enable_allocate-attribute"></a>Attribut \_ "allocate" aktivieren

Das **\[ Enable \_ allocate \]** ACF-Attribut gibt an, dass der Serverstubcode die Stubspeicherverwaltungsumgebung aktivieren soll.

> [!Note]  
> Das **\[ Attribut enable \_ allocate \]** ist veraltet und wird nicht mehr unterstützt.

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optional-attribute-list* 
</dt> <dd>

Gibt eine Liste mit null oder mehr zusätzlichen MIDL-Attributen an.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Der Name der Schnittstelle, auf die **\[ das Enable \_ allcoate-Attribut \]** angewendet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Im Standardmodus aktiviert der Serverstub die Speicherumgebung nur, wenn das **\[ Attribut enable \_ allocate \]** verwendet wird. Die Speicherverwaltungsumgebung muss aktiviert sein, bevor Arbeitsspeicher mithilfe von [**RpcSmAllocate zugeordnet werden kann.**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate) Im **osf-Modus** (wenn Sie mit dem [**Schalter /osf**](-osf.md) kompilieren) aktiviert der Stub diese Umgebung automatisch oder auf Anforderung, wenn das **\[ Attribut enable \_ allocate \]** verwendet wird.

Der clientseitige Stub kann für die **Rpcss-Speicherverwaltungsumgebung** vertraulich sein. Wenn ein sensibler Clientstub ausgeführt wird, wenn das **Rpcss-Paket** deaktiviert ist, werden die Standardbenutzerzuweisungen bzw. -zuordnungen aufgerufen (z. B. der Midl-Benutzer weist [midl \_ \_](/windows/desktop/Rpc/the-midl-user-allocate-function)user /  [ \_ free \_ zu).](/windows/desktop/Rpc/the-midl-user-free-function) Wenn diese Option aktiviert ist, verwendet das **Rpcss-Paket** das Zuweisungs-/Zuordnungspaar aus dem Paket. Im Standardmodus ist der Client nur dann sensibel, wenn das **\[ Attribut enable \_ allocate \]** verwendet wird. In der Regel wird der clientseitige Stub in der deaktivierten Umgebung ausgeführt. Im **osf-Modus** (wenn Sie mit dem [**Schalter /osf**](-osf.md) kompilieren) ist der Client immer auf die **Rpcss-Speicherverwaltungsumgebung** sensibel, und daher wirkt sich das **\[ Enable \_ \] Allocate-Attribut** nicht auf die Clientstubs aus.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ user \_ free](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 