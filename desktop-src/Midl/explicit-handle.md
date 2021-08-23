---
title: explicit_handle-Attribut
description: Das Attribut \explicit handle\ ACF gibt an, dass jede Prozedur als ersten Parameter über ein primitives Handle verfügt, z. \_ B. einen \_ Handle-t-Typ.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle MIDL-Attribut
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b50aa69c43e27b4797f6619b4efa14b90f16dd2b4bee45df2db6b708e58f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013918"
---
# <a name="explicit_handle-attribute"></a>Explizites \_ Handleattribut

Das \[ **\_ explizite Handle-ACF-Attribut** gibt an, dass jede Prozedur als ersten Parameter über ein primitives Handle verfügt, z. B. \] einen Handle [**\_ t-Typ.**](handle-t.md)

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie das **\[ \_ \] explizite Handleattribut** verwenden, verfügt jede Prozedur über ein primitives Handle als ersten Parameter, auch wenn die IDL-Datei dieses Handle nicht in der Parameterliste enthält. Die in die Headerdatei ausgegebenen Prototypen und Stubroutinen enthalten den zusätzlichen Parameter, und dieser Parameter wird als Handle für die Anweisung des Remoteaufrufs verwendet.

Das **\[ explizite \_ \] Handleattribut** wirkt sich sowohl auf Remote- als auch auf Serialisierungsvorgänge aus. Bei der Typserialisierung werden die Unterstützungsroutinen mit dem anfänglichen Parameter als explizites Handle (Serialisierung) generiert. Wenn das **\[ \_ explizite \] Handleattribut** nicht verwendet wird, kann die Anwendung weiterhin angeben, dass ein Vorgang ein explizites Handle (Bindung oder Serialisierung) hat, das den Aufruf leitet. Zu diesem Schritt wird ein Prototyp mit einem Argument, das einen Handletyp enthält, für die IDL-Datei bereitgestellt. Beachten Sie, dass im Standardmodus ein Argument, das nicht zuerst angezeigt wird, auch als Handle verwendet werden kann, das den Aufruf leitet.

Obwohl das **\[ \_ \]** explizite Handleattribut eine Möglichkeit ist, dem IDL-Prototyp ein **\[ \_ \] primitives** explizites Handleattribut zu geben, ist es nicht notwendigerweise eine Änderung der IDL-Datei erforderlich. Im [**/osf-Modus**](-osf.md) kann nur das erste Argument als expliziter Handletyp verwendet werden.

Das **\[ \_ explizite \] Handleattribut** kann entweder als Schnittstellenattribut oder als Vorgangsattribut verwendet werden. Als Schnittstellenattribut wirkt es sich auf alle Vorgänge in der Schnittstelle und alle Typen aus, die Serialisierungsunterstützung erfordern. Wenn sie jedoch als Vorgangsattribut verwendet wird, wirkt sich dies nur auf diesen bestimmten Vorgang aus. Wenn eine Methode mindestens ein in Kontexthandles enthält, wird das linke am meisten im Kontexthandles als Bindungshandles verwendet, und es wird kein \[ \] \[ \] zusätzliches explizites Handle erstellt.

## <a name="examples"></a>Beispiele

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Automatisches \_ Handle**](auto-handle.md)
</dt> <dt>

[**implizites \_ Handle**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




