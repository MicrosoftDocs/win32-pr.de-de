---
title: /protocol-Switch
description: Der Schalter /protocol gibt an, welches Wire Protocol vom generierten Stub unterstützt wird.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /protocol switch MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555482677afff83d9f52e06c7b8e445504d222c8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887375"
---
# <a name="protocol-switch"></a>/protocol-Switch

Der Schalter **/protocol** gibt an, welches Wire Protocol vom generierten Stub unterstützt wird.

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>dce


</dt> <dd>

Der generierte Stub unterstützt nur das DCE-Protokoll.

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>ndr64


</dt> <dd>

Der generierte Stub unterstützt nur das Microsoft NDR64-Protokoll.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>all(


</dt> <dd>

Der generierte Stub unterstützt alle verfügbaren Protokolle für eine bestimmte Umgebung.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

RPC marshallt und entmarshalsiert Daten gemäß einem strengen Wire Protocol, das auch als Übertragungssyntax bezeichnet wird und die Darstellung der Datenverkabelung definiert, z. B. die Reihenfolge, in der Datenmember gemarshallt werden, die Ausrichtung der Daten auf dem Kabel, zusätzliche Informationen, die in den Daten enthalten sind, usw. Microsoft RPC ist mit dem NDR-Protokoll (Network Data Representation, Netzwerkdatendarstellung) von OSF DCE kompatibel. In der 64-Bit-Version von Windows XP führt Microsoft ein experimentelles Protokoll NDR64 ein, das für die Übertragung von 64-Bit-Daten optimiert ist. NDR64 ist nicht abwärtskompatibel mit dem DCE-Protokoll.

Das **DCE-Protokoll** ist mit der NDR-Übertragungssyntax von OSF DCE kompatibel. Dieses Protokoll ist für die Übertragung von 32-Bit-Daten optimiert.

Das **ndr64-Protokoll** wird derzeit nur unterstützt, wenn es in Verbindung mit dem [**Schalter /win64**](-win64.md) verwendet wird. Wenn nur ein ndr64-Client versucht, eine Verbindung mit einem reinen DCE-Server herzustellen oder umgekehrt, wird der Aufruf mit RPC \_ S \_ UNSUPPORTED \_ TRANS SYN \_ abgelehnt.

Die Option **all** erstellt einen Stub, der ein beliebiges verfügbares Protokoll verwenden kann. Für 32-Bit-Stubs ist das einzige derzeit verfügbare Protokoll DCE. Für 64-Bit-Stubs, die mit dem Schalter [**/win64**](-win64.md) erstellt wurden, sind sowohl DCE als auch NDR64 verfügbar.

## <a name="examples"></a>Beispiele

**midl /protocol all /win64 filename.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**/&lt;System&gt;**](-system-.md)
</dt> </dl>

 

 




