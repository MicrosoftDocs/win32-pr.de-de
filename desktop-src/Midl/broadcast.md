---
title: Broadcastattribut
description: Das Schlüsselwort \broadcast\ gibt an, dass Remoteprozeduraufrufe an alle Server in einem lokalen Netzwerk gesendet werden.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- Broadcastattribut MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f176b03f9d33ee1bbe1d0e805dfc109de477b7499f8fd624ba7732709dc61a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385236"
---
# <a name="broadcast-attribute"></a>Broadcastattribut

Die **\[ Schlüsselwortübertragung \]** gibt an, dass Remoteprozeduraufrufe an alle Server in einem lokalen Netzwerk gesendet werden.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Gibt eine Liste von null oder mehr IDL-Attributen an, die für die gesamte Schnittstelle gelten. Wenn zwei oder mehr Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt zusätzliche Attribute an, die auf die Funktion angewendet werden sollen. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*returntype* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ \] Broadcastattribut** angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameterliste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \] Broadcastschlüsselwort** gibt an, dass die Routine immer an alle Server im Netzwerk übertragen wird, anstatt an einen bestimmten Server übermittelt zu werden. Der Client empfängt die Ausgabe der ersten Antwort, die erfolgreich zurückgegeben wird, während nachfolgende Antworten verworfen werden.

Ein Vorgang mit dem **\[ \] Broadcastattribut** ist implizit ein [**\[ \] idempotenter**](idempotent.md) Vorgang. Das **\[ \] Broadcastattribut** gibt jedoch zusätzliche Eigenschaften an, über die Funktionen mit dem **\[ idempotenten \]** Attribut nicht verfügen. Insbesondere geben Funktionen, die das **\[ \] Broadcastattribut** verwenden, an, dass die Routine als Ergebnis eines Remoteprozeduraufrufs mehrmals aufgerufen werden kann. Gleichzeitig können sie an mehrere Server gesendet werden. Dies unterscheidet sich vom **\[ idempotenten \]** Attribut, das nur angibt, dass ein Aufruf wiederholt werden kann, wenn er nicht abgeschlossen ist.

Wenn eine Remoteprozedur ihren Aufruf an alle Hosts in einem lokalen Netzwerk überträgt, muss sie entweder die [**ncadg \_ ip \_ udp-**](ncadg-ip-udp.md) oder die [**ncadg \_ ipx-Protokollsequenz**](ncadg-ipx.md) verwenden. Beachten Sie, dass die Größe eines **\[ \] Broadcastpakets** vom verwendeten Datagrammdienst bestimmt wird.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Vielleicht**](maybe.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> </dl>

 

 




