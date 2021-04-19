---
title: explicit_handle-Attribut
description: Das \ explizite \_ handle \ ACF-Attribut gibt an, dass jede Prozedur als ersten Parameter ein Primitives handle, z. b. ein Handle t-Typ, aufweist \_ .
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341894"
---
# <a name="explicit_handle-attribute"></a>explizites \_ handle

Das \[ **explizite \_ handle** - \] ACF-Attribut gibt an, dass jede Prozedur als ersten Parameter ein Primitives handle, z. b. ein [**handle \_ t**](handle-t.md) -Typ, aufweist.

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

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie das **\[ explizite \_ handle \]** -Attribut verwenden, verfügt jede Prozedur über ein Primitives Handle als ersten Parameter, auch wenn die IDL-Datei dieses Handle nicht in der Parameterliste enthält. Die Prototypen, die an die Header Datei und die Stub-Routinen ausgegeben werden, enthalten den zusätzlichen Parameter, und dieser Parameter wird als Handle zum Weiterleiten des Remote Aufrufes verwendet.

Das **\[ explizite \_ handle \]** -Attribut wirkt sich auf Remote Prozeduren und Serialisierungsprozesse aus Bei der Typserialisierung werden die Unterstützungs Routinen mit dem anfänglichen Parameter als explizites (Serialisierungs-) handle generiert. Wenn das **\[ explizite \_ handle \]** -Attribut nicht verwendet wird, kann die Anwendung immer noch angeben, dass ein Vorgang über ein explizites handle (Bindung oder Serialisierung) verfügt, das den-Befehl umleitet. Zu diesem Zweck wird ein Prototyp mit einem Argument, das einen Handles-Typ enthält, für die IDL-Datei bereitgestellt. Beachten Sie, dass im Standardmodus ein Argument, das nicht zuerst angezeigt wird, auch als Handle verwendet werden kann, das den-Befehl anleitet.

Obwohl das **\[ explizite \_ handle \]** -Attribut eine Möglichkeit ist, dem IDL-Prototyp ein Primitives **\[ explizites \_ handle \]** -Attribut zuzuweisen, ist es nicht unbedingt erforderlich, eine Änderung an der IDL-Datei durchzuführen. Im [**/OSF**](-osf.md) -Modus kann nur das erste Argument als expliziter Handlertyp verwendet werden.

Das **\[ explizite \_ handle \]** -Attribut kann entweder als Schnittstellen Attribut oder als Vorgangs Attribut verwendet werden. Als Schnittstellen Attribut wirkt sich dies auf alle Vorgänge in der-Schnittstelle und alle Typen aus, die die Serialisierungsunterstützung benötigen. Wenn Sie jedoch als Vorgangs Attribut verwendet wird, wirkt sich dies nur auf den jeweiligen Vorgang aus. Wenn eine Methode mindestens ein in- \[ \] Kontext Handle enthält, wird das am weitesten links \[ \] verwendete Kontext Handle als Bindungs Handle verwendet, und es wird kein zusätzliches explizites Handle erstellt.

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

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Automatisches \_ handle**](auto-handle.md)
</dt> <dt>

[**implizites \_ handle**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




