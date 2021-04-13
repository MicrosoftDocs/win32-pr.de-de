---
title: Broadcast-Attribut
description: Das Schlüsselwort \ Broadcast \ gibt an, dass Remote Prozedur Aufrufe an alle Server in einem lokalen Netzwerk gesendet werden.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- Broadcast Attribut-Mittel l
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312852"
---
# <a name="broadcast-attribute"></a>Broadcast-Attribut

Das Schlüsselwort **\[ Broadcast \]** gibt an, dass Remote Prozedur Aufrufe an alle Server in einem lokalen Netzwerk gesendet werden.

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

*Interface-Attribute-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden. Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt zusätzliche Attribute an, die auf die Funktion angewendet werden sollen. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ Broadcast \]** -Attribut angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameter Liste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Broadcast \]** -Schlüsselwort gibt an, dass die Routine immer an alle Server im Netzwerk übermittelt wird, anstatt Sie an einen bestimmten Server zu übermitteln. Der Client empfängt die Ausgabe der ersten Antwort, um erfolgreich zurückzukehren, während nachfolgende Antworten verworfen werden.

Ein Vorgang mit dem **\[ Broadcast \]** -Attribut ist implizit ein [**\[ idempotenter \]**](idempotent.md) Vorgang. Das **\[ Broadcast \]** -Attribut gibt jedoch zusätzliche Eigenschaften an, die Funktionen mit dem **\[ idempotenten \]** Attribut nicht haben. Funktionen, die das **\[ Broadcast \]** -Attribut verwenden, geben insbesondere an, dass die Routine mehrmals als Ergebnis eines Remote Prozedur Aufrufs aufgerufen werden kann. Gleichzeitig können Sie an mehrere Server gesendet werden. Dies unterscheidet sich vom **\[ idempotenten \]** Attribut, das nur angibt, dass ein Aufruf wiederholt werden kann, wenn er nicht abgeschlossen ist.

Wenn eine Remote Prozedur ihren-Aufrufe an alle Hosts in einem lokalen Netzwerk überträgt, muss Sie entweder die [**ncadg \_ -IP- \_ UDP-**](ncadg-ip-udp.md) oder die [**ncadg- \_ IPX**](ncadg-ipx.md) -Protokoll Sequenz verwenden. Beachten Sie, dass die Größe eines **\[ Broadcast \]** Pakets durch den verwendeten Datagramm-Dienst bestimmt wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**auch**](maybe.md)
</dt> <dt>

[**ncadg \_ -IP- \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> </dl>

 

 




